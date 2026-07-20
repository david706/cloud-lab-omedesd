---
layout: default
title: Contenedores
description: Despliegue y administración de servicios mediante Docker y Compose.
permalink: /contenedores/
---

## Objetivo

Desplegar servicios reproducibles mediante Docker y Docker Compose, documentando imágenes, redes, volúmenes y comprobaciones.

## Servicios desplegados

<div class="responsive-table">
<table>
<thead><tr><th>Servicio</th><th>Imagen</th><th>Puerto</th><th>Estado</th></tr></thead>
<tbody>
<tr><td>Web</td><td><code>nginx:alpine</code></td><td>8080</td><td><span class="badge pending">Pendiente</span></td></tr>
<tr><td>Administración</td><td><code>portainer/portainer-ce</code></td><td>9443</td><td><span class="badge pending">Pendiente</span></td></tr>
</tbody>
</table>
</div>

## Instalación de Docker

```bash
sudo apt update
sudo apt install -y docker.io docker-compose-plugin
sudo systemctl enable --now docker
sudo usermod -aG docker "$USER"
```

Después de añadir el usuario al grupo `docker`, cierra la sesión y vuelve a entrar.

## Archivo Compose completo

```yaml
services:
  web:
    image: nginx:alpine
    container_name: cloudlab-web
    restart: unless-stopped
    ports:
      - "8080:80"
    volumes:
      - ./html:/usr/share/nginx/html:ro
    networks:
      - cloudlab

  portainer:
    image: portainer/portainer-ce:latest
    container_name: cloudlab-portainer
    restart: unless-stopped
    ports:
      - "9443:9443"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
      - portainer_data:/data
    networks:
      - cloudlab

networks:
  cloudlab:
    driver: bridge

volumes:
  portainer_data:
```

## Puesta en marcha

```bash
docker compose config
docker compose up -d
docker compose ps
```

## Comprobaciones

```bash
docker ps
docker logs cloudlab-web
curl -I http://localhost:8080
```

## Parada y limpieza

```bash
docker compose down
```

Para eliminar también los volúmenes:

```bash
docker compose down -v
```

## Evidencias

Incluye capturas de `docker compose ps`, de la aplicación funcionando y de la configuración relevante. Explica qué demuestra cada una.

## Incidencias y soluciones

Anota los problemas relevantes, su diagnóstico y la solución aplicada.

## Conclusiones

Explica qué has aprendido sobre aislamiento, persistencia y redes de contenedores.
