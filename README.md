# Localizador Visual de Almacén — Farmacias San Camilo

Escanea un producto (pistola o cámara del celular) y la página muestra **dónde va**:
croquis del almacén con la ruta a la fila, rejilla anaquel × charola con la celda
parpadeando y la existencia según el último archivo.

**URL:** `https://retana1885.github.io/buscador/`

## Qué hace

- Búsqueda por código de barras (principal y secundarios), código interno o nombre.
  Ignora ceros a la izquierda (Excel se los come).
- **Modo escáner (pistola)**: el campo mantiene el foco y se limpia tras cada lectura (ON en PC).
- **Modo cámara** 📷: funciona en iPhone y Android (HTTPS). Beep + vibración al detectar,
  lámpara si el teléfono lo permite.
- Tema claro/oscuro y estilo de fondo (botones arriba a la derecha; se recuerdan por navegador).
- Fila 8 = zona de tarimas junto a recepción (se muestra "A PISO", sin anaquel/charola).
- Tras la primera búsqueda el buscador se hace panel lateral (PC) o barra compacta (celular)
  para que el mapa quede completo en pantalla.

## Cómo actualizar posiciones

1. Reemplazar `posiciones_buscador.xlsx` en este repositorio (rama `main`), igual que siempre.
2. Esperar 1-2 min el despliegue de Pages y recargar con Ctrl+F5.

Columnas requeridas: `Cod. De Barras`, `Secundarios`, `Codigo`, `Nombre`, `Fila`, `Anaquel`,
`Charola`. La hoja 2 (existencias con `Art_Codigo` / `AA_ExistenciaActualU`) es opcional.

## Archivos

- `index.html` — la aplicación (versión visual "Centro de Mando", ago-2026).
- `v1.html` — respaldo de la versión anterior (solo texto).
- `posiciones_buscador.xlsx` — fuente de datos.
- `favicono.ico`, `logo_sancamilo.png` — identidad.

La fuente de trabajo local vive en `C:\desarrollos\buscador_posiciones_v2` (y el xlsx
maestro en `C:\desarrollos\buscador_posiciones`).
