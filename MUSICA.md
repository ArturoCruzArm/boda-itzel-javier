# Instrucciones para agregar "Mi Bendición" de Juan Luis Guerra

## Opción 1: Subir el archivo MP3 al repositorio (Recomendado)

1. Descarga "Mi Bendición - Juan Luis Guerra" en formato MP3
2. Renombra el archivo a: `mi-bendicion.mp3`
3. Sube el archivo al repositorio en GitHub:
   - Ve a https://github.com/ArturoCruzArm/boda-itzel-javier
   - Haz clic en "Add file" → "Upload files"
   - Arrastra el archivo `mi-bendicion.mp3`
   - Haz commit de los cambios

4. Actualiza la línea 630 del `index.html` con:
   ```html
   <source src="mi-bendicion.mp3" type="audio/mpeg">
   ```

## Opción 2: Usar un servicio de hosting de audio

Si el archivo MP3 es muy grande, puedes usar servicios como:

- **Google Drive**: Sube el archivo y obtén un enlace público
- **Dropbox**: Similar a Google Drive
- **SoundCloud** o servicios especializados

Luego actualiza la URL en la línea 630 del archivo HTML.

## Nota sobre la reproducción automática

La música está configurada para:
- ✅ Reproducirse al PRIMER CLIC en cualquier parte de la página
- ✅ Reproducirse al hacer scroll por primera vez
- ✅ Tener un botón flotante para pausar/continuar

**Importante**: Los navegadores modernos bloquean la reproducción automática de audio sin interacción del usuario por políticas de privacidad. Por eso la música se reproduce en la primera interacción (clic o scroll).

## Estado actual

Actualmente usa una canción de prueba temporal. Reemplázala con "Mi Bendición" siguiendo las instrucciones arriba.
