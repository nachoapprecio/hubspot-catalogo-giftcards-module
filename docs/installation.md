# 📦 Guía de Instalación

## Opción 1: Instalación desde GitHub (Recomendado)

### Prerrequisitos
- Cuenta HubSpot con acceso a Design Manager
- Permisos de developer en HubSpot
- Conexión GitHub configurada en HubSpot

### Pasos

1. **Conectar GitHub a HubSpot**
   - Ve a `Settings > Integrations > Connected Apps`
   - Conecta tu cuenta de GitHub
   - Autoriza acceso a repositorios

2. **Crear Módulo desde GitHub**
   - Ve a `Marketing > Files and Templates > Design Manager`
   - Click `Create` → `Module`
   - Selecciona `From GitHub repository`
   - Repository: `nachoapprecio/hubspot-catalogo-giftcards-module`
   - Branch: `main`
   - Nombre: `Catálogo Gift Cards`

3. **Configurar Auto-sync**
   - Habilita `Auto-sync` para actualizaciones automáticas
   - Selecciona `main` branch para production
   - Guarda configuración

4. **Verificar Instalación**
   - El módulo aparecerá en Design Manager
   - Todos los archivos se importarán automáticamente
   - Estará disponible en el editor de páginas

## Opción 2: Instalación Manual

### Pasos

1. **Descargar Archivos**
   ```bash
   git clone https://github.com/nachoapprecio/hubspot-catalogo-giftcards-module.git
   cd hubspot-catalogo-giftcards-module
   ```

2. **Crear Módulo en HubSpot**
   - Ve a `Marketing > Files and Templates > Design Manager`
   - Click `Create` → `Module`
   - Nombre: `Catálogo Gift Cards`

3. **Copiar Archivos**

   **Template (module.html):**
   ```html
   <!-- Copiar contenido completo de module.html -->
   ```

   **CSS (module.css):**
   ```css
   /* Copiar contenido completo de module.css */
   ```

   **JavaScript (module.js):**
   ```javascript
   // Copiar contenido completo de module.js
   ```

   **Fields (fields.json):**
   ```json
   // Copiar contenido completo de fields.json
   ```

4. **Publicar Módulo**
   - Guardar todos los archivos
   - Click `Publish`
   - Verificar que no hay errores

## Verificación Post-Instalación

### Checklist

- [ ] ✅ Módulo aparece en Design Manager
- [ ] ✅ No hay errores de sintaxis
- [ ] ✅ Archivos CSS y JS cargan correctamente
- [ ] ✅ Configuraciones aparecen en el editor
- [ ] ✅ Módulo está disponible para arrastrar y soltar

### Prueba Rápida

1. **Crear página de prueba**
   - Ve a `Marketing > Website > Website Pages`
   - Crear nueva página
   - Usar editor drag & drop

2. **Agregar módulo**
   - Buscar "Catálogo Gift Cards" en módulos
   - Arrastrar al área de contenido
   - Verificar que se renderiza correctamente

3. **Probar configuraciones**
   - Cambiar título
   - Modificar país por defecto
   - Ajustar colores
   - Verificar preview

## Solución de Problemas

### Error: "Módulo no encontrado"
- Verificar que el módulo está publicado
- Limpiar cache del navegador
- Verificar permisos de usuario

### Error: "CSS no carga"
- Verificar URLs de assets externos
- Comprobar conectividad con estudios.apprecio.com
- Revisar configuración de CORS

### Error: "JavaScript no funciona"
- Verificar que no hay errores en consola
- Comprobar sintaxis HubL
- Verificar callbacks personalizados

### Error: "Configuraciones no aparecen"
- Revisar sintaxis de fields.json
- Verificar que todos los campos tienen ID único
- Comprobar estructura de grupos

## Actualizaciones

### GitHub Auto-sync
Si usaste la instalación desde GitHub:
- Las actualizaciones se aplicarán automáticamente
- Recibirás notificaciones de cambios
- Puedes revertir a versiones anteriores

### Manual
Si instalaste manualmente:
1. Descargar nueva versión
2. Reemplazar archivos en Design Manager
3. Publicar cambios
4. Probar funcionalidad

## Soporte

- **Issues**: [GitHub Issues](https://github.com/nachoapprecio/hubspot-catalogo-giftcards-module/issues)
- **Documentación**: [docs/](../README.md)
- **Ejemplos**: [examples.md](examples.md)
