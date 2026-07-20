# Cloud Lab

Plantilla del proyecto profesional del módulo.

## Nombre del repositorio

Cada alumno debe renombrarlo con este formato:

```text
cloud-lab-apellido-inicial
```

Ejemplo:

```text
cloud-lab-garcia-j
```

## Preparación

1. Renombra la carpeta.
2. Edita `mkdocs.yml`.
3. Sustituye los datos de ejemplo por los tuyos.
4. Instala MkDocs:

```bash
python -m pip install -r requirements.txt
```

5. Prueba la web:

```bash
python -m mkdocs serve
```

## Subida a GitHub

Crea un repositorio vacío en GitHub con el mismo nombre y copia los comandos que GitHub muestra en la pantalla de creación.

Ejemplo:

```bash
git init
git add .
git commit -m "Inicio de Cloud Lab"
git branch -M main
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

La URL y el usuario deben ser los de cada alumno.
