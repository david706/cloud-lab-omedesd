---
layout: default
title: Inteligencia artificial
description: Despliegue y uso responsable de modelos de IA en sistemas.
permalink: /ia/
---

## Objetivo

Desplegar un servicio local de inferencia, comprobar su API y analizar sus requisitos de hardware, rendimiento y privacidad.

## Modelo y entorno

<div class="tech-grid">
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-cpu-2"></i></span><div><small>Motor</small><strong>Ollama</strong></div></div>
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-box-model-2"></i></span><div><small>Modelo</small><strong>llama3.2</strong></div></div>
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-memory"></i></span><div><small>Memoria</small><strong>Según modelo</strong></div></div>
  <div class="tech-card"><span class="tech-icon"><i class="ti ti-plug-connected"></i></span><div><small>Puerto</small><strong>11434</strong></div></div>
</div>

## Instalación de Ollama

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## Descargar y ejecutar un modelo

```bash
ollama pull llama3.2
ollama run llama3.2
```

## Consultar los modelos instalados

```bash
ollama list
```

## Probar la API

```bash
curl http://localhost:11434/api/generate \
  -H "Content-Type: application/json" \
  -d '{
    "model": "llama3.2",
    "prompt": "Explica qué es un hipervisor en tres líneas.",
    "stream": false
  }'
```

## Consultar el estado del servicio

```bash
systemctl status ollama --no-pager
ss -lntp | grep 11434
```

## Acceso desde otro equipo de la red

Edita el servicio solo si la práctica requiere acceso remoto y la red está controlada.

```bash
sudo systemctl edit ollama
```

Añade:

```ini
[Service]
Environment="OLLAMA_HOST=0.0.0.0:11434"
```

Después aplica los cambios:

```bash
sudo systemctl daemon-reload
sudo systemctl restart ollama
```

## Pruebas

Registra el tiempo de respuesta, el consumo de RAM o VRAM y las limitaciones observadas.

## Uso responsable

- No envíes datos personales o sensibles al modelo.
- Comprueba la respuesta antes de utilizarla.
- Indica cuándo se ha empleado IA.
- Distingue entre una sugerencia del modelo y una evidencia técnica verificada.

## Conclusiones

Resume los aprendizajes y valora si el modelo y el equipo son adecuados para el servicio propuesto.
