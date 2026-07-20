---
layout: default
title: Inicio
hero: true
---
<div class="dashboard-grid">
<a class="module-card" href="{{ '/virtualizacion/' | relative_url }}"><span class="module-icon"><i class="ti ti-server-2"></i></span><h2>Virtualización</h2><p>Hipervisores, máquinas virtuales, redes y almacenamiento.</p><span class="module-link">Abrir documentación <i class="ti ti-arrow-up-right"></i></span></a>
<a class="module-card" href="{{ '/contenedores/' | relative_url }}"><span class="module-icon"><i class="ti ti-packages"></i></span><h2>Contenedores</h2><p>Docker, Compose, volúmenes, redes y administración.</p><span class="module-link">Abrir documentación <i class="ti ti-arrow-up-right"></i></span></a>
<a class="module-card" href="{{ '/cloud/' | relative_url }}"><span class="module-icon"><i class="ti ti-topology-ring-3"></i></span><h2>Cloud</h2><p>Servicios, arquitectura, automatización, seguridad y costes.</p><span class="module-link">Abrir documentación <i class="ti ti-arrow-up-right"></i></span></a>
<a class="module-card" href="{{ '/ia/' | relative_url }}"><span class="module-icon"><i class="ti ti-cpu-2"></i></span><h2>Inteligencia artificial</h2><p>Modelos locales, inferencia y servicios aplicados a sistemas.</p><span class="module-link">Abrir documentación <i class="ti ti-arrow-up-right"></i></span></a>
</div>
<div class="overview"><section class="panel"><h2>Progreso del proyecto</h2><p>Actualiza el valor <code>progress</code> en <code>_config.yml</code> al cerrar un hito.</p><div class="progress"><span style="width: {{ site.progress }}%"></span></div><p><strong>{{ site.progress }} % completado</strong></p></section><section class="panel"><ul class="milestones"><li><span>Sesión inicial</span><span class="status done">En curso</span></li><li><span>Virtualización</span><span class="status">Pendiente</span></li><li><span>Contenedores</span><span class="status">Pendiente</span></li><li><span>Cloud</span><span class="status">Pendiente</span></li></ul></section></div>
