# Calificador de Moodle · Embebible

Versión de archivo único preparada para publicar mediante GitHub Pages e incorporar en Google Sites.

## Versiones publicadas

GitHub Pages se despliega mediante `.github/workflows/pages-versionadas.yml`:

- `/`: versión estable construida desde `main`.
- `/v2/`: vista previa de la versión 2 construida desde `codex/v2`.

Cada cambio publicado en `codex/v2` actualiza la vista previa sin modificar la versión estable.

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

1. En GitHub, abrí **Settings > Pages**.
2. En **Build and deployment > Source**, seleccioná **GitHub Actions**.
3. Ejecutá el workflow **Publicar versiones en GitHub Pages**.
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
