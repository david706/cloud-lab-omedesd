---
layout: default
title: Virtualización
description: Diseño, creación y administración de infraestructuras virtualizadas.
permalink: /virtualizacion/
---
## Objetivo
Explica qué infraestructura vas a construir y qué problema resolverá.

> **Resultado esperado:** una infraestructura funcional, validada y documentada con evidencias propias.

## Arquitectura
![Arquitectura de ejemplo](../imagenes/arquitectura-ejemplo.svg)

## Datos técnicos

<div class="tech-grid">
  <div class="tech-card">
    <span class="tech-icon"><i class="ti ti-server-2"></i></span>
    <div><small>Hipervisor</small><strong>Proxmox VE</strong></div>
  </div>
  <div class="tech-card">
    <span class="tech-icon"><i class="ti ti-cpu"></i></span>
    <div><small>Procesador</small><strong>4 vCPU</strong></div>
  </div>
  <div class="tech-card">
    <span class="tech-icon"><i class="ti ti-device-desktop-analytics"></i></span>
    <div><small>Memoria RAM</small><strong>8 GB</strong></div>
  </div>
  <div class="tech-card">
    <span class="tech-icon"><i class="ti ti-network"></i></span>
    <div><small>Red</small><strong>Bridge vmbr0</strong></div>
  </div>
</div>

> Sustituye los valores de ejemplo por la configuración real de tu infraestructura.

## Procedimiento
1. Describe el primer paso.
2. Explica las decisiones tomadas.
3. Añade evidencias relevantes.

## Comandos utilizados
```bash
ip addr
```

## Validación
- [ ] La máquina arranca.
- [ ] La red funciona.
- [ ] Los servicios responden.

## Incidencias y soluciones
Describe una incidencia real, su causa y la solución aplicada.

## Conclusiones
Resume lo aprendido y las mejoras propuestas.
