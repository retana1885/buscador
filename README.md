# Sistema de Localizacion de Productos en almacén 

Aplicacion web estatica para buscar la ubicacion fisica de productos en almacen a partir de un archivo Excel oficial.

## Que hace

- Carga automaticamente el archivo base `posiciones_buscador.xlsx`.
- Permite buscar por codigo de barras, codigos secundarios, codigo o nombre/descripcion.
- Prioriza coincidencias exactas e inicio para resultados mas utiles.
- Muestra ubicacion principal del producto: `Fila`, `Anaquel`, `Charola`.
- Incluye modo escaner: limpia el campo y mantiene el foco tras cada busqueda.

## Estructura esperada del Excel

El archivo `posiciones_buscador.xlsx` debe contener encabezados compatibles con:

- `Cod. De Barras` (o similar)
- `Secundarios` (opcional)
- `Codigo`
- `Nombre` o `Descripcion`
- `Fila`
- `Anaquel`
- `Charola`

La app detecta columnas por nombre, por lo que variaciones comunes en mayusculas/minusculas suelen funcionar.

## Ejecucion local

Desde la carpeta del proyecto:

```bash
python -m http.server 5500
```

Abrir en navegador:

`http://localhost:5500/index.html`

## Publicacion en GitHub Pages

1. Subir cambios a la rama `main`.
2. Verificar en `Settings > Pages`:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/(root)`
3. Esperar el workflow `Pages-Build-Deployment` en `Actions`.
4. Abrir:
   - `https://retana1885.github.io/buscador/`

## Como actualizar posiciones

1. Reemplazar `posiciones_buscador.xlsx` por la version nueva.
2. Subir el archivo al repositorio en `main`.
3. Esperar el despliegue de Pages.

## Notas

- Si no ves cambios, recarga con cache forzada (`Ctrl + F5`).
- No abrir con `file://`; usar servidor local o GitHub Pages para carga automatica del Excel.
