# Calificador de Moodle · Embebible

Versión de archivo único preparada para publicar mediante GitHub Pages e incorporar en Google Sites.

## Versiones publicadas

GitHub Pages continúa publicando la rama `main` y el workflow `.github/workflows/pages-versionadas.yml` actualiza la vista previa:

- `/`: versión estable conservada en la raíz de `main`.
- `/v2/`: copia automática de la versión 2 desarrollada en `codex/v2`.

Cada cambio publicado en `codex/v2` actualiza solamente la carpeta `v2/` de `main`, sin modificar el `index.html` estable.

## Importante

`index.html` es generado automáticamente desde el proyecto principal `calificador-de-moodle-v1`.

No realices cambios funcionales directamente en este archivo porque se reemplazarán durante la próxima sincronización.

## Sincronización

Después de modificar el proyecto principal, ejecutá desde su carpeta:

```powershell
node tools/build-embeddable.js
```

El generador combina:

- `index.html`
- `styles.css`
- `app.js`
- Ajustes responsive específicos para Google Sites

## Publicación

1. GitHub Pages debe publicar la rama `main` y la carpeta raíz.
2. Publicá los cambios embebibles en `codex/v2`.
3. El workflow **Publicar vista previa V2** actualizará automáticamente `main/v2/`.
4. Usá la URL raíz para V1 y agregá `/v2/` para revisar V2.

## Incorporación en Google Sites

1. Abrí el sitio en modo edición.
2. Elegí **Insertar > Incorporar > URL**.
3. Pegá la URL de GitHub Pages.
4. Ajustá el alto del bloque para visualizar el dashboard completo.

## Dependencias externas

La interfaz, estilos y lógica están contenidos en `index.html`. La aplicación mantiene dependencias externas cargadas mediante CDN:

- SheetJS para leer y generar planillas.
- Google Fonts para la tipografía.
