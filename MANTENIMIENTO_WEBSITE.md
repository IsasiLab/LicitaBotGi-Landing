# 🔧 Guía de Mantenimiento y Actualización - isasilab3d.com

## 📋 Contenido

1. [Añadir Nuevo Software](#añadir-nuevo-software)
2. [Añadir Nuevo Servicio 3D](#añadir-nuevo-servicio-3d)
3. [Actualizar Precios](#actualizar-precios)
4. [Cambiar Información de Contacto](#cambiar-información-de-contacto)
5. [Modificar Colores del Sitio](#modificar-colores-del-sitio)
6. [Actualizar Enlaces de Redes Sociales](#actualizar-enlaces-de-redes-sociales)
7. [Plantillas Reutilizables](#plantillas-reutilizables)

---

## 🚀 1. AÑADIR NUEVO SOFTWARE

### Paso a Paso

Cuando tengas un nuevo software listo para publicar:

#### 1.1. Localiza los placeholders

1. Abre el archivo HTML de tu web en WordPress (modo Código/Texto)
2. Busca con Ctrl+F: `<!-- PLACEHOLDER para futuro software -->`
3. Encontrarás 2 cards de placeholder:

```html
<!-- PLACEHOLDER para futuro software -->
<div class="card placeholder-card">
    <div class="card-icon">📦</div>
    <h3 class="card-title">Próximamente</h3>
    <p style="color: #999;">Más herramientas empresariales en desarrollo</p>
</div>
```

#### 1.2. Reemplaza con esta plantilla

**ELIMINA** todo el bloque `<div class="card placeholder-card">...</div>` y **PEGA** esta plantilla:

```html
<!-- NUEVO SOFTWARE -->
<div class="card">
    <div class="card-icon">🔧</div>
    <h3 class="card-title">Nombre de tu Software</h3>
    <p class="card-description">
        Descripción breve de qué hace el software (2-3 líneas). 
        Explica el problema que resuelve de forma clara.
    </p>
    
    <ul class="card-features">
        <li>Característica principal 1</li>
        <li>Característica principal 2</li>
        <li>Característica principal 3</li>
        <li>Característica principal 4</li>
        <li>Característica principal 5</li>
    </ul>
    
    <div class="card-price">149€ <span class="card-price-note">/ licencia</span></div>
    
    <a href="https://TU_LANDING_PAGE_AQUI" target="_blank" class="card-button">
        Ver Detalles →
    </a>
</div>
```

#### 1.3. Personaliza los campos

**Reemplaza estos valores**:

| Campo | Qué poner |
|-------|-----------|
| `🔧` (icono) | Emoji apropiado: 📊 📈 📋 🗂️ 💼 🎯 |
| `Nombre de tu Software` | Nombre comercial del producto |
| `Descripción breve` | 2-3 frases sobre qué hace |
| `Característica 1-5` | Lista de beneficios clave |
| `149€` | Precio de tu licencia |
| `https://TU_LANDING_PAGE_AQUI` | URL de la landing page |

#### 1.4. Ejemplo real

```html
<!-- EJEMPLO: FacturaBot -->
<div class="card">
    <div class="card-icon">📄</div>
    <h3 class="card-title">FacturaBot</h3>
    <p class="card-description">
        Automatiza la lectura y extracción de datos de facturas PDF en formato Facturae. 
        Integra con tu sistema de contabilidad en segundos.
    </p>
    
    <ul class="card-features">
        <li>Lectura automática de XML Facturae</li>
        <li>Extracción de datos fiscales</li>
        <li>Validación de NIFs</li>
        <li>Exportación a Excel/CSV</li>
        <li>Integración con ERP</li>
    </ul>
    
    <div class="card-price">79€ <span class="card-price-note">/ licencia</span></div>
    
    <a href="https://isasilab.github.io/FacturaBot-Landing/" target="_blank" class="card-button">
        Ver Detalles →
    </a>
</div>
```

---

### Si necesitas MÁS de 3 software

Si ya usaste los 2 placeholders y necesitas añadir más software:

1. Copia **toda** la plantilla anterior otra vez
2. Pégala **antes** de la etiqueta de cierre `</div>` de `.cards-grid`
3. Personaliza los datos
4. El grid se ajustará automáticamente (responsive)

---

## 🎨 2. AÑADIR NUEVO SERVICIO 3D

### Paso a Paso

#### 2.1. Localiza la grid de diseño 3D

Busca con Ctrl+F: `<div class="design-grid">`

Verás 6 items como este:

```html
<div class="design-item">
    <div class="design-item-icon">🖼️</div>
    <h3>Litofanías</h3>
    <p>Transforma tus fotos en relieves 3D iluminados</p>
</div>
```

#### 2.2. Añadir un nuevo servicio

**AL FINAL** de la lista (antes del `</div>` de cierre de `.design-grid`), **PEGA**:

```html
<div class="design-item">
    <div class="design-item-icon">🎁</div>
    <h3>Nombre del Servicio</h3>
    <p>Descripción corta del servicio (1-2 líneas)</p>
</div>
```

#### 2.3. Ejemplo real

```html
<div class="design-item">
    <div class="design-item-icon">🏆</div>
    <h3>Trofeos Personalizados</h3>
    <p>Diseño de trofeos y premios únicos para eventos y competiciones</p>
</div>
```

---

## 💰 3. ACTUALIZAR PRECIOS

### Cambiar precio de LicitaBotGi

1. Busca: `<div class="card-price">99€`
2. Cambia `99€` por el nuevo precio (ej. `129€`)
3. **IMPORTANTE**: Busca con Ctrl+F `99€` para cambiar **todas las apariciones**:
   - En la card destacada de LicitaBotGi
   - En el footer si aparece
   - En cualquier otra mención

### Añadir descuentos temporales

Debajo del precio, añade:

```html
<div class="card-price">
    <span style="text-decoration: line-through; color: #999;">149€</span> 
    99€ 
    <span class="card-price-note">/ licencia</span>
</div>
<p style="color: #059669; font-weight: bold; margin-top: 10px;">
    ✨ Oferta de lanzamiento - Ahorra 50€
</p>
```

---

## 📧 4. CAMBIAR INFORMACIÓN DE CONTACTO

### Email

Busca todas las apariciones de `isasiapp2023@gmail.com` y reemplaza por tu nuevo email.

**IMPORTANTE**: Hay varios lugares donde aparece:
- Botones "Consultar Proyecto"
- Footer (múltiples menciones)
- Enlaces de contacto

**Usa Ctrl+H** (Buscar y Reemplazar) para cambiarlos todos a la vez:
- Buscar: `isasiapp2023@gmail.com`
- Reemplazar con: `tunuevoemail@ejemplo.com`

### Instagram

Busca: `https://instagram.com/isasilab3d`  
Reemplaza por tu nueva cuenta (si cambias)

### Otras redes

En el footer, sección `<div class="social-links">`, añade más iconos:

```html
<!-- LinkedIn -->
<a href="https://linkedin.com/in/TU_PERFIL" target="_blank" class="social-link" title="LinkedIn">💼</a>

<!-- Twitter/X -->
<a href="https://twitter.com/TU_USUARIO" target="_blank" class="social-link" title="Twitter">🐦</a>

<!-- YouTube -->
<a href="https://youtube.com/@TU_CANAL" target="_blank" class="social-link" title="YouTube">📺</a>
```

---

## 🎨 5. MODIFICAR COLORES DEL SITIO

### Cambio global de colores

Si quieres cambiar el esquema de color morado/azul por otro:

#### 5.1. Identifica los colores actuales

- **Morado claro**: `#667eea`
- **Morado oscuro**: `#764ba2`
- **Azul Cloud**: `#0078d4` y `#0053a0`
- **Verde (checkmarks)**: `#059669`

#### 5.2. Elige tu nueva paleta

**Ejemplo 1: Esquema Verde**
- Color 1: `#10b981`
- Color 2: `#059669`

**Ejemplo 2: Esquema Naranja**
- Color 1: `#f97316`
- Color 2: `#ea580c`

**Ejemplo 3: Esquema Rojo**
- Color 1: `#ef4444`
- Color 2: `#dc2626`

#### 5.3. Reemplazar colores

Usa **Ctrl+H** (Buscar y Reemplazar):

1. Buscar: `#667eea` → Reemplazar: `#10b981` (tu nuevo color 1)
2. Buscar: `#764ba2` → Reemplazar: `#059669` (tu nuevo color 2)
3. Haz clic en "Reemplazar todo"

**NOTA**: No toques `#0078d4` (azul de Cloud) ni `#059669` (verde checks) a menos que quieras cambiarlos también.

---

## 🔗 6. ACTUALIZAR ENLACES DE REDES SOCIALES

### Footer social links

Localiza en el footer:

```html
<div class="social-links">
    <a href="https://instagram.com/isasilab3d" target="_blank" class="social-link" title="Instagram">📷</a>
    <a href="mailto:isasiapp2023@gmail.com" class="social-link" title="Email">✉️</a>
    <a href="https://github.com/IsasiLab" target="_blank" class="social-link" title="GitHub">💻</a>
</div>
```

**Cambia las URLs** según tus perfiles.

---

## 📦 7. PLANTILLAS REUTILIZABLES

### Plantilla: Card de Software Completa

```html
<div class="card">
    <div class="card-icon">[EMOJI]</div>
    <h3 class="card-title">[NOMBRE SOFTWARE]</h3>
    <p class="card-description">
        [DESCRIPCIÓN 2-3 LÍNEAS]
    </p>
    
    <ul class="card-features">
        <li>[FEATURE 1]</li>
        <li>[FEATURE 2]</li>
        <li>[FEATURE 3]</li>
        <li>[FEATURE 4]</li>
        <li>[FEATURE 5]</li>
        <li>[FEATURE 6 opcional]</li>
    </ul>
    
    <div class="card-price">[PRECIO]€ <span class="card-price-note">/ licencia</span></div>
    
    <a href="[URL_LANDING]" target="_blank" class="card-button">
        Ver Detalles →
    </a>
</div>
```

---

### Plantilla: Servicio 3D Simple

```html
<div class="design-item">
    <div class="design-item-icon">[EMOJI]</div>
    <h3>[NOMBRE SERVICIO]</h3>
    <p>[DESCRIPCIÓN CORTA]</p>
</div>
```

---

### Plantilla: Feature Cloud

```html
<div class="cloud-feature">
    <div class="cloud-feature-icon">[EMOJI]</div>
    <h3>[NOMBRE FEATURE]</h3>
    <p>[DESCRIPCIÓN]</p>
</div>
```

---

### Plantilla: Sección FAQ (si quieres añadir)

```html
<!-- SECCIÓN FAQ -->
<section style="padding: 80px 20px; background: #f8f9fa;">
    <div class="container">
        <h2 class="section-title">❓ Preguntas Frecuentes</h2>
        
        <div style="max-width: 800px; margin: 0 auto;">
            
            <!-- Pregunta 1 -->
            <div style="margin-bottom: 30px; padding: 25px; background: white; border-radius: 15px; box-shadow: 0 5px 20px rgba(0,0,0,0.05);">
                <h3 style="color: #667eea; margin-bottom: 10px;">¿[PREGUNTA]?</h3>
                <p style="color: #666; line-height: 1.8;">[RESPUESTA]</p>
            </div>
            
            <!-- Pregunta 2 -->
            <div style="margin-bottom: 30px; padding: 25px; background: white; border-radius: 15px; box-shadow: 0 5px 20px rgba(0,0,0,0.05);">
                <h3 style="color: #667eea; margin-bottom: 10px;">¿[PREGUNTA]?</h3>
                <p style="color: #666; line-height: 1.8;">[RESPUESTA]</p>
            </div>
            
        </div>
    </div>
</section>
```

---

## 📅 CALENDARIO DE MANTENIMIENTO SUGERIDO

### Trimestral (cada 3 meses)

- [ ] Revisar que todos los enlaces funcionen (landing pages, email, redes)
- [ ] Verificar que los precios estén actualizados
- [ ] Añadir nuevos software si están listos
- [ ] Actualizar servicios 3D si hay novedades
- [ ] Revisar métricas de visitas (Google Analytics)

### Semestral (cada 6 meses)

- [ ] Revisar colores y diseño (¿sigue siendo moderno?)
- [ ] Actualizar contenido de texto (descripción de servicios)
- [ ] Verificar que la web sea responsive en nuevos dispositivos
- [ ] Backup completo de la web

### Anual

- [ ] Rediseño parcial si es necesario
- [ ] Actualizar estrategia de marketing pasivo
- [ ] Revisar y ajustar precios según mercado
- [ ] Añadir testimonios de clientes si tienes

---

## 🎯 EMOJIS RECOMENDADOS

Para mantener coherencia visual, usa estos emojis según categoría:

### Software/Tech
🚀 📱 💻 🖥️ ⚙️ 🔧 🛠️ 📊 📈 📉 💾 🗂️ 📋 🎯 💼 🔐 🔑

### Diseño 3D
🎨 🖼️ 🎭 🏺 💍 🦴 🔬 🏥 🦷 🏆 🎁 🧩 🎲

### Cloud/Network
☁️ 🌐 📡 🔗 📮 ✉️ 🔒 🛡️

### Checkmarks/Success
✅ ✓ ✔️ 🟢 ⭐

---

## 🚨 ERRORES COMUNES Y SOLUCIONES

### Error 1: El código se muestra como texto

**Problema**: Pegas el HTML y se ve el código crudo en la web

**Solución**: Estás en modo "Visual" en lugar de "Código/Texto"
1. Edita la página en WordPress
2. Cambia a modo "Editar como HTML" o pestaña "Texto"
3. Pega de nuevo

---

### Error 2: Los estilos desaparecen

**Problema**: Después de actualizar, los colores o diseño se pierde

**Solución**: Tu tema de WordPress está sobrescribiendo los estilos
1. En la etiqueta `<style>`, añade `!important` a las propiedades clave:

```css
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%) !important;
}
```

---

### Error 3: Los enlaces no abren

**Problema**: Al hacer clic en botones no pasa nada

**Solución**: Verifica que tengan `target="_blank"` y el protocolo completo:
- ✅ Correcto: `https://isasilab.github.io/LicitaBotGi-Landing/`
- ❌ Incorrecto: `isasilab.github.io` (falta https://)

---

## 📞 AYUDA RÁPIDA

### Para editar, recuerda:

1. **Siempre** trabaja en modo "Código/Texto" (NO Visual)
2. **Haz backup** antes de editar (exportar contenido)
3. **Prueba en navegador incógnito** después de cambios
4. **Limpia caché** del navegador si no ves cambios (Ctrl+Shift+Delete)
5. **Guarda con frecuencia** mientras editas

### Archivos relacionados

- `isasilab3d_nueva_web_completa.html` - Código fuente completo
- `INSTRUCCIONES_WORDPRESS_WEB_COMPLETA.md` - Guía de instalación inicial
- `ESTRATEGIA_MARKETING_PASIVO.md` - Estrategia de promoción

---

## ✅ CHECKLIST DESPUÉS DE EDITAR

Antes de publicar cambios, verifica:

- [ ] El código está pegado en modo "Código/Texto" (NO Visual)
- [ ] Los cambios se ven correctamente en la vista previa
- [ ] La web se ve bien en móvil (F12 → modo responsive)
- [ ] Todos los enlaces funcionan (probar cada uno)
- [ ] Los botones de email abren el cliente de correo
- [ ] El precio está actualizado correctamente
- [ ] Los emojis se ven (no cuadrados vacíos)
- [ ] El footer tiene la información correcta

---

**Última actualización**: Febrero 2026  
**Versión**: 1.0  
**Mantenedor**: IsasiLab  

---

**¿Dudas?** Consulta primero:
1. `INSTRUCCIONES_WORDPRESS_WEB_COMPLETA.md` (instalación inicial)
2. Este documento (mantenimiento)
3. `ESTRATEGIA_MARKETING_PASIVO.md` (promoción)

**🎉 ¡Tu web está lista para crecer!**
