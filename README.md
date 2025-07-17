# 🧩 HubSpot Catálogo Gift Cards Module

Un módulo personalizado de HubSpot para mostrar un catálogo interactivo de gift cards con control total desde el editor visual del CMS.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![HubSpot](https://img.shields.io/badge/HubSpot-Module-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Características

### 🎨 **Personalización Visual Completa**
- **Colores**: Control total de fondos, títulos, botones desde el CMS
- **Tipografía**: Fuentes Google Fonts, tamaños, pesos, alineación
- **Espaciado**: Padding, márgenes, alturas personalizables
- **Bordes y Sombras**: Radio, grosor, colores, efectos
- **Animaciones**: Entrada configurables (Fade, Slide, Zoom)

### ⚙️ **Funcionalidad Avanzada**
- **Filtros**: País y categoría por defecto
- **URL Parameters**: Compatibilidad con `?country=peru&category=ecommerce`
- **Responsive**: Configuración específica para móvil
- **Búsqueda**: Barra de búsqueda opcional
- **Contenido**: Títulos, subtítulos, texto del pie editable

### 📊 **Tracking y Analytics**
- **Google Analytics**: Eventos automáticos
- **HubSpot**: Lead tracking y scoring integrado
- **Callbacks**: Funciones JavaScript personalizadas
- **Debug Mode**: Para desarrollo y testing

## 🚀 Instalación Rápida

### **Opción 1: Desde GitHub (Recomendado)**
1. **HubSpot Design Manager** → `Create` → `Module`
2. **Conectar con GitHub** → Seleccionar este repositorio
3. **Auto-sync** habilitado para actualizaciones automáticas

### **Opción 2: Copia Manual**
1. **HubSpot Design Manager** → `Create` → `Module`
2. **Copiar archivos**:
   - `module.html` → Template
   - `module.css` → CSS
   - `module.js` → JavaScript
   - `fields.json` → Fields

## 📁 Estructura del Proyecto

```
hubspot-catalogo-giftcards-module/
├── module.html           # Template principal HubL
├── module.css            # Estilos personalizables
├── module.js             # JavaScript con configuraciones
├── fields.json           # Configuración del editor (80+ opciones)
├── meta.json             # Metadatos del módulo
├── README.md             # Documentación
├── CHANGELOG.md          # Historial de cambios
├── LICENSE               # Licencia MIT
└── docs/                 # Documentación adicional
    ├── installation.md   # Guía de instalación
    ├── configuration.md  # Guía de configuración
    └── examples.md       # Ejemplos de uso
```

## 🎛️ Configuración desde HubSpot

El módulo incluye **10 grupos de configuración** con más de **80 opciones**:

### 📋 **Configuración General**
- Título y subtítulo personalizables
- Etiquetas HTML (H1, H2, H3, H4)
- Mostrar/ocultar elementos

### ⚙️ **Configuración Funcional**
- País por defecto (Chile, Perú, Colombia, México, Ecuador)
- Categoría por defecto (E-commerce, Gastronomía, etc.)
- Activar/desactivar búsqueda y filtros

### 🎨 **Estilos Visuales**
- Dimensiones (ancho, alto, padding, márgenes)
- Colores (fondos, títulos, botones)
- Tipografía (Google Fonts, tamaños, pesos)

### 🔘 **Botones Personalizables**
- Colores primario, hover, texto
- Efectos hover (agrandar, elevar, reducir)

### 🎭 **Bordes y Sombras**
- Radio de bordes personalizables
- Sombras configurables (offset, blur, color)

### ✨ **Animaciones**
- Fade In Up, Slide In Left, Zoom In
- Duración personalizable

### 📱 **Responsive**
- Configuración específica móvil
- Breakpoints personalizables

### 📊 **Tracking**
- Google Analytics integrado
- HubSpot lead tracking
- Callbacks JavaScript personalizados

## 💡 Ejemplos de Uso

### **Landing Page E-commerce**
```html
Configuración sugerida:
- País: "peru"
- Categoría: "e-commerce" 
- Color primario: #8b5cf6
- Animación: "fadeInUp"
```

### **Página Corporativa**
```html
Configuración sugerida:
- País: "all"
- Mostrar filtros: true
- Fuente: "Roboto"
- Altura: 600px
```

## 🔗 URLs de Ejemplo

- **Básica**: `https://tudominio.com/catalogo`
- **Con filtros**: `https://tudominio.com/catalogo?country=peru&category=ecommerce`
- **Búsqueda**: `https://tudominio.com/catalogo?search=amazon`

## 🛠️ Desarrollo

### **Dependencias Externas**
El módulo carga automáticamente:
- **CSS**: `https://estudios.apprecio.com/hubfs/catalogo-gift-cards/css/`
- **JavaScript**: `https://estudios.apprecio.com/hubfs/catalogo-gift-cards/js/`

### **Personalización Avanzada**
```javascript
// Callbacks disponibles
window.catalogoFilterChange = function(data) {
  console.log('Filtro cambiado:', data);
};

window.catalogoCardClick = function(data) {
  console.log('Tarjeta clickeada:', data);
};
```

## 📈 Versionado

Usamos [SemVer](http://semver.org/) para el versionado. Para las versiones disponibles, ve las [tags en este repositorio](../../tags).

## 🤝 Contribuir

1. **Fork** el proyecto
2. **Crear branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit** los cambios (`git commit -m 'Add some AmazingFeature'`)
4. **Push** al branch (`git push origin feature/AmazingFeature`)
5. **Crear Pull Request**

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ve el archivo [LICENSE](LICENSE) para detalles.

## 📞 Soporte

- **Documentación**: [docs/](docs/)
- **Issues**: [GitHub Issues](../../issues)
- **Contacto**: crear issue para soporte técnico

## 🏆 Changelog

Ver [CHANGELOG.md](CHANGELOG.md) para historial de cambios.

---

**Desarrollado con ❤️ para HubSpot CMS Hub**
