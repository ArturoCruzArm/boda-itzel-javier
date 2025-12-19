# Selector de Fotos - Boda Itzel & Javier

Sistema interactivo para seleccionar fotos del evento para diferentes propósitos: ampliación, impresión, invitaciones, etc.

## Estado Actual

- **Fotos convertidas**: 541 fotos en formato WebP
- **Origen**: `F:\2025\12\13\boda-itzel-javier\boda Luz`
- **Destino**: `D:\eventos\boda-itzel-javier\images`
- **Espacio ahorrado**: 96.2% (3.0 GB reducidos a 122.1 MB)

## Cómo Usar

### 1. Abrir el Selector

Simplemente abre `selector.html` en tu navegador web preferido.

### 2. Seleccionar Fotos

1. **Click en una foto** para abrir el modal de selección
2. **Elige una o varias opciones:**
   - 🖼️ Ampliación
   - 📸 Impresión
   - 💌 Invitación
   - ❌ Descartar

3. **Click en "Guardar"** para confirmar
   - Las selecciones se guardan automáticamente en tu navegador
   - No perderás tu progreso al cerrar la página

### 3. Usar los Filtros

En la parte superior puedes filtrar las fotos por categoría:
- **Todas**: Muestra todas las fotos (541 fotos)
- **Ampliación**: Solo fotos marcadas para ampliar
- **Impresión**: Solo fotos marcadas para imprimir
- **Invitación**: Solo fotos marcadas para invitaciones
- **Descartadas**: Fotos que no se usarán
- **Sin Clasificar**: Fotos que aún no has revisado

### 4. Exportar Resultados

#### Descargar Reporte (JSON)

Click en el botón "📥 Descargar Reporte" para obtener un archivo JSON con:
- Total de fotos
- Estadísticas por categoría
- Lista detallada de cada foto y sus categorías

#### Copiar Resumen

Click en "📤 Copiar Resumen" para copiar al portapapeles un resumen en texto plano.

## Características

- **Guardado Automático**: Las selecciones se guardan en localStorage del navegador
- **Filtros Inteligentes**: Filtra por cualquier categoría
- **Diseño Responsive**: Funciona en desktop, tablet y móvil
- **Atajos de Teclado**:
  - `Esc` - Cerrar modal sin guardar
  - `Enter` - Guardar y cerrar
  - `←` / `→` - Navegar entre fotos en el modal
- **Selección Múltiple**: Una foto puede tener varias categorías

## Agregar Más Fotos

Si necesitas agregar más fotos después:

1. Coloca las nuevas fotos en `F:\2025\12\13\boda-itzel-javier\boda Luz`
2. Ejecuta: `python convertir_a_webp.py`
3. Ejecuta: `python generar_lista_fotos.py`
4. Recarga `selector.html` en el navegador (F5)

**Nota**: Tus selecciones previas se mantendrán intactas.

## Estructura de Archivos

```
boda-itzel-javier/
├── selector.html              # Página principal del selector
├── convertir_a_webp.py        # Script para convertir fotos a WebP
├── generar_lista_fotos.py     # Script para actualizar la lista
├── SELECTOR_FOTOS_README.md   # Esta documentación
│
├── css/
│   └── selector.css           # Estilos del selector
│
├── js/
│   ├── selector.js            # Lógica del selector
│   └── proteccion.js          # Placeholder de protección
│
└── images/                    # Directorio de fotos (541 fotos WebP)
    ├── DSC_0393.webp
    ├── DSC_0398.webp
    └── ...
```

## Usar el Reporte JSON

El archivo JSON descargado puede usarse para copiar automáticamente las fotos seleccionadas:

### Python - Copiar fotos para ampliación

```python
import json
import shutil
from pathlib import Path

# Leer el reporte
with open('seleccion-fotos-boda-2025-12-19.json', 'r') as f:
    data = json.load(f)

# Crear directorio destino
Path('fotos_ampliacion').mkdir(exist_ok=True)

# Copiar fotos para ampliación
for foto in data['selecciones']:
    if foto['ampliacion']:
        origen = foto['archivo']
        destino = f"fotos_ampliacion/{Path(origen).name}"
        shutil.copy2(origen, destino)
        print(f"Copiada: {Path(origen).name}")

print(f"\nTotal de fotos copiadas: {data['estadisticas']['ampliacion']}")
```

## Consejos

1. **Exporta regularmente**: Descarga el reporte JSON cada cierto tiempo como respaldo

2. **Usa filtros**: Para revisar muchas fotos, trabaja por categorías

3. **Navega con teclado**: Usa las flechas ← → para navegar rápidamente entre fotos

4. **Revisa el resumen**: Usa "Copiar Resumen" para compartir las estadísticas

## Solución de Problemas

### Las fotos no se ven

1. Verifica que las fotos estén en `images/`
2. Recarga la página con Ctrl+F5 (forzar recarga)

### Perdí mis selecciones

Las selecciones se guardan en localStorage del navegador. Si limpiaste el caché o usaste modo incógnito, las selecciones no estarán disponibles.

**Solución**: Exporta regularmente el reporte JSON como respaldo.

---

**Desarrollado para**: Boda Itzel & Javier
**Fecha de configuración**: 2025-12-19
**Total de fotos**: 541 fotos
