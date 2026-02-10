# 🎯 Guía: Integrar Sección de Software en Tu WordPress Actual

## ✅ Lo Que Vas a Hacer

**AÑADIR** una nueva sección de software a tu página actual **SIN cambiar** nada del diseño existente.

---

## 📋 Paso a Paso (10 minutos)

### Paso 1: Acceder a tu Página Principal

1. Entra a WordPress: `www.isasilab3d.com/wp-admin`
2. Ve a **"Páginas"** en el menú lateral
3. Busca tu página de **"Inicio"** o la que aparece en la portada
4. Haz clic en **"Editar"**

---

### Paso 2: Decidir DÓNDE Insertar la Sección

Tienes 2 opciones:

#### Opción A: ANTES del contenido de Diseño 3D (Recomendado)
- La sección de software aparecerá destacada al principio
- Luego seguirá tu contenido actual de diseño 3D

#### Opción B: DESPUÉS del contenido de Diseño 3D
- Mantienes el diseño 3D como principal
- Software aparece abajo como servicio adicional

---

### Paso 3: Añadir el Bloque HTML

#### Si usas Gutenberg (Editor de bloques):

1. Coloca el cursor donde quieres insertar la sección
2. Haz clic en **"+"** para añadir un bloque
3. Busca: **"HTML Personalizado"** o **"Custom HTML"**
4. Abre el archivo: `wordpress_seccion_software_integrada.html`
5. **Copia TODO** el contenido (Ctrl+A, Ctrl+C)
6. **Pega** en el bloque HTML (Ctrl+V)
7. Haz clic en **"Actualizar"** o **"Publicar"**

#### Si usas Editor Clásico:

1. Cambia a la pestaña **"Texto"** (no "Visual")
2. Coloca el cursor en el lugar deseado
3. **Pega** todo el código del archivo
4. Haz clic en **"Actualizar"**

---

### Paso 4: Vista Previa

1. Haz clic en **"Vista previa"** (botón arriba a la derecha)
2. Verifica que:
   - ✅ La sección aparece correctamente
   - ✅ Los colores se ven bien
   - ✅ El botón "Ver Detalles" funciona
   - ✅ En móvil se ve correctamente (prueba reduciendo la ventana)

---

## 🎨 Personalizar para que Coincida con Tu Tema

### 1. Cambiar Colores

Si los colores morado/azul no coinciden con tu marca:

**Abre el archivo HTML** y busca estas líneas:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

**Reemplaza** `#667eea` y `#764ba2` por tus colores:

**Ejemplo Verde:**
```css
background: linear-gradient(135deg, #10b981 0%, #059669 100%);
```

**Ejemplo Azul:**
```css
background: linear-gradient(135deg, #0078d4 0%, #0053a0 100%);
```

**Ejemplo Rojo:**
```css
background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);
```

**¿Cómo saber tus colores actuales?**

1. Abre tu web: www.isasilab3d.com
2. F12 (DevTools)
3. Haz clic en el icono de seleccionar elemento (flecha)
4. Haz clic en un botón o título de tu web
5. En el panel derecho busca `background-color` o `color`
6. Verás algo como `#XXXXXX` → ese es tu color

---

### 2. Ajustar Espaciado

Si el espaciado no coincide con tu tema:

**Busca la primera línea** del código:
```html
<div class="wp-block-group alignfull" style="margin: 60px 0; padding: 60px 20px;">
```

**Ajusta estos valores**:
- `margin: 60px 0` → Espacio arriba/abajo (60px = espacio generoso)
- `padding: 60px 20px` → Relleno interno

**Ejemplo para menos espacio**:
```html
style="margin: 30px 0; padding: 40px 20px;"
```

---

### 3. Cambiar Ancho Máximo

**Busca**:
```html
style="max-width: 1200px; margin: 0 auto;">
```

**Cambia** `1200px` por el ancho de tu tema:
- Si tu tema usa 1140px: `max-width: 1140px;`
- Si tu tema usa 960px: `max-width: 960px;`
- Si quieres ancho completo: `max-width: 100%;`

---

### 4. Añadir Tu Imagen de LicitaBotGi

**Busca** el div con el icono:
```html
<!-- Imagen/Icono placeholder -->
<div style="text-align: center; padding: 40px; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 10px; margin-bottom: 25px;">
    <div style="font-size: 4rem;">🚀</div>
    ...
</div>
```

**Reemplaza TODO ese bloque** por:
```html
<!-- Tu imagen -->
<div style="text-align: center; margin-bottom: 25px;">
    <img src="URL_DE_TU_IMAGEN" 
         alt="LicitaBotGi - Software de Licitaciones" 
         style="width: 100%; max-width: 600px; height: auto; border-radius: 10px; box-shadow: 0 10px 30px rgba(0,0,0,0.2);">
</div>
```

**Cómo subir la imagen**:

1. En WordPress: **"Medios"** → **"Añadir nuevo"**
2. Sube tu captura de LicitaBotGi o logo
3. Haz clic en la imagen subida
4. Copia la **"URL del archivo"**
5. Pégala donde dice `URL_DE_TU_IMAGEN`

---

### 5. Cambiar Fuentes (si es necesario)

El código usa `inherit` para heredar las fuentes de tu tema automáticamente.

**Si quieres forzar una fuente específica**, añade al principio del div principal:

```html
<div class="wp-block-group alignfull" style="font-family: 'Tu Fuente', sans-serif; ...">
```

**¿Qué fuente usa tu tema actual?**

1. F12 en tu web
2. Selecciona cualquier texto
3. Busca `font-family` en el inspector
4. Copia el valor exacto

**Fuentes comunes de WordPress**:
- Roboto
- Open Sans
- Lato
- Montserrat
- Poppins

---

## 🔧 Integración Avanzada (Opcional)

### Añadir Pestaña de Navegación "Software"

Si tu tema tiene un menú de navegación:

1. Ve a **"Apariencia"** → **"Menús"**
2. En "Enlaces personalizados":
   - **URL**: `#software` (enlace a la sección)
   - **Texto**: `Software`
3. Haz clic en **"Añadir al menú"**
4. **Guarda el menú**

**Ahora añade el ID a la sección**:

En el HTML que pegaste, busca la primera línea:
```html
<div class="wp-block-group alignfull" style="...">
```

Cámbiala por:
```html
<div id="software" class="wp-block-group alignfull" style="...">
```

Ahora el menú navegará directamente a la sección de software.

---

### Duplicar el Estilo de Tus "Cards" Actuales

Si tu tema tiene un estilo de cards específico (como las de Litofanías, Piezas, DICOM):

1. **Inspecciona** una de tus cards actuales con F12
2. Copia las clases CSS: `class="algo-card"` o similar
3. **Añade** esas clases al HTML de la sección software

**Ejemplo**:
```html
<!-- Si tu tema usa class="service-card" -->
<div class="service-card" style="background: white; padding: 30px; ...">
```

Esto hará que las cards de software tengan **exactamente** el mismo estilo que las de diseño 3D.

---

## 📱 Verificar Responsive

Después de publicar, verifica en diferentes tamaños:

### Desktop
- ✅ La card de LicitaBotGi ocupa el ancho completo
- ✅ Los placeholders aparecen en 2 columnas

### Tablet (iPad)
- ✅ Las cards se adaptan
- ✅ Texto legible (no muy pequeño)

### Móvil
- ✅ Cards apiladas verticalmente
- ✅ Precio de 99€ visible y grande
- ✅ Botón "Ver Detalles" clickeable fácilmente

**Cómo probar**:
1. F12 en Chrome
2. Ctrl + Shift + M (modo responsive)
3. Prueba diferentes tamaños

---

## ❓ Problemas Comunes

### Problema 1: El código se muestra como texto

**Causa**: Estás en modo "Visual" en lugar de "Texto/HTML"

**Solución**:
1. Edita la página
2. Si usas Gutenberg: Asegúrate de usar bloque "HTML Personalizado"
3. Si usas Editor Clásico: Cambia a pestaña "Texto"

---

### Problema 2: Los colores no coinciden con mi tema

**Solución**:
1. Inspecciona tu web actual (F12)
2. Encuentra tus colores (hex codes como #XXXXXX)
3. Reemplaza en el código (ver sección "Cambiar Colores")

---

### Problema 3: La sección es muy ancha o muy estrecha

**Solución**:
Ajusta el `max-width`:
```html
style="max-width: 1200px; ..."
```

Prueba con: 1140px, 960px, o 100%

---

### Problema 4: No se ve bien en móvil

**Solución**:
El código YA es responsive. Si tienes problemas:

1. Verifica que tu tema tenga:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

2. Limpia la caché del navegador (Ctrl + Shift + Delete)

3. Prueba en navegador de incógnito

---

## ✅ Checklist Final

Antes de dar por terminado:

- [ ] Sección de software visible en la página principal
- [ ] Colores coinciden con tu tema (o te gustan así)
- [ ] LicitaBotGi destacado correctamente
- [ ] Precio 99€ visible y claro
- [ ] Botón "Ver Detalles" funciona (abre landing page)
- [ ] Placeholders "Próximamente" visibles
- [ ] Responsive: se ve bien en móvil
- [ ] El contenido de Diseño 3D sigue intacto debajo/arriba
- [ ] Menú de navegación actualizado (si añadiste)

---

## 🚀 Próximos Pasos

1. **Publicar** la sección de software
2. **Probar** en diferentes dispositivos
3. **Compartir** con amigos para feedback
4. **Actualizar** cuando tengas más software (usar plantillas de `MANTENIMIENTO_WEBSITE.md`)
5. **Seguir** la estrategia de marketing pasivo (`ESTRATEGIA_MARKETING_PASIVO.md`)

---

## 📞 ¿Necesitas Más Personalización?

Si después de esto quieres:

- Cambiar más cosas del diseño
- Añadir animaciones
- Integrar con plugins específicos
- Modificar la estructura

Consulta `MANTENIMIENTO_WEBSITE.md` para más opciones.

---

**Tiempo total**: 10-15 minutos  
**Dificultad**: Fácil (copiar/pegar)  
**Resultado**: Sección de software integrada profesionalmente en tu web actual

**🎉 ¡Tu web IsasiLab ahora vende Software Y Diseño 3D!**
