# 💡 Ejemplos de Uso

## Landing Page E-commerce

### Configuración
```json
{
  "titulo": "Descubre Gift Cards para E-commerce",
  "mostrar_titulo": true,
  "titulo_tag": "h1",
  "subtitulo": "Las mejores opciones para compras online",
  "mostrar_subtitulo": true,
  "pais_por_defecto": "peru",
  "categoria_por_defecto": "e-commerce",
  "color_fondo": "#f8f9fa",
  "color_titulo": "#2c3e50",
  "color_boton_primario": "#e74c3c",
  "personalizar_botones": true,
  "animacion_entrada": "fadeInUp"
}
```

### URL de Ejemplo
`https://tudominio.com/gift-cards?country=peru&category=e-commerce`

### Resultado
- Título prominente H1 para SEO
- Subtítulo descriptivo
- Filtros pre-configurados para Perú/E-commerce
- Colores de marca personalizados
- Animación suave de entrada

---

## Página Corporativa

### Configuración
```json
{
  "titulo": "Catálogo Corporativo",
  "mostrar_titulo": true,
  "titulo_tag": "h2",
  "pais_por_defecto": "all",
  "mostrar_filtros": true,
  "mostrar_busqueda": true,
  "fuente_titulo": "Roboto",
  "titulo_tamano": 36,
  "altura_maxima": 700,
  "mostrar_sombra": true,
  "activar_tracking_hubspot": true
}
```

### Características
- Todos los países disponibles
- Filtros y búsqueda habilitados
- Tipografía corporativa (Roboto)
- Tracking HubSpot para leads
- Altura ajustada para contenido

---

## Blog Post Integration

### Configuración
```json
{
  "mostrar_titulo": false,
  "altura_maxima": 500,
  "padding": 16,
  "margen_vertical": 20,
  "border_radius": 8,
  "animacion_entrada": "slideInLeft",
  "ocultar_filtros_mobile": true
}
```

### Características
- Sin título (usa el del blog post)
- Altura compacta
- Padding reducido
- Animación lateral
- Optimizado para móvil

---

## Página de Producto

### Configuración
```json
{
  "titulo": "Gift Cards Relacionadas",
  "titulo_tag": "h3",
  "pais_por_defecto": "chile",
  "categoria_por_defecto": "gastronomia",
  "mostrar_busqueda": false,
  "mostrar_filtros": false,
  "altura_maxima": 400,
  "color_fondo": "#ffffff",
  "mostrar_sombra": false
}
```

### Uso
- Como sección de productos relacionados
- Filtros ocultos (categoría fija)
- Sin búsqueda para simplicidad
- Altura compacta
- Diseño limpio sin sombras

---

## Landing Page Premium

### Configuración
```json
{
  "titulo": "Colección Premium",
  "titulo_tag": "h1",
  "fuente_titulo": "Playfair Display",
  "titulo_tamano": 48,
  "titulo_peso": "700",
  "color_titulo": "#1a202c",
  "subtitulo": "Experiencias exclusivas y únicas",
  "mostrar_subtitulo": true,
  "color_subtitulo": "#4a5568",
  "personalizar_botones": true,
  "color_boton_primario": "#d69e2e",
  "color_boton_hover": "#b7791f",
  "boton_efecto_hover": "scale(1.05)",
  "mostrar_sombra": true,
  "sombra_blur": 20,
  "animacion_entrada": "zoomIn",
  "duracion_animacion": 0.8
}
```

### Características
- Tipografía elegante (Playfair Display)
- Colores premium dorados
- Efectos hover llamativos
- Sombras pronunciadas
- Animación zoom impactante

---

## Página Responsive Mobile-First

### Configuración
```json
{
  "titulo": "Gift Cards Móvil",
  "titulo_tamano": 32,
  "titulo_tamano_mobile": 24,
  "padding": 20,
  "padding_mobile": 12,
  "altura_maxima": 600,
  "ocultar_filtros_mobile": true,
  "mostrar_busqueda": true,
  "animacion_entrada": "fadeInUp",
  "duracion_animacion": 0.4
}
```

### Características
- Tamaños optimizados para móvil
- Filtros ocultos en mobile
- Búsqueda mantenida
- Animación rápida
- Padding ajustado por dispositivo

---

## Dashboard Interno

### Configuración
```json
{
  "titulo": "Dashboard Gift Cards",
  "mostrar_titulo": true,
  "titulo_tag": "h2",
  "debug_mode": true,
  "activar_tracking": false,
  "activar_tracking_hubspot": false,
  "mostrar_texto_pie": true,
  "texto_pie": "<p>Dashboard interno - Datos actualizados en tiempo real</p>",
  "color_fondo": "#f7fafc",
  "border_radius": 0,
  "mostrar_sombra": false
}
```

### Características
- Modo debug habilitado
- Sin tracking externo
- Texto informativo en pie
- Diseño dashboard (sin bordes redondeados)
- Información de estado

---

## E-commerce Marketplace

### Configuración
```json
{
  "titulo": "Marketplace Gift Cards",
  "subtitulo": "Encuentra la gift card perfecta para cada ocasión",
  "mostrar_subtitulo": true,
  "pais_por_defecto": "all",
  "mostrar_filtros": true,
  "mostrar_busqueda": true,
  "personalizar_botones": true,
  "color_boton_primario": "#38a169",
  "color_boton_hover": "#2f855a",
  "activar_tracking": true,
  "activar_lead_tracking": true,
  "callback_card_click": "trackPurchaseIntent"
}
```

### JavaScript Personalizado
```html
<script>
function trackPurchaseIntent(data) {
  // Track purchase intent
  gtag('event', 'purchase_intent', {
    'item_name': data.cardName,
    'item_category': data.category,
    'value': 1
  });
  
  // HubSpot lead scoring
  _hsq.push(['identify', {
    giftcard_interest: data.cardName,
    last_interaction: new Date().toISOString()
  }]);
}
</script>
```

---

## Configuraciones por Industria

### Retail/Moda
```json
{
  "color_boton_primario": "#e53e3e",
  "fuente_titulo": "Poppins",
  "animacion_entrada": "slideInLeft",
  "categoria_por_defecto": "moda-y-accesorios"
}
```

### Gastronomía
```json
{
  "color_boton_primario": "#dd6b20",
  "fuente_titulo": "Lora",
  "animacion_entrada": "fadeInUp",
  "categoria_por_defecto": "gastronomia"
}
```

### Tecnología
```json
{
  "color_boton_primario": "#3182ce",
  "fuente_titulo": "Inter",
  "animacion_entrada": "zoomIn",
  "categoria_por_defecto": "e-commerce"
}
```

### Servicios
```json
{
  "color_boton_primario": "#805ad5",
  "fuente_titulo": "Source Sans Pro",
  "animacion_entrada": "fadeInUp",
  "categoria_por_defecto": "servicios"
}
```

---

## Testing y Debugging

### Configuración de Test
```json
{
  "debug_mode": true,
  "activar_tracking": false,
  "titulo": "TEST - Catálogo Gift Cards",
  "mostrar_texto_pie": true,
  "texto_pie": "<p style='color: red;'>⚠️ MODO TEST - NO USAR EN PRODUCCIÓN</p>"
}
```

### Callbacks de Debug
```javascript
window.catalogoFilterChange = function(data) {
  console.log('🔍 Filtro cambiado:', data);
  console.table(data);
};

window.catalogoCardClick = function(data) {
  console.log('🎯 Tarjeta clickeada:', data);
  alert('Debug: ' + data.cardName);
};
```

---

## URLs de Ejemplo

### Filtros Específicos
- **Perú E-commerce**: `?country=peru&category=e-commerce`
- **Chile Gastronomía**: `?country=chile&category=gastronomia`
- **Colombia Servicios**: `?country=colombia&category=servicios`

### Búsquedas
- **Amazon**: `?search=amazon`
- **Uber**: `?search=uber`
- **Netflix**: `?search=netflix`

### Combinaciones
- **Perú + Amazon**: `?country=peru&category=e-commerce&search=amazon`
- **Chile + Gastronomía + Uber**: `?country=chile&category=gastronomia&search=uber`

---

## Mejores Prácticas

### Performance
- Usar alturas máximas razonables (< 1000px)
- Evitar animaciones muy largas (< 1s)
- Optimizar para móvil primero

### UX/UI
- Mantener buen contraste de colores
- Usar fuentes legibles
- Probar en múltiples dispositivos

### SEO
- Usar etiquetas H1 apropiadas
- Incluir subtítulos descriptivos
- Optimizar para palabras clave

### Analytics
- Configurar tracking apropiado
- Usar callbacks para eventos custom
- Monitorear conversiones
