# Invitación de Boda - Itzel & Javier

Invitación web para la boda de Itzel y Javier el 13 de Diciembre de 2025.

## Instrucciones para publicar en GitHub Pages

### Paso 1: Crear un repositorio en GitHub

1. Ve a [GitHub](https://github.com) e inicia sesión
2. Haz clic en el botón "+" en la esquina superior derecha y selecciona "New repository"
3. Nombra tu repositorio (por ejemplo: `boda-itzel-javier`)
4. Marca la opción "Public"
5. Haz clic en "Create repository"

### Paso 2: Subir los archivos al repositorio

Tienes dos opciones:

#### Opción A: Usando la interfaz web de GitHub

1. En tu nuevo repositorio, haz clic en "uploading an existing file"
2. Arrastra los archivos `index.html` y `novios.jpg` a la página
3. Escribe un mensaje de commit (por ejemplo: "Agregar invitación de boda")
4. Haz clic en "Commit changes"

#### Opción B: Usando Git desde la terminal

```bash
cd C:\Users\foro7\Downloads\boda-itzel-javier
git init
git add .
git commit -m "Agregar invitación de boda"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/boda-itzel-javier.git
git push -u origin main
```

(Reemplaza `TU-USUARIO` con tu nombre de usuario de GitHub)

### Paso 3: Activar GitHub Pages

1. En tu repositorio de GitHub, ve a "Settings" (Configuración)
2. En el menú lateral izquierdo, haz clic en "Pages"
3. En "Source" (Fuente), selecciona "main" branch
4. Haz clic en "Save" (Guardar)
5. Espera unos minutos mientras GitHub publica tu sitio

### Paso 4: Acceder a tu invitación

Tu invitación estará disponible en:
```
https://TU-USUARIO.github.io/boda-itzel-javier/
```

(Reemplaza `TU-USUARIO` con tu nombre de usuario de GitHub)

## Características de la invitación

- Diseño elegante y responsive (se adapta a móviles y tablets)
- Foto de los novios
- Historia de la pareja
- Detalles de la ceremonia religiosa con enlace a Google Maps
- Información de la recepción
- Código de vestimenta
- Animaciones suaves y efectos visuales

## Personalización

Si necesitas hacer cambios:

1. Edita el archivo `index.html`
2. Para cambiar la foto, reemplaza `novios.jpg`
3. Sube los cambios a GitHub y se actualizarán automáticamente

## Notas

- El enlace al mapa de la recepción está incompleto en los datos originales. Por favor actualízalo en el HTML.
- Los colores principales son morado/azul, pero puedes cambiarlos editando los valores en la sección `<style>`
