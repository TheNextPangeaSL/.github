# Política de seguridad

En TheNextPangea nos tomamos en serio la seguridad de nuestros productos y de los datos
de nuestros clientes. Si crees haber encontrado una vulnerabilidad en algo nuestro, te
agradecemos que nos la comuniques de forma responsable.

## Cómo informar

**No abras un issue público** ni publiques los detalles hasta que lo hayamos resuelto.

1. **Desde GitHub (preferido):** en el repositorio afectado, pestaña *Security* →
   *Report a vulnerability*. El informe solo lo ve el equipo responsable.
2. **Por correo:** escribe a **contact@thenextpangea.com** con el asunto
   `[SEGURIDAD] <producto o repositorio>`.

Incluye, si puedes:

- Producto, repositorio o URL afectados, y versión.
- Descripción del problema y su impacto.
- Pasos para reproducirlo o una prueba de concepto.
- Cómo prefieres que te contactemos.

## Qué puedes esperar

| Plazo | Qué hacemos |
| --- | --- |
| 2 días laborables | Confirmamos que lo hemos recibido. |
| 10 días laborables | Te damos una primera valoración y el plan de corrección. |
| Al corregirlo | Te avisamos y, si quieres, te reconocemos públicamente. |

Te pedimos que no accedas a datos de terceros más allá de lo imprescindible para
demostrar el problema, que no degrades nuestros servicios y que no hagas pública la
vulnerabilidad hasta acordarlo con nosotros.

## Para el equipo de TheNextPangea

- Nunca subas secretos (claves de AWS, tokens, contraseñas, `.env`) a un repositorio. Si
  ocurre, **rótalos de inmediato**: borrarlos del historial no basta.
- Para desplegar en AWS desde GitHub Actions usa **roles OIDC**, no claves de acceso. El
  DPWG mantiene workflows compartidos y genera el rol de cada repositorio.
- Activa Dependabot y el escaneo de secretos en tus repositorios.

---

<details>
<summary><b>English</b></summary>

Please **do not open public issues** for security problems. Report them privately via
the repository's *Security → Report a vulnerability* tab, or by email to
**contact@thenextpangea.com** with the subject `[SECURITY] <product or repository>`.
We acknowledge reports within 2 business days and share an assessment and fix plan
within 10 business days.

</details>
