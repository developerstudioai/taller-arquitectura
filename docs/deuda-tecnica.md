# Deuda técnica y SonarQube Community

La aplicación conserva algunos problemas a propósito para que el análisis de calidad tenga algo que reportar.

| Mal olor | Problema | Refactorización propuesta |
|---|---|---|
| CSS dentro de `index.html` | Mezcla estructura y presentación. | Mover estilos a `styles.css`. |
| `onclick` en el HTML | Mezcla comportamiento e interfaz. | Crear `app.js` y usar `addEventListener`. |
| Datos escritos directamente en la página | El catálogo no tiene modelo ni API. | Cargar eventos desde una API. |
| Compra simulada | No crea orden ni valida inventario real. | Crear orden, validar cupo y persistirla. |

## Alternativa gratuita recomendada

Se recomienda SonarQube Community autoalojado. No es un producto de Bitbucket; es un servidor de análisis estático que puede integrarse con repositorios y pipelines de Bitbucket o GitHub. La instancia se puede ejecutar localmente en Docker o desplegarse en un servidor, VPS o alojamiento que soporte Docker.

La ventaja es evitar una suscripción mensual para un taller pequeño. La contrapartida es que el equipo administra actualizaciones, seguridad, usuarios, tokens, copias de seguridad y almacenamiento. Community se enfoca en el análisis de la rama principal y no ofrece todas las funciones avanzadas de ediciones Cloud o comerciales, pero es suficiente para encontrar y explicar code smells de EventFlow.

## Evidencia requerida

En SonarQube Community, crear o importar un proyecto EventFlow, ejecutar el análisis y capturar el panel que muestre el nombre del proyecto, fecha de análisis y code smells. La pantalla de un SonarQube con otros proyectos solo sirve como evidencia de acceso, no del análisis de EventFlow.
