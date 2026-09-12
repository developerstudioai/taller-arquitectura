# Arquitectura de EventFlow

## Definición

La arquitectura de software es la estructura de un sistema, comprendida por sus elementos de software, las propiedades visibles de esos elementos y las relaciones entre ellos.

## Atributos de calidad

| Atributo | Escenario | Decisión |
|---|---|---|
| Escalabilidad | 10.000 usuarios en un minuto al iniciar la venta. | Réplicas del servicio de pedidos, caché y colas. |
| Seguridad | Los datos de pago deben estar protegidos. | HTTPS, tokenización y secretos fuera del código. |
| Disponibilidad | Una compra no debe perderse ante un fallo. | Réplicas y persistencia de órdenes. |
| Rendimiento | El catálogo debe mostrarse en menos de dos segundos. | Índices, paginación y caché. |
| Mantenibilidad | Pagos debe cambiar sin modificar catálogo. | Límites claros, APIs y pruebas. |

## Stakeholders

| Interesado | Necesidad principal |
|---|---|
| Comprador | Aplicación rápida, clara y confiable. |
| Organizador | Inventario correcto y ventas visibles. |
| Finanzas | Pagos seguros y trazables. |
| Desarrollo | Código fácil de mantener y probar. |
| Operaciones | Despliegues repetibles y monitoreo. |

## Decisión propuesta

EventFlow puede comenzar como monolito en capas. Si el volumen de venta exige escalar pedidos sin duplicar todo el sistema, se puede evolucionar a microservicios orientados a eventos. Microservicios no son una mejora automática: agregan comunicación distribuida, despliegues independientes y consistencia eventual.
