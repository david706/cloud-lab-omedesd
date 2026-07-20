---
layout: default
title: Cloud
description: Servicios cloud, automatización e infraestructura escalable.
permalink: /cloud/
---

## Objetivo

Desplegar una solución cloud sencilla, segura y verificable, justificando recursos, costes y decisiones técnicas.

## Recursos

<div class="responsive-table">
<table>
<thead><tr><th>Recurso</th><th>Servicio</th><th>Región</th><th>Finalidad</th></tr></thead>
<tbody>
<tr><td>Servidor web</td><td>EC2</td><td>us-east-1</td><td>Alojamiento de la aplicación</td></tr>
<tr><td>Contenido estático</td><td>S3</td><td>us-east-1</td><td>Imágenes y copias de seguridad</td></tr>
<tr><td>Control de acceso</td><td>Security Group</td><td>us-east-1</td><td>Permitir SSH y HTTP</td></tr>
</tbody>
</table>
</div>

## Preparación del servidor web

```bash
sudo dnf update -y
sudo dnf install -y httpd
sudo systemctl enable --now httpd
```

En Ubuntu:

```bash
sudo apt update
sudo apt install -y apache2
sudo systemctl enable --now apache2
```

## Crear una página de prueba

```bash
sudo tee /var/www/html/index.html > /dev/null <<'HTML'
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <title>Cloud Lab</title>
</head>
<body>
  <h1>Cloud Lab funcionando</h1>
  <p>Servidor desplegado correctamente.</p>
</body>
</html>
HTML
```

## Comprobaciones

```bash
systemctl status httpd --no-pager
curl -I http://localhost
```

En Ubuntu sustituye `httpd` por `apache2`.

## Copia de seguridad en S3 desde CloudShell

```bash
fecha=$(date +%F-%H%M)
tar -czf "backup-${fecha}.tar.gz" /ruta/del/proyecto
aws s3 cp "backup-${fecha}.tar.gz" s3://NOMBRE-DEL-BUCKET/backups/
```

## Seguridad y costes

- Limita los puertos del grupo de seguridad.
- Evita dejar SSH abierto a todo Internet.
- Detén o elimina los recursos que no utilices.
- Comprueba el consumo en Cost Explorer.
- No publiques claves ni credenciales en el repositorio.

## Evidencias

Documenta la instancia, el grupo de seguridad, la web accesible y el recurso almacenado en S3.

## Conclusiones

Valora la solución y explica qué cambiarías para hacerla más segura, disponible o escalable.
