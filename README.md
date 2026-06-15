# Calificador de Moodle · Embebible

Versión de archivo único preparada para publicar mediante GitHub Pages e incorporar en Google Sites.

## Publicación versionada

La publicación pública versionada se administra desde el repositorio principal `calificador-de-moodle`:

- `https://profesorbombina.github.io/calificador-de-moodle/`: versión estable.
- `https://profesorbombina.github.io/calificador-de-moodle/v2/`: vista previa V2.

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

1. Publicá los cambios del proyecto principal en `codex/v2`.
2. El repositorio principal generará y actualizará automáticamente la vista previa.
3. Este repositorio conserva la versión embebible sincronizada para Google Sites.

## Incorporación en Google Sites

1. Abrí el sitio en modo edición.
2. Elegí **Insertar > Incorporar > URL**.
3. Pegá la URL de GitHub Pages.
4. Ajustá el alto del bloque para visualizar el dashboard completo.

## Dependencias externas

La interfaz, estilos y lógica están contenidos en `index.html`. La aplicación mantiene dependencias externas cargadas mediante CDN:

- SheetJS para leer y generar planillas.
- Google Fonts para la tipografía.
