# ⚙️ Guía de Configuración

## Grupos de Configuración

### 📋 Configuración General

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `titulo` | text | Título principal del catálogo | "Catálogo de Gift Cards" |
| `mostrar_titulo` | boolean | Mostrar/ocultar título | `true` |
| `titulo_tag` | choice | Etiqueta HTML (H1-H4) | `h2` |
| `subtitulo` | text | Texto del subtítulo | `""` |
| `mostrar_subtitulo` | boolean | Mostrar/ocultar subtítulo | `false` |

**Ejemplo:**
```html
Título: "Encuentra tu Gift Card Perfecta"
Tag: H1
Subtítulo: "Más de 100 opciones disponibles"
```

### ⚙️ Configuración Funcional

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `pais_por_defecto` | choice | País inicial | `all` |
| `categoria_por_defecto` | choice | Categoría inicial | `all` |
| `mostrar_busqueda` | boolean | Barra de búsqueda | `true` |
| `mostrar_filtros` | boolean | Filtros de país/categoría | `true` |

**Opciones de País:**
- `all` - Todos los países
- `chile` - Chile
- `peru` - Perú
- `colombia` - Colombia
- `mexico` - México
- `ecuador` - Ecuador

**Opciones de Categoría:**
- `all` - Todas las categorías
- `e-commerce` - E-commerce
- `gastronomia` - Gastronomía
- `supermercados-y-minimarket` - Supermercados
- `grandes-tiendas` - Grandes Tiendas
- `servicios` - Servicios

### 🎨 Estilos Generales

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `ancho_maximo` | number | Ancho máximo en px | `1200` |
| `altura_minima` | number | Altura mínima en px | `400` |
| `altura_maxima` | number | Altura máxima en px | `800` |
| `padding` | number | Padding interno en px | `24` |
| `margen_vertical` | number | Margen vertical en px | `32` |

### 🌈 Colores

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `color_fondo` | color | Fondo principal | `#ffffff` |
| `color_fondo_catalogo` | color | Fondo del catálogo | `#fafafa` |
| `color_titulo` | color | Color del título | `#1a1a1a` |
| `color_subtitulo` | color | Color del subtítulo | `#666666` |

**Ejemplo de Configuración de Marca:**
```css
Fondo principal: #f8f9fa
Fondo catálogo: #ffffff
Título: #2c3e50
Subtítulo: #7f8c8d
```

### 📝 Tipografía

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `fuente_titulo` | font | Fuente Google Fonts | `Montserrat` |
| `titulo_tamano` | number | Tamaño en px | `40` |
| `titulo_peso` | choice | Peso de fuente | `700` |
| `titulo_alineacion` | choice | Alineación | `center` |
| `titulo_margen_inferior` | number | Margen inferior en px | `24` |

**Opciones de Peso:**
- `300` - Light
- `400` - Normal
- `500` - Medium
- `600` - SemiBold
- `700` - Bold
- `800` - ExtraBold

**Opciones de Alineación:**
- `left` - Izquierda
- `center` - Centro
- `right` - Derecha

### 🔘 Personalización de Botones

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `personalizar_botones` | boolean | Habilitar personalización | `false` |
| `color_boton_primario` | color | Color principal | `#8b5cf6` |
| `color_boton_hover` | color | Color al pasar mouse | `#7c3aed` |
| `color_texto_boton` | color | Color del texto | `#ffffff` |
| `boton_efecto_hover` | choice | Efecto hover | `translateY(-2px)` |

**Efectos Hover Disponibles:**
- `none` - Sin efecto
- `scale(1.05)` - Agrandar 5%
- `translateY(-2px)` - Elevar 2px
- `scale(0.95)` - Reducir 5%

### 🎭 Bordes y Sombras

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `border_radius` | number | Radio del borde en px | `12` |
| `mostrar_borde` | boolean | Mostrar borde | `false` |
| `borde_ancho` | number | Grosor del borde en px | `1` |
| `color_borde` | color | Color del borde | `#e5e7eb` |
| `mostrar_sombra` | boolean | Mostrar sombra | `true` |
| `sombra_offset_y` | number | Desplazamiento Y en px | `4` |
| `sombra_blur` | number | Difuminado en px | `15` |
| `color_sombra` | color | Color de la sombra | `rgba(0,0,0,0.1)` |

### ✨ Animaciones

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `activar_animaciones` | boolean | Habilitar animaciones | `true` |
| `animacion_entrada` | choice | Tipo de animación | `fadeInUp` |
| `duracion_animacion` | number | Duración en segundos | `0.6` |

**Animaciones Disponibles:**
- `fadeInUp` - Aparece desde abajo
- `slideInLeft` - Desliza desde izquierda
- `zoomIn` - Aparece con zoom
- `none` - Sin animación

### �� Responsive

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `padding_mobile` | number | Padding móvil en px | `16` |
| `titulo_tamano_mobile` | number | Tamaño título móvil en px | `28` |
| `ocultar_filtros_mobile` | boolean | Ocultar filtros en móvil | `false` |

### 📊 Tracking y Analytics

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `activar_tracking` | boolean | Google Analytics | `true` |
| `activar_tracking_hubspot` | boolean | HubSpot tracking | `true` |
| `activar_lead_tracking` | boolean | Lead scoring | `false` |

### 📄 Contenido Adicional

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `mostrar_texto_pie` | boolean | Mostrar pie de página | `false` |
| `texto_pie` | richtext | Contenido del pie | `"¿Necesitas ayuda? <a href='/contacto'>Contáctanos</a>"` |

### ⚡ Configuración Avanzada

| Campo | Tipo | Descripción | Valor por Defecto |
|-------|------|-------------|-------------------|
| `debug_mode` | boolean | Modo debug | `false` |
| `callback_filtro_cambio` | text | Función JS filtro | `""` |
| `callback_card_click` | text | Función JS click tarjeta | `""` |

**Ejemplo de Callbacks:**
```javascript
// Callback filtro cambio
window.catalogoFilterChange = function(data) {
  console.log('Filtro:', data.country, data.category);
  // Tu código personalizado
};

// Callback click tarjeta
window.catalogoCardClick = function(data) {
  console.log('Tarjeta:', data.cardName);
  // Tu código personalizado
};
```

## Casos de Uso Comunes

### Landing Page E-commerce
```yaml
Configuración recomendada:
- pais_por_defecto: "peru"
- categoria_por_defecto: "e-commerce"
- color_boton_primario: "#8b5cf6"
- animacion_entrada: "fadeInUp"
- personalizar_botones: true
```

### Página Corporativa
```yaml
Configuración recomendada:
- mostrar_filtros: true
- fuente_titulo: "Roboto"
- altura_maxima: 600
- mostrar_sombra: true
- activar_tracking_hubspot: true
```

### Blog Post
```yaml
Configuración recomendada:
- mostrar_titulo: false
- altura_maxima: 500
- padding: 16
- responsive optimizado
```

## Validación de Configuración

### Campos Requeridos
- Ningún campo es obligatorio
- Todos tienen valores por defecto
- Validación automática de tipos

### Límites y Restricciones
- Números: min 0, max 9999
- Colores: formato hexadecimal válido
- Fuentes: solo Google Fonts disponibles
- Texto: máximo 500 caracteres

### Mejores Prácticas
- Usar colores con buen contraste
- Mantener tamaños de fuente legibles
- Probar en móvil y desktop
- Validar callbacks JavaScript
- Usar animaciones sutiles
