# Cómo contribuir

Guía común para los repositorios de TheNextPangea. Si un repositorio tiene su propio
`CONTRIBUTING.md`, manda ese.

## Ramas

| Rama | Para qué |
| --- | --- |
| `development` | Integración diaria. Despliega al entorno de desarrollo. Es la rama por defecto. |
| `staging` | Validación con datos reales o cliente. Despliega a staging. |
| `main` / `production` | Lo que está en producción, si el proyecto la tiene. |
| `feat/…`, `fix/…`, `chore/…` | Ramas de trabajo, cortas, que salen de `development`. |

Nunca se hace push directo a `staging` ni a producción: se llega por Pull Request.

## Commits

Usamos [Conventional Commits](https://www.conventionalcommits.org/es/), en inglés:

```
feat(backend): add budget alerts per project
fix(frontend): keep filters when changing page
ci: deploy through the shared platform workflows
```

Tipos habituales: `feat`, `fix`, `refactor`, `perf`, `test`, `docs`, `ci`, `chore`.
Si la tarea está en ClickUp, añade su identificador al final: `(CU-1240ccejkka)`.

## Pull Requests

1. Una PR, un cambio. Si crece mucho, divídela.
2. Rellena la plantilla: qué cambia, por qué y cómo se ha probado.
3. Los checks de CI tienen que pasar antes de pedir revisión.
4. Al menos una aprobación de alguien del equipo del repositorio.
5. Se fusiona con *squash* o *merge commit* según el repositorio; borra la rama al
   terminar.

## Código

- Código, nombres, comentarios y commits en **inglés**; la interfaz de usuario, en el
  idioma del cliente (normalmente español).
- Antes de abrir la PR: linter, formateador y tests del proyecto en verde.
- Nada de secretos en el repositorio: usa variables de entorno, GitHub Secrets o AWS
  Secrets Manager. Consulta la [política de seguridad](SECURITY.md).

## Despliegues en AWS

- Los workflows de GitHub Actions se autentican con **roles OIDC**, nunca con claves de
  acceso guardadas en Secrets.
- Usa los workflows compartidos de
  [`platform-workflows`](https://github.com/TheNextPangeaSL/platform-workflows)
  (`deploy-ecs.yml`, `deploy-s3-static.yml`) en lugar de copiar pasos de despliegue en
  cada repositorio.
- Etiqueta los recursos que crees con `Project=<proyecto>` para que su coste se atribuya
  bien.
- ¿Dudas con CI, AWS o un rol nuevo? Pregunta al equipo
  [DPWG](https://github.com/orgs/TheNextPangeaSL/teams/dpwg).
