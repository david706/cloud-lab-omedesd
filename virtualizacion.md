---
layout: default
title: Virtualización
description: Diseño, creación y administración de infraestructuras virtualizadas.
permalink: /virtualizacion/
---

## Objetivo

Construir una infraestructura virtual funcional, justificar sus recursos y dejar evidencias verificables de su funcionamiento.

> **Resultado esperado:** una máquina virtual o contenedor operativo, con red, almacenamiento y servicios correctamente documentados.

## Arquitectura

![Arquitectura de ejemplo](../imagenes/arquitectura-ejemplo.svg)

## Datos técnicos

<div class="tech-grid">
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-server-2"></i></span><div><small>Hipervisor</small><strong>Proxmox VE</strong></div></div>
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-cpu"></i></span><div><small>Procesador</small><strong>4 vCPU</strong></div></div>
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-device-desktop-analytics"></i></span><div><small>Memoria RAM</small><strong>8 GB</strong></div></div>
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-network"></i></span><div><small>Red</small><strong>Bridge vmbr0</strong></div></div>
</div>

> Sustituye los valores de ejemplo por la configuración real de tu infraestructura.

## Procedimiento

1. Crear la máquina virtual o el contenedor.
2. Asignar CPU, memoria y almacenamiento.
3. Configurar la interfaz de red.
4. Instalar el sistema operativo.
5. Comprobar conectividad y servicios.

## Comandos utilizados

### Consultar las interfaces de red

```bash
ip addr
```

### Consultar la puerta de enlace y las rutas

```bash
ip route
```

### Comprobar la resolución DNS

```bash
getent hosts archive.ubuntu.com
```

### Comprobar conectividad

```bash
ping -c 4 8.8.8.8
ping -c 4 archive.ubuntu.com
```

### Verificar recursos del sistema

```bash
lscpu
free -h
lsblk
```

### Actualizar el sistema

```bash
sudo apt update
sudo apt upgrade -y
```

### Consultar los servicios activos

```bash
systemctl --type=service --state=running
```

## Validación

- [ ] La máquina arranca correctamente.
- [ ] Tiene una dirección IP válida.
- [ ] La puerta de enlace responde.
- [ ] La resolución DNS funciona.
- [ ] Los servicios requeridos están activos.
- [ ] Las capturas demuestran el resultado.

## Incidencias y soluciones

Describe una incidencia real, su causa, las pruebas realizadas y la solución aplicada.

## Conclusiones

Resume lo aprendido y las mejoras que introducirías en una siguiente versión.
