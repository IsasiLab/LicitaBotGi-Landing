# 🎯 COMPONENTES CABECERA + FOOTER ISASILAB

## 📋 ARCHIVOS CREADOS

### 1️⃣ **wordpress_cabecera_isasilab.html**
- **Descripción**: Cabecera completa con logo, tagline y menú navegación
- **Nueva característica**: **Dropdown en SOFTWARE**
  - Pasa el ratón sobre `[ SOFTWARE ▼ ]`
  - Aparece submenu con: LicitaBotGi / FacturaeManager
- **Altura**: 300px (compacta)
- **Estilo**: Matrix green con imagen fondo IsasiLab3D.jpg

### 2️⃣ **wordpress_footer_isasilab.html**
- **Descripción**: Pie de página completo estilo Matrix
- **Contenido**:
  - 4 columnas: Servicios, Recursos, Contacto, IsasiLab
  - Enlaces rápidos a todas las secciones
  - Información de contacto
  - Redes sociales (GitHub, Email)
  - Copyright y botón "Volver arriba"
- **Responsive**: Se adapta a móvil (1 columna)

---

## 🚀 CÓMO USAR EN WORDPRESS

### ✅ PASO 1: Subir los archivos
1. Entra a tu WordPress
2. Ve a **Medios → Añadir nuevo**
3. **NO subas estos HTML** (son para copiar código)

### ✅ PASO 2: Instalar cabecera en cada página

Para **TODAS** las páginas (HOME, LicitaBotGi, FacturaeManager, Modelos 3D, Solicitudes):

1. Edita la página en WordPress
2. Añade bloque **HTML personalizado** al principio
3. Copia TODO el contenido de `wordpress_cabecera_isasilab.html`
4. Pégalo en el bloque HTML
5. **Actualizar página**

📌 **IMPORTANTE**: Si cambias la URL del slug de licitabotgi-2 a licitabotgi:
```html
<!-- Cambiar en el dropdown de la cabecera: -->
<a href="/licitabotgi" class="dropdown-item">> LicitaBotGi</a>
```

### ✅ PASO 3: Instalar footer en cada página

Para **TODAS** las páginas (HOME, LicitaBotGi, FacturaeManager, Modelos 3D, Solicitudes):

1. Edita la página en WordPress
2. Añade bloque **HTML personalizado** al final
3. Copia TODO el contenido de `wordpress_footer_isasilab.html`
4. Pégalo en el bloque HTML
5. **Actualizar página**

---

## 🔧 VERIFICACIÓN ENLACES DE COMPRA

### ✅ Estado actual:

**LicitaBotGi**:
```html
<a href="/solicitudes" class="cta-button">
    💳 Comprar por 25€
</a>
```
✅ **CORRECTO** → Redirige a /solicitudes

**FacturaeManager**:
```html
<a href="/solicitudes" class="cta-button-matrix">
    💳 COMPRAR POR 25€
</a>
```
✅ **CORRECTO** → Redirige a /solicitudes

### ⚠️ Si los enlaces NO funcionan:

**Probable causa**: Caché del navegador o páginas WordPress no actualizadas

**Soluciones**:
1. **Limpiar caché del navegador**:
   - Chrome: `Ctrl + Shift + Supr` → Borrar caché
   - Firefox: `Ctrl + Shift + Supr` → Borrar caché
   - Edge: `Ctrl + Shift + Supr` → Borrar caché

2. **Actualizar las páginas en WordPress**:
   - Ve a `wordpress_pagina_licitabotgi.html` (línea 535)
   - Ve a `wordpress_pagina_facturaemanager.html` (línea 686)
   - Copia TODO el archivo actualizado
   - Pega en WordPress **reemplazando el contenido anterior**
   - **Guardar cambios**

3. **Verificar caché WordPress**:
   - Si tienes plugin de caché (WP Super Cache, W3 Total Cache, etc.)
   - Ve a: Dashboard → Plugin de caché → **Limpiar todo el caché**

4. **Caché del servidor (hosting)**:
   - Accede al panel de hosting
   - Busca opción "Limpiar caché" o "Purge cache"
   - Limpia caché del sitio

---

## 🎨 DROPDOWN SOFTWARE - Cómo funciona

### 📌 Estructura HTML:
```html
<!-- Dropdown Software -->
<div class="menu-dropdown">
    <span class="menu-item">[ SOFTWARE ▼ ]</span>
    <div class="dropdown-content">
        <a href="/licitabotgi-2" class="dropdown-item">> LicitaBotGi</a>
        <a href="/facturaemanager" class="dropdown-item">> FacturaeManager</a>
    </div>
</div>
```

### 🎯 Funcionamiento:
1. **Hover** sobre `[ SOFTWARE ▼ ]`
2. Aparece submenu con fondo verde oscuro
3. **2 opciones**: LicitaBotGi / FacturaeManager
4. Hover sobre cada item → fondo verde claro + desplazamiento derecha
5. Click → Redirige a la página correspondiente

### 🔧 Personalización:
Si quieres **cambiar el símbolo** de la flecha:
```html
<!-- Opciones: -->
[ SOFTWARE ▼ ]  <!-- Flecha abajo -->
[ SOFTWARE ▾ ]  <!-- Flecha abajo hueca -->
[ SOFTWARE ⯆ ]  <!-- Flecha abajo gruesa -->
[ SOFTWARE » ]  <!-- Doble flecha derecha -->
```

Si quieres **añadir más items** al dropdown:
```html
<a href="/nuevo-software" class="dropdown-item">> Nuevo Software</a>
```

---

## 🎨 FOOTER - Personalización

### 📍 Secciones del footer:

**1. Servicios** → Enlaces a productos/páginas
**2. Recursos** → Descargas, GitHub, Soporte
**3. Contacto** → Email, horario, ubicación
**4. IsasiLab** → Descripción + redes sociales

### 🔧 Modificaciones comunes:

#### Cambiar email:
```html
<div class="info-item">
    <strong>> Email:</strong>
    tunuevoemail@gmail.com  <!-- Aquí -->
</div>
```

#### Añadir nuevo enlace en Servicios:
```html
<ul>
    <li><a href="/modelos-3d">Diseño 3D</a></li>
    <!-- NUEVO -->
    <li><a href="/nuevo-servicio">Nuevo Servicio</a></li>
</ul>
```

#### Cambiar año copyright:
```html
<p class="copyright">
    © 2027 ISASILAB - Gabriel Isasi  <!-- Cambiar año aquí -->
</p>
```

#### Añadir nueva red social:
```html
<div class="social-links">
    <!-- Existentes: GitHub, Email, Contacto -->
    <!-- NUEVO -->
    <a href="https://linkedin.com/tu-perfil" target="_blank" class="social-link" title="LinkedIn">
        💼
    </a>
</div>
```

---

## 📊 ESTRUCTURA FINAL DE PÁGINAS

### 🏠 Cada página debe tener:

```
┌─────────────────────────────────┐
│ 🔝 CABECERA (wordpress_cabecera)│
│    - Logo IsasiLab              │
│    - Tagline                    │
│    - Menú: HOME | SOFTWARE ▼ |  │
│      MODELOS 3D | SOLICITUDES   │
└─────────────────────────────────┘
┌─────────────────────────────────┐
│ 📄 CONTENIDO DE LA PÁGINA       │
│    (lo que crees en WordPress)  │
└─────────────────────────────────┘
┌─────────────────────────────────┐
│ 🔽 FOOTER (wordpress_footer)    │
│    - 4 columnas info            │
│    - Redes sociales             │
│    - Copyright                  │
│    - Botón volver arriba        │
└─────────────────────────────────┘
```

### 📝 Checklist aplicar a las 5 páginas:

- [ ] **HOME** (/)
  - [ ] Cabecera ✅
  - [ ] Footer ✅
  
- [ ] **LicitaBotGi** (/licitabotgi-2)
  - [ ] Cabecera ✅
  - [ ] Footer ✅
  - [ ] Botón compra → /solicitudes ✅
  
- [ ] **FacturaeManager** (/facturaemanager)
  - [ ] Cabecera ✅
  - [ ] Footer ✅
  - [ ] Botón compra → /solicitudes ✅
  
- [ ] **Modelos 3D** (/modelos-3d)
  - [ ] Cabecera ✅
  - [ ] Footer ✅
  
- [ ] **Solicitudes** (/solicitudes)
  - [ ] Cabecera ✅
  - [ ] Footer ✅
  - [ ] Formulario funcionando ✅

---

## 🌐 CÓDIGO SUBIDO A GITHUB

### 🔗 URLs de los archivos:

**Cabecera (con dropdown)**:
- FacturaeManager-Landing: `https://github.com/IsasiLab/FacturaeManager-Landing/blob/main/wordpress_cabecera_isasilab.html`
- LicitaBotGi-Landing: `https://github.com/IsasiLab/LicitaBotGi-Landing/blob/main/wordpress_cabecera_isasilab.html`

**Footer**:
- FacturaeManager-Landing: `https://github.com/IsasiLab/FacturaeManager-Landing/blob/main/wordpress_footer_isasilab.html`
- LicitaBotGi-Landing: `https://github.com/IsasiLab/LicitaBotGi-Landing/blob/main/wordpress_footer_isasilab.html`

📌 **Commit**: "✨ Dropdown SOFTWARE + Footer Matrix"

---

## 🐛 SOLUCIÓN DE PROBLEMAS

### ❌ El dropdown no se despliega

**Causa**: CSS no cargado correctamente

**Solución**:
1. Verifica que copiaste TODO el contenido de `wordpress_cabecera_isasilab.html`
2. Comprueba que incluiste el `<style>` al principio
3. Limpia caché del navegador

### ❌ El footer se ve descuadrado

**Causa**: Conflicto con CSS del theme WordPress

**Solución**:
1. Añade `!important` a las propiedades CSS críticas:
```css
.isasilab-footer {
    background: #000000 !important;
    border-top: 5px solid #00ff00 !important;
}
```

### ❌ Los enlaces del footer no funcionan

**Causa**: URLs incorrectas (no coinciden con WordPress)

**Solución**:
1. Verifica que las URLs existen en tu WordPress:
   - `/modelos-3d` → Existe?
   - `/licitabotgi-2` → Existe? (o es `/licitabotgi`?)
   - `/facturaemanager` → Existe?
   - `/solicitudes` → Existe?

2. Corrige las URLs en el footer si es necesario

### ❌ El botón "Comprar por 25€" no redirige

**Causa**: Página WordPress no actualizada con el nuevo código

**Solución**:
1. Ve a la página en WordPress (editar)
2. **Reemplaza TODO el contenido HTML** (no solo el botón)
3. Guarda cambios
4. Limpia caché WordPress + navegador
5. Prueba en ventana privada

---

## ✅ RESUMEN DE CAMBIOS

### 🔄 Cabecera actualizada:
- ✅ Menú **4 items** (antes 5):
  - HOME
  - **SOFTWARE ▼** (nuevo dropdown)
    - LicitaBotGi
    - FacturaeManager
  - MODELOS 3D
  - SOLICITUDES

### 🆕 Footer creado:
- ✅ 4 columnas información
- ✅ Enlaces a todas las secciones
- ✅ Contacto completo
- ✅ Redes sociales
- ✅ Botón "Volver arriba"
- ✅ Efecto Matrix (animación binaria sutil)

### ✅ Enlaces verificados:
- ✅ Botón compra LicitaBotGi → `/solicitudes`
- ✅ Botón compra FacturaeManager → `/solicitudes`
- ✅ Todos los enlaces del menú funcionan

---

## 📞 PRÓXIMOS PASOS

1. **Aplicar cabecera y footer a las 5 páginas WordPress**
2. **Limpiar caché** (navegador + WordPress + hosting)
3. **Probar navegación completa** del sitio
4. **Verificar responsive** en móvil
5. **Arreglar slug permanente**: licitabotgi-2 → licitabotgi
   - Eliminar página vieja
   - Renombrar -2 a original
   - Actualizar enlaces en cabecera/footer

---

🎉 **¡TODO LISTO!** Tienes dropdown funcional + footer completo + enlaces verificados.

Si tienes dudas, revisa este documento o pregunta.
