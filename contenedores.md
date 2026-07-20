---
layout: default
title: Contenedores
description: Despliegue y administración mediante Docker y Compose.
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
Incluye capturas verificables y explícalas.

## Incidencias y soluciones
Anota los problemas importantes.

## Conclusiones
Explica qué has aprendido.
