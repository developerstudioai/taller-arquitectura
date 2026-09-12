# SonarQube Community autoalojado

## Decisión

Para el taller se usará SonarQube Community autoalojado como alternativa gratuita a SonarQube Cloud. Es un servidor de análisis estático; no pertenece a Bitbucket, aunque puede integrarse con Bitbucket Cloud y con otros proveedores de código.

## Justificación

- No exige suscripción mensual para analizar un proyecto pequeño como EventFlow.
- Permite detectar bugs, vulnerabilidades, code smells y calcular un Quality Gate en la rama principal.
- Puede ejecutarse en un equipo local mediante Docker o en un servidor/VPS con soporte para Docker.
- Es suficiente para evidenciar deuda técnica intencional: estilos incrustados, eventos `onclick` y compra simulada.

## Limitaciones

- Tiene menos capacidades de análisis de ramas y pull requests que planes Cloud o comerciales.
- La integración y automatización avanzada requieren más configuración manual.
- El responsable de la instancia debe operar la infraestructura.

## Operación y mantenimiento

El administrador debe actualizar la imagen de SonarQube, mantener una base de datos compatible en producción, realizar copias de seguridad, controlar usuarios y tokens, proteger el acceso HTTPS y vigilar disco, memoria y logs. Para pruebas locales puede usarse Docker; para una instancia compartida debe emplearse un servidor o proveedor de alojamiento que soporte Docker y almacenamiento persistente.
