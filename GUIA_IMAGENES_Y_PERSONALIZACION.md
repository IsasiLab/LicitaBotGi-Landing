# 🖼️ Guía: Añadir Imágenes y Personalización Avanzada

## 📋 Contenido

1. [Cómo Añadir Imágenes Reales](#cómo-añadir-imágenes-reales)
2. [Servicios de Imágenes Gratuitas](#servicios-de-imágenes-gratuitas)
3. [Optimización de Imágenes](#optimización-de-imágenes)
4. [Personalizar el Menú de Navegación](#personalizar-el-menú-de-navegación)
5. [Añadir Logo Profesional](#añadir-logo-profesional)
6. [Integración con WordPress](#integración-con-wordpress)

---

## 🖼️ 1. CÓMO AÑADIR IMÁGENES REALES

### En la Card de LicitaBotGi

**Ubicación**: Busca el comentario `<!-- Software de Licitaciones con IA -->`

**Reemplaza este bloque**:
```html
<div class="image-placeholder" style="background: rgba(255,255,255,0.1); margin-bottom: 30px;">
    <div style="text-align: center;">
        <div style="font-size: 5em; margin-bottom: 10px;">🚀</div>
        <div style="font-size: 1.2em; opacity: 0.9;">Software de Licitaciones con IA</div>
    </div>
</div>
```

**Por esto**:
```html
<img src="URL_DE_TU_IMAGEN" 
     alt="LicitaBotGi - Software de Licitaciones" 
     style="width: 100%; max-width: 500px; height: auto; border-radius: 15px; margin: 0 auto 30px; display: block; box-shadow: 0 10px 40px rgba(255,255,255,0.2);">
```

---

### En las Cards de Placeholder (Futuros Software)

**Ubicación**: Busca `<!-- Para añadir imagen real -->`

**Reemplaza**:
```html
<div class="image-placeholder" style="border: 3px dashed #ddd;">
    📦
</div>
```

**Por**:
```html
<img src="URL_DE_TU_IMAGEN" 
     alt="Descripción del software" 
     class="featured-image" 
     style="width: 100%; height: 200px; object-fit: cover; border-radius: 15px; margin-bottom: 20px;">
```

---

### En la Sección de Diseño 3D (opcional)

Si quieres añadir ejemplos visuales de tus trabajos 3D, **después de cada** `<div class="design-item">`, añade:

```html
<div class="design-item">
    <!-- AÑADIR IMAGEN ANTES DEL ICONO -->
    <img src="URL_DE_TU_TRABAJO_3D" 
         alt="Ejemplo de [Servicio]" 
         style="width: 100%; height: 180px; object-fit: cover; border-radius: 10px; margin-bottom: 15px;">
    
    <div class="design-item-icon">🖼️</div>
    <h3>Litofanías</h3>
    <p>Transforma tus fotos en relieves 3D iluminados</p>
</div>
```

---

## 📸 2. SERVICIOS DE IMÁGENES GRATUITAS

### Opción 1: Unsplash (Recomendado)

**URL**: https://unsplash.com

**Categorías sugeridas**:
- **Software/Tech**: busca "dashboard", "software interface", "data visualization"
- **3D Design**: busca "3d printing", "3d model", "design"
- **Cloud**: busca "cloud computing", "servers", "data center"

**Cómo usar**:
1. Busca la imagen que necesitas
2. Haz clic en "Download Free"
3. Sube la imagen a tu WordPress (Medios → Añadir nuevo)
4. Copia la URL de la imagen subida
5. Pega en el atributo `src="URL_AQUI"`

---

### Opción 2: Pexels

**URL**: https://www.pexels.com

Similar a Unsplash, búsquedas recomendadas:
- "business software"
- "3d printing technology"
- "cloud technology"

---

### Opción 3: Tus Propias Capturas

**Para LicitaBotGi**:
1. Abre el software
2. Captura la pantalla principal (Windows + Shift + S)
3. Edita en Paint/Photoshop para recortar y mejorar
4. Guarda como JPG (calidad 80-90%)
5. Sube a WordPress

**Para Diseño 3D**:
1. Fotografía tus mejores trabajos con buena iluminación
2. Fondo neutro (blanco o gris)
3. Edita para mejorar colores
4. Recorta al tamaño adecuado (recomendado: 800x600px)

---

## ⚡ 3. OPTIMIZACIÓN DE IMÁGENES

### Tamaños Recomendados

| Ubicación | Ancho | Alto | Formato |
|-----------|-------|------|---------|
| Hero section | 1920px | 1080px | JPG |
| Card destacada (LicitaBotGi) | 800px | 500px | JPG/PNG |
| Cards normales | 600px | 400px | JPG |
| Servicios 3D | 500px | 500px | JPG |
| Logo | 200px | 200px | PNG (transparente) |

---

### Herramientas de Optimización

**Online (Gratis)**:
- **TinyPNG**: https://tinypng.com (reduce tamaño 60-80%)
- **Squoosh**: https://squoosh.app (control total de calidad)
- **JPEG Optimizer**: https://jpeg-optimizer.com

**Proceso recomendado**:
1. Redimensiona a tamaño correcto
2. Pasa por TinyPNG para comprimir
3. Sube a WordPress
4. Verifica que se carga rápido (< 200KB por imagen)

---

## 🧭 4. PERSONALIZAR EL MENÚ DE NAVEGACIÓN

### Cambiar Elementos del Menú

**Ubicación**: Busca `<ul class="nav-menu">`

**Estructura actual**:
```html
<ul class="nav-menu" id="navMenu">
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#software">Software</a></li>
    <li><a href="#diseno3d">Diseño 3D</a></li>
    <li><a href="#cloud">Cloud M365</a></li>
    <li><a href="#contacto" class="nav-cta">Contacto</a></li>
</ul>
```

---

### Añadir Más Páginas

Si tienes otras páginas en WordPress (ej. Blog, Portfolio), añade:

```html
<ul class="nav-menu" id="navMenu">
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#software">Software</a></li>
    <li><a href="#diseno3d">Diseño 3D</a></li>
    <li><a href="#cloud">Cloud M365</a></li>
    <li><a href="/blog">Blog</a></li>  <!-- NUEVO -->
    <li><a href="/portfolio">Portfolio</a></li>  <!-- NUEVO -->
    <li><a href="#contacto" class="nav-cta">Contacto</a></li>
</ul>
```

---

### Cambiar Color del Menú

**Ubicación**: Busca `.nav-cta` en los estilos CSS

**Color actual** (morado):
```css
.nav-menu .nav-cta {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

**Para cambiar a verde**:
```css
.nav-menu .nav-cta {
    background: linear-gradient(135deg, #10b981 0%, #059669 100%);
}
```

---

## 🎨 5. AÑADIR LOGO PROFESIONAL

### Crear un Logo Simple

Si no tienes logo, puedes usar **Canva** gratis:
1. Ve a https://www.canva.com
2. Busca "Logo" en plantillas
3. Personaliza con "IsasiLab"
4. Descarga como PNG (transparente)
5. Optimiza con TinyPNG

---

### Reemplazar el Emoji con Logo

**Ubicación**: Busca `<a href="#inicio" class="nav-logo">`

**Actual**:
```html
<a href="#inicio" class="nav-logo">
    <span>🚀</span>
    <span>IsasiLab</span>
</a>
```

**Con logo**:
```html
<a href="#inicio" class="nav-logo">
    <img src="URL_DE_TU_LOGO" 
         alt="IsasiLab Logo" 
         style="height: 40px; width: auto; margin-right: 10px;">
    <span>IsasiLab</span>
</a>
```

---

### Logo Solo (Sin Texto)

```html
<a href="#inicio" class="nav-logo">
    <img src="URL_DE_TU_LOGO" 
         alt="IsasiLab" 
         style="height: 50px; width: auto;">
</a>
```

---

## 🔧 6. INTEGRACIÓN CON WORDPRESS

### Método 1: Página Completa (Recomendado)

Sigue las instrucciones de `INSTRUCCIONES_WORDPRESS_WEB_COMPLETA.md`:

1. Páginas → Añadir nueva
2. Modo "Código/Texto"
3. Pega TODO el HTML
4. Configura como página de inicio

**Ventaja**: Control total del diseño.

---

### Método 2: Usar con Elementor

Si usas **Elementor** en WordPress:

1. Crea nueva página con Elementor
2. Añade widget "HTML"
3. Pega el código completo
4. Ajusta márgenes/padding si es necesario

**Ventaja**: Puedes editar visualmente después.

---

### Método 3: Theme File (Avanzado)

Si tienes acceso FTP:

1. Conecta por FTP a tu hosting
2. Ve a `/wp-content/themes/[tu-tema]/`
3. Crea archivo `template-isasilab.php`
4. Añade al inicio:
```php
<?php
/*
Template Name: IsasiLab Home
*/
?>
```
5. Pega el HTML completo después
6. Guarda el archivo
7. En WordPress, selecciona este template para la página de inicio

---

## 📱 7. VERIFICAR RESPONSIVE

Después de añadir imágenes, verifica en diferentes dispositivos:

### Desktop (>1200px)
- ✅ Menú horizontal visible
- ✅ Imágenes no pixeladas
- ✅ Cards en grid de 3 columnas

### Tablet (768px - 1024px)
- ✅ Menú puede necesitar ajuste
- ✅ Cards en grid de 2 columnas
- ✅ Imágenes se redimensionan correctamente

### Móvil (<768px)
- ✅ Menú hamburguesa funciona
- ✅ Cards apiladas verticalmente
- ✅ Imágenes 100% ancho (no overflow)
- ✅ Texto legible (no muy pequeño)

### Cómo Probar

**Opción 1: Chrome DevTools**
1. F12 para abrir DevTools
2. Ctrl + Shift + M (modo responsive)
3. Prueba diferentes tamaños

**Opción 2: Dispositivos Reales**
- Prueba en tu móvil visitando la URL
- Verifica que se ve bien
- Prueba que todos los enlaces funcionan

---

## 🎯 CHECKLIST FINAL CON IMÁGENES

- [ ] Logo añadido en el menú
- [ ] Imagen de LicitaBotGi añadida
- [ ] Imágenes de placeholders añadidas (si aplica)
- [ ] Imágenes de trabajos 3D añadidas (opcional)
- [ ] Todas las imágenes optimizadas (< 200KB)
- [ ] Todas las imágenes tienen atributo `alt` descriptivo
- [ ] Menú de navegación funciona en móvil
- [ ] Enlaces del menú llevan a las secciones correctas
- [ ] Web carga rápido (< 3 segundos)
- [ ] Responsive verificado en desktop, tablet, móvil
- [ ] Colores del menú personalizados (si aplica)
- [ ] Items del menú actualizados según necesidad

---

## 💡 TIPS PROFESIONALES

### Para Fotografía de Productos 3D

1. **Iluminación**: Luz natural o softbox
2. **Fondo**: Blanco puro o gris neutro
3. **Ángulo**: 45 grados frontal
4. **Múltiples fotos**: 3-5 ángulos diferentes
5. **Edición**: Aumenta contraste ligeramente

---

### Para Capturas de Software

1. **Resolución**: Pantalla completa (1920x1080)
2. **Limpia**: Sin notificaciones ni distracciones
3. **Datos reales**: Usa ejemplos realistas (no "Lorem ipsum")
4. **Blur sensible**: Difumina datos confidenciales
5. **Anotaciones**: Opcional - flechas destacando features

---

### Para Logos

1. **Simple es mejor**: Máximo 2 colores
2. **Legible**: Tipografía clara
3. **Escalable**: Se debe ver bien pequeño (40px) y grande
4. **Formato**: PNG con transparencia
5. **Versiones**: Ten versión oscura y clara si usas fondos variables

---

## 🆘 PROBLEMAS COMUNES

### Las imágenes no se cargan

**Causa**: URL incorrecta o imagen no existe

**Solución**:
1. Verifica la URL en el navegador (copia/pega)
2. Asegúrate de que la imagen esté subida
3. Verifica permisos de la carpeta (hosting)

---

### Las imágenes son muy pesadas (lentitud)

**Causa**: Imágenes sin optimizar (> 500KB cada una)

**Solución**:
1. Pasa por TinyPNG todas las imágenes
2. Redimensiona al tamaño exacto necesario
3. Usa JPG para fotos, PNG solo para logos con transparencia

---

### El menú móvil no funciona

**Causa**: JavaScript no se ejecuta

**Solución**:
1. Verifica que el script está al final del HTML (antes de `</body>`)
2. Abre consola del navegador (F12) y busca errores
3. Si usas WordPress, puede haber conflicto con otros plugins

**Fix alternativo**: Desactiva temporalmente otros plugins de JavaScript

---

### Las imágenes se ven pixeladas

**Causa**: Resolución muy baja

**Solución**:
1. Usa imágenes al menos 2x el tamaño mostrado
2. Para una card de 600px, usa imagen de 1200px
3. Comprime después de redimensionar

---

## 📞 SIGUIENTE PASO

Una vez añadidas las imágenes:

1. **Sube a WordPress** siguiendo `INSTRUCCIONES_WORDPRESS_WEB_COMPLETA.md`
2. **Verifica responsive** en múltiples dispositivos
3. **Optimiza SEO** (Yoast plugin)
4. **Test de velocidad** con https://pagespeed.web.dev
5. **Comparte** con amigos para feedback

---

**Actualización**: Febrero 2026  
**Versión**: 1.0  
**Archivos relacionados**: 
- `isasilab3d_nueva_web_completa.html`
- `INSTRUCCIONES_WORDPRESS_WEB_COMPLETA.md`
- `MANTENIMIENTO_WEBSITE.md`
