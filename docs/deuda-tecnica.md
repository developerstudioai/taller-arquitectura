# Deuda técnica y SonarQube Cloud

La aplicación conserva algunos problemas a propósito para que el análisis de calidad tenga algo que reportar.

| Mal olor | Problema | Refactorización propuesta |
|---|---|---|
| CSS dentro de `index.html` | Mezcla estructura y presentación. | Mover estilos a `styles.css`. |
| `onclick` en el HTML | Mezcla comportamiento e interfaz. | Crear `app.js` y usar `addEventListener`. |
| Datos escritos directamente en la página | El catálogo no tiene modelo ni API. | Cargar eventos desde una API. |
| Compra simulada | No crea orden ni valida inventario real. | Crear orden, validar cupo y persistirla. |

## Evidencia requerida

En SonarQube Cloud, importar el repositorio `developerstudioai/taller-arquitectura`, ejecutar el análisis y capturar el panel que muestre el nombre del proyecto, fecha de análisis y code smells. La pantalla de un SonarQube con otros proyectos no sustituye esta evidencia.
