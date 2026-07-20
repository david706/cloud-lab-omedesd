---
layout: default
title: Contenedores
description: Despliegue y administración de servicios mediante Docker y Compose.
permalink: /contenedores/
---
## Objetivo
Documenta el objetivo del hito.
## Servicios desplegados
| Servicio | Imagen | Puerto | Estado |
|---|---|---:|---|
| Ejemplo | nginx:alpine | 8080 | Pendiente |
## Archivo Compose
```yaml
services:
  web:
    image: nginx:alpine
    ports:
      - "8080:80"
```
## Evidencias
Incluye capturas verificables y explica qué demuestra cada una.
## Incidencias y soluciones
Anota los problemas relevantes.
## Conclusiones
Explica qué has aprendido.
