# 🌐 Instrucciones: Implementar Nueva Web Completa en WordPress

## 📋 Resumen

Este documento te guía paso a paso para **reemplazar completamente tu sitio www.isasilab3d.com** con el nuevo diseño que incluye:
- ✅ Sección destacada de Software Empresarial (LicitaBotGi + placeholders)
- ✅ Diseño 3D Profesional (6 servicios en grid)
- ✅ Arquitectura Cloud M365
- ✅ Footer con 4 columnas
- ✅ Diseño moderno con gradientes
- ✅ 100% responsive (móvil, tablet, desktop)

**Archivo a usar**: `isasilab3d_nueva_web_completa.html`

---

## ⏱️ Tiempo estimado: 20-30 minutos

---

## 🔧 OPCIÓN 1: Reemplazar Página Principal (RECOMENDADO)

### Paso 1: Hacer Backup (5 min)

**IMPORTANTE**: Antes de hacer cambios, guarda una copia de seguridad.

1. Accede al panel de WordPress: `www.isasilab3d.com/wp-admin`
2. En el menú lateral izquierdo, ve a **"Herramientas"** → **"Exportar"**
3. Selecciona **"Todo el contenido"**
4. Haz clic en **"Descargar archivo de exportación"**
5. Guarda el archivo `.xml` en tu PC (es tu copia de seguridad)

---

### Paso 2: Crear Nueva Página Principal (10 min)

#### 2.1. Crear nueva página

1. En WordPress, ve a **"Páginas"** → **"Añadir nueva"**
2. En el título, escribe: `Home IsasiLab Nuevo`
3. Busca el botón en la esquina superior derecha que dice **"Editar como HTML"** o **cambiar a editor de texto**
   - Si usas Gutenberg (bloques), haz clic en los **tres puntos `⋮`** → **"Editor de código"**
   - Si usas editor clásico, ve a la pestaña **"Texto"** (no "Visual")

#### 2.2. Pegar el código HTML

1. **Abre el archivo** `isasilab3d_nueva_web_completa.html` en un editor de texto (Bloc de notas)
2. **Selecciona TODO** el contenido (Ctrl+A)
3. **Copia** (Ctrl+C)
4. Vuelve a WordPress y **pega** (Ctrl+V) en el editor de código/texto
5. Haz clic en **"Publicar"** (botón azul arriba a la derecha)

#### 2.3. Verificar la página

1. Después de publicar, haz clic en **"Ver página"** para asegurarte de que se ve correctamente
2. Verifica que:
   - ✅ Los colores morados/azules se ven bien
   - ✅ LicitaBotGi aparece destacado
   - ✅ Los iconos (emojis) se ven
   - ✅ En móvil también se ve bien (reduce la ventana para probar)

---

### Paso 3: Configurar como Página de Inicio (5 min)

1. En WordPress, ve a **"Ajustes"** → **"Lectura"**
2. En **"La página de inicio muestra"**, selecciona **"Una página estática"**
3. En el desplegable **"Página de inicio"**, elige: `Home IsasiLab Nuevo`
4. Haz clic en **"Guardar cambios"**
5. **Visita tu web**: `www.isasilab3d.com` (en navegador de incógnito para ver cambios)

---

### Paso 4: Actualizar Menú de Navegación (OPCIONAL - 5 min)

Si tu web tiene menú de navegación en la parte superior:

1. Ve a **"Apariencia"** → **"Menús"**
2. Localiza el enlace a "Inicio" o "Home"
3. Cámbialo para que apunte a tu nueva página `Home IsasiLab Nuevo`
4. Guarda el menú
5. Si quieres agregar enlaces adicionales:
   - Añade enlace a **"Software"** → `#software-section` (ancla a sección)
   - Añade enlace a **"Diseño 3D"** → `#design-section`
   - Añade enlace a **"Cloud"** → `#cloud-section`

---

## 🔧 OPCIÓN 2: Crear Tema Hijo Personalizado (AVANZADO)

Si prefieres mantener tu tema actual pero reemplazar solo la plantilla de inicio:

### Requisitos:
- Acceso FTP o cPanel File Manager
- Conocimientos básicos de estructura de WordPress

### Pasos:

1. **Conecta por FTP/cPanel** a tu hosting
2. Navega a: `/wp-content/themes/[tu-tema-actual]/`
3. Localiza el archivo `front-page.php` o `home.php`
4. **Haz una copia de seguridad** del archivo original
5. **Edita** el archivo:
   - Busca la sección `<?php get_header(); ?>`
   - Justo después, pega el contenido de `isasilab3d_nueva_web_completa.html`
   - Elimina el resto del contenido hasta `<?php get_footer(); ?>`
6. **Guarda** el archivo
7. Actualiza tu sitio: `www.isasilab3d.com`

**⚠️ ADVERTENCIA**: Esta opción puede romperse al actualizar el tema. Es mejor crear un **tema hijo**.

---

## 🎨 PERSONALIZACIÓN RÁPIDA

### Cambiar colores principales

Localiza en el código HTML la sección `<style>` y busca estas líneas:

```css
/* Color principal morado/azul */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

**Puedes cambiar a:**
- Verde: `#10b981` y `#059669`
- Rojo: `#ef4444` y `#dc2626`
- Naranja: `#f97316` y `#ea580c`

Sustituye **todas las apariciones** de `#667eea` y `#764ba2` por los nuevos colores.

---

### Cambiar textos

Busca en el HTML y edita directamente:
- **Título principal**: Línea `<h1>🚀 IsasiLab</h1>`
- **Subtítulo**: `Software Empresarial • Diseño 3D...`
- **Email contacto**: Todas las apariciones de `isasiapp2023@gmail.com`
- **Precio LicitaBotGi**: `<div class="card-price">99€`

---

### Actualizar enlaces de redes sociales

En el footer, busca la sección `<div class="social-links">`:

```html
<a href="https://instagram.com/isasilab3d" target="_blank" class="social-link">📷</a>
<a href="mailto:isasiapp2023@gmail.com" class="social-link">✉️</a>
<a href="https://github.com/IsasiLab" target="_blank" class="social-link">💻</a>
```

Cambia las URLs según tus perfiles.

---

## ❓ SOLUCIÓN DE PROBLEMAS

### Problema 1: El código HTML se muestra como texto

**Causa**: WordPress está en modo "Visual" en lugar de "Código/Texto"

**Solución**:
1. Edita la página
2. Cambia a **"Editar como HTML"** o pestaña **"Texto"**
3. Vuelve a pegar el código
4. Actualiza

---

### Problema 2: Los estilos (colores) no se ven

**Causa**: Tu tema de WordPress está sobrescribiendo los estilos

**Solución**:
1. En el HTML, busca la línea `<style>`
2. Cámbiala por: `<style>` pero con mayor prioridad:
   
```html
<style id="custom-isasilab-styles">
   /* Añade !important a las propiedades clave */
   .hero { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%) !important; }
</style>
```

---

### Problema 3: La página no se muestra en móvil correctamente

**Causa**: Falta la etiqueta viewport

**Solución**: Asegúrate de que esta línea está en el `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Si usas WordPress, normalmente el tema ya incluye esta etiqueta.

---

### Problema 4: Los enlaces no funcionan

**Verifica**:
- Que el enlace a LicitaBotGi sea: `https://isasilab.github.io/LicitaBotGi-Landing/`
- Que los emails sean clicables: `mailto:isasiapp2023@gmail.com`
- Que el enlace de Instagram sea: `https://instagram.com/isasilab3d`

---

## 📱 VERIFICACIÓN FINAL (Checklist)

Antes de dar por terminado, verifica:

- [ ] La web se ve correctamente en **escritorio**
- [ ] La web se ve correctamente en **móvil** (Chrome DevTools F12 → toggle device toolbar)
- [ ] El color morado/azul se ve en hero y secciones destacadas
- [ ] LicitaBotGi aparece **destacado** con fondo morado
- [ ] Los 2 placeholders dicen "Próximamente"
- [ ] Los 6 servicios de Diseño 3D están en grid
- [ ] La sección Cloud tiene fondo azul
- [ ] Los botones de contacto funcionan (abren email)
- [ ] El enlace a LicitaBotGi abre la landing page
- [ ] El footer tiene 4 columnas con información
- [ ] Los iconos sociales (Instagram, Email, GitHub) funcionan
- [ ] En móvil, las cards se apilan verticalmente (no horizontal)

---

## ⚡ ACCESO RÁPIDO A SECCIONES (para editar después)

Si necesitas editar algo específico, busca estos comentarios en el HTML:

- **Hero**: Busca `<!-- HERO SECTION -->`
- **Software**: Busca `<!-- SOFTWARE SECTION -->`
- **LicitaBotGi destacado**: Busca `<!-- LICITABOTGI - FEATURED -->`
- **Placeholders**: Busca `<!-- PLACEHOLDER para futuro software -->`
- **Diseño 3D**: Busca `<!-- DISEÑO 3D SECTION -->`
- **Cloud**: Busca `<!-- CLOUD SECTION -->`
- **Footer**: Busca `<!-- FOOTER -->`

---

## 📞 NECESITAS AYUDA

Si después de seguir estos pasos algo no funciona:

1. **Verifica** que estás en modo "Código/Texto" (no Visual)
2. **Limpia caché** del navegador (Ctrl+Shift+Delete)
3. **Prueba** en navegador de incógnito
4. **Revisa** si tu hosting/WordPress tiene caché activa (desactívala temporalmente)

---

## ✅ RESULTADO FINAL

Tu nueva web `www.isasilab3d.com` tendrá:

- Hero moderno con gradiente morado/azul
- Sección **Software Empresarial** destacada con LicitaBotGi
- 2 placeholders para futuros software
- Grid de 6 servicios de Diseño 3D
- Sección Cloud M365 profesional
- Footer organizado en 4 columnas
- Totalmente responsive
- Sin dependencias externas (todo inline)

**🎉 ¡Listo para recibir visitas y generar ventas pasivas!**

---

## 📊 PRÓXIMOS PASOS (después de publicar)

1. **Indexa en Google** → Usa [Google Search Console](https://search.google.com/search-console)
2. **Verifica SEO** → Instala plugin Yoast SEO o Rank Math
3. **Añade Analytics** → Google Analytics para ver estadísticas
4. **Promociona** → Sigue la estrategia en `ESTRATEGIA_MARKETING_PASIVO.md`

---

**Fecha de creación**: Febrero 2026  
**Versión**: 1.0  
**Archivo relacionado**: `isasilab3d_nueva_web_completa.html`
