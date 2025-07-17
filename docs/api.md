# 🔌 API Reference

## Funciones JavaScript Disponibles

### `window.updateCatalogoFilters(filters)`

Actualiza los filtros del catálogo programáticamente.

**Parámetros:**
- `filters` (Object): Objeto con los filtros a aplicar

**Ejemplo:**
```javascript
// Filtrar por país y categoría
window.updateCatalogoFilters({
  country: 'peru',
  category: 'e-commerce'
});

// Aplicar búsqueda
window.updateCatalogoFilters({
  search: 'amazon'
});

// Combinar filtros
window.updateCatalogoFilters({
  country: 'chile',
  category: 'gastronomia',
  search: 'uber'
});
```

---

### `window.getCatalogoData()`

Obtiene los datos actuales del catálogo.

**Retorna:**
```javascript
{
  filters: {
    country: 'peru',
    category: 'e-commerce',
    search: 'amazon'
  },
  visibleCards: [...],
  totalCards: 156,
  filteredCards: 12
}
```

**Ejemplo:**
```javascript
const data = window.getCatalogoData();
console.log('Cards visibles:', data.visibleCards.length);
console.log('Total de cards:', data.totalCards);
```

---

### Callbacks de Eventos

#### `window.catalogoFilterChange`

Se ejecuta cuando cambian los filtros.

**Parámetros:**
```javascript
{
  filters: {
    country: 'peru',
    category: 'e-commerce',
    search: 'amazon'
  },
  resultsCount: 12,
  timestamp: '2024-01-15T10:30:00Z'
}
```

**Ejemplo:**
```javascript
window.catalogoFilterChange = function(data) {
  console.log('Filtros cambiados:', data.filters);
  console.log('Resultados:', data.resultsCount);
  
  // Analytics personalizado
  gtag('event', 'filter_change', {
    'country': data.filters.country,
    'category': data.filters.category,
    'results': data.resultsCount
  });
};
```

#### `window.catalogoCardClick`

Se ejecuta cuando se hace clic en una gift card.

**Parámetros:**
```javascript
{
  cardId: 'amazon-peru',
  cardName: 'Amazon',
  country: 'peru',
  category: 'e-commerce',
  description: 'Compra en Amazon Perú',
  imageUrl: '...',
  timestamp: '2024-01-15T10:30:00Z'
}
```

**Ejemplo:**
```javascript
window.catalogoCardClick = function(data) {
  console.log('Card clickeada:', data.cardName);
  
  // Track conversion intent
  gtag('event', 'gift_card_click', {
    'item_name': data.cardName,
    'item_category': data.category,
    'item_brand': data.country,
    'value': 1
  });
  
  // HubSpot contact property
  _hsq.push(['identify', {
    last_giftcard_interest: data.cardName,
    preferred_country: data.country
  }]);
};
```

#### `window.catalogoSearchChange`

Se ejecuta cuando cambia la búsqueda.

**Parámetros:**
```javascript
{
  searchTerm: 'amazon',
  resultsCount: 8,
  suggestions: ['Amazon', 'Amazon Prime'],
  timestamp: '2024-01-15T10:30:00Z'
}
```

**Ejemplo:**
```javascript
window.catalogoSearchChange = function(data) {
  console.log('Búsqueda:', data.searchTerm);
  console.log('Resultados:', data.resultsCount);
  
  // Track search behavior
  gtag('event', 'search', {
    'search_term': data.searchTerm,
    'results_count': data.resultsCount
  });
};
```

---

## CSS Variables Disponibles

### Colores
```css
:root {
  --catalogo-primary-color: #3b82f6;
  --catalogo-primary-hover: #2563eb;
  --catalogo-background: #ffffff;
  --catalogo-text-primary: #1f2937;
  --catalogo-text-secondary: #6b7280;
  --catalogo-border: #e5e7eb;
  --catalogo-shadow: rgba(0, 0, 0, 0.1);
}
```

### Tipografía
```css
:root {
  --catalogo-font-family: 'Montserrat', sans-serif;
  --catalogo-title-size: 32px;
  --catalogo-title-weight: 600;
  --catalogo-text-size: 14px;
}
```

### Espaciado
```css
:root {
  --catalogo-padding: 24px;
  --catalogo-margin: 16px;
  --catalogo-border-radius: 12px;
  --catalogo-max-height: 800px;
}
```

### Animaciones
```css
:root {
  --catalogo-animation-duration: 0.3s;
  --catalogo-animation-easing: ease-in-out;
}
```

---

## Clases CSS Disponibles

### Contenedor Principal
```css
.catalogo-giftcards {
  /* Contenedor principal del catálogo */
}

.catalogo-giftcards--loading {
  /* Estado de carga */
}

.catalogo-giftcards--error {
  /* Estado de error */
}
```

### Filtros
```css
.catalogo-filters {
  /* Contenedor de filtros */
}

.catalogo-filters__country {
  /* Selector de país */
}

.catalogo-filters__category {
  /* Selector de categoría */
}

.catalogo-filters__search {
  /* Campo de búsqueda */
}
```

### Cards
```css
.catalogo-card {
  /* Card individual */
}

.catalogo-card:hover {
  /* Estado hover */
}

.catalogo-card__image {
  /* Imagen de la card */
}

.catalogo-card__content {
  /* Contenido de la card */
}

.catalogo-card__title {
  /* Título de la card */
}

.catalogo-card__description {
  /* Descripción */
}

.catalogo-card__country {
  /* Badge del país */
}
```

---

## Eventos DOM

### `catalogoReady`

Se dispara cuando el catálogo está completamente cargado.

```javascript
document.addEventListener('catalogoReady', function(event) {
  console.log('Catálogo listo:', event.detail);
  console.log('Total de cards:', event.detail.totalCards);
});
```

### `catalogoFilterApplied`

Se dispara cuando se aplica un filtro.

```javascript
document.addEventListener('catalogoFilterApplied', function(event) {
  console.log('Filtro aplicado:', event.detail.filter);
  console.log('Resultados:', event.detail.resultsCount);
});
```

### `catalogoCardInteraction`

Se dispara en interacciones con las cards.

```javascript
document.addEventListener('catalogoCardInteraction', function(event) {
  console.log('Interacción:', event.detail.type); // 'click', 'hover', 'focus'
  console.log('Card:', event.detail.card);
});
```

---

## URL Parameters

### Parámetros Soportados

| Parámetro | Tipo | Valores | Descripción |
|-----------|------|---------|-------------|
| `country` | string | `peru`, `chile`, `colombia`, `ecuador`, `mexico`, `all` | País a filtrar |
| `category` | string | `e-commerce`, `gastronomia`, `entretenimiento`, `servicios`, `moda-y-accesorios`, `all` | Categoría a filtrar |
| `search` | string | Cualquier texto | Término de búsqueda |
| `debug` | boolean | `true`, `false` | Activa modo debug |

### Ejemplos de URLs

```
# Filtro básico
https://tudominio.com/gift-cards?country=peru

# Filtros combinados
https://tudominio.com/gift-cards?country=chile&category=gastronomia

# Con búsqueda
https://tudominio.com/gift-cards?country=peru&search=amazon

# Modo debug
https://tudominio.com/gift-cards?debug=true

# URL completa
https://tudominio.com/gift-cards?country=colombia&category=e-commerce&search=netflix&debug=false
```

---

## Configuración Avanzada

### Custom Data Sources

```javascript
// Reemplazar fuente de datos
window.catalogoCustomData = {
  baseUrl: 'https://mi-api.com/giftcards',
  endpoints: {
    peru: '/peru.json',
    chile: '/chile.json',
    // ...
  },
  transform: function(data) {
    // Transformar datos si es necesario
    return data.map(item => ({
      ...item,
      customField: 'valor'
    }));
  }
};
```

### Custom Renderers

```javascript
// Renderer personalizado para cards
window.catalogoCustomRenderer = {
  card: function(cardData) {
    return `
      <div class="mi-card-custom">
        <img src="${cardData.image}" alt="${cardData.name}" />
        <h3>${cardData.name}</h3>
        <p>${cardData.description}</p>
        <span class="custom-badge">${cardData.country}</span>
      </div>
    `;
  },
  
  filter: function(filterData) {
    // Custom filter renderer
  }
};
```

### Performance Optimization

```javascript
// Configuración de performance
window.catalogoConfig = {
  lazyLoad: true,
  virtualScrolling: false,
  debounceSearch: 300,
  cacheEnabled: true,
  preloadImages: true
};
```

---

## Troubleshooting

### Problemas Comunes

#### 1. Catálogo no se carga
```javascript
// Verificar si está listo
if (window.catalogoReady) {
  console.log('Catálogo disponible');
} else {
  console.log('Esperando catálogo...');
  document.addEventListener('catalogoReady', function() {
    console.log('Catálogo listo!');
  });
}
```

#### 2. Filtros no funcionan
```javascript
// Verificar filtros aplicados
console.log('Filtros actuales:', window.getCatalogoData().filters);

// Forzar actualización
window.updateCatalogoFilters({
  country: 'peru',
  category: 'all'
});
```

#### 3. CSS no se aplica
```javascript
// Verificar variables CSS
const style = getComputedStyle(document.documentElement);
console.log('Color primario:', style.getPropertyValue('--catalogo-primary-color'));
```

#### 4. Debug Mode
```javascript
// Activar debug
window.catalogoDebug = true;

// Ver logs detallados
localStorage.setItem('catalogo-debug', 'true');
```

---

## Versionado

### Verificar Versión
```javascript
console.log('Versión del catálogo:', window.catalogoVersion);
```

### Compatibilidad
- **v1.x**: Funcionalidades básicas
- **v2.x**: Añadido tracking y callbacks
- **v3.x**: URL parameters y SEO
- **v4.x**: Configuración avanzada HubSpot

### Migración
Ver [CHANGELOG.md](../CHANGELOG.md) para detalles de migración entre versiones.
