# Infraestructura como código

Ejecute los siguientes comandos en Google Cloud Shell desde la carpeta `infra`:

```bash
/usr/bin/terraform init
/usr/bin/terraform plan
```

El resultado esperado de `plan` es **No changes**, porque esta configuración no declara recursos. Es una demostración segura de infraestructura como código; permite evidenciar que Terraform inicializa y compara la configuración sin crear servicios ni incurrir en costos.
