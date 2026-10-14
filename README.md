# .github

Repositorio especial de la organización **TheNextPangeaSL**. GitHub usa su contenido de
forma automática:

| Ruta | Para qué |
| --- | --- |
| [`profile/README.md`](profile/README.md) | Perfil público de la organización en github.com/TheNextPangeaSL. (El README para miembros vive en `.github-private`.) |
| [`SECURITY.md`](SECURITY.md), [`CONTRIBUTING.md`](CONTRIBUTING.md), [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md), [`SUPPORT.md`](SUPPORT.md) | Ficheros por defecto para todos los repositorios que no tengan los suyos. |
| [`.github/pull_request_template.md`](.github/pull_request_template.md), [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Plantillas por defecto de Pull Requests e issues. |
| [`workflow-templates/`](workflow-templates) | Workflows que aparecen en *Actions → New workflow* de cualquier repositorio ("By TheNextPangeaSL"). |

> **Este repositorio es público.** No subas aquí nada interno: ni IDs de cuenta, ni
> nombres de roles, ni URLs de herramientas internas, ni datos de clientes que no estén
> ya en la web.

## Plantillas de workflow

Son una copia de [`platform-workflows/workflow-templates`](https://github.com/TheNextPangeaSL/platform-workflows/tree/development/workflow-templates)
(que es la fuente). Solo crean el fichero inicial de un repositorio; la lógica del
despliegue vive en `platform-workflows` y se actualiza con su tag `@v1`. Si cambias una
plantilla allí, cópiala aquí.

Mantenido por el equipo [DPWG](https://github.com/orgs/TheNextPangeaSL/teams/dpwg).
