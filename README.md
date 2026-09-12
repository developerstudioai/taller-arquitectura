# EventFlow

Ejercicio del Taller de Arquitectura en la Nube. EventFlow es una aplicación web estática y deliberadamente simple para simular la venta de entradas a eventos.

## Ejecutar localmente

No requiere instalación. Abra `index.html` en un navegador o use un servidor estático, por ejemplo:

```bash
python3 -m http.server 8080
```

Después abra `http://localhost:8080`.

## Contenido del repositorio

- `index.html`: aplicación monolítica mínima usada para la demostración y el análisis de deuda técnica.
- `docs/`: backlog, decisiones arquitectónicas, diagramas PlantUML y contrato API.
- `infra/`: configuración Terraform segura para ejecutar `init` y `plan` sin crear recursos.
- `.github/workflows/ci.yml`: validación mínima en GitHub Actions.
- `sonar-project.properties`: configuración base para analizar el proyecto con SonarQube Cloud.

## Deuda técnica intencional

El ejercicio conserva CSS incrustado y manejadores `onclick` en el HTML. Son decisiones intencionalmente simples para que SonarQube Cloud pueda mostrar problemas de mantenibilidad. La mejora propuesta está documentada en `docs/deuda-tecnica.md`.

## Seguridad y costos

No ejecute `terraform apply` para este taller. `terraform init` y `terraform plan` no crean recursos de Google Cloud con la configuración incluida.
