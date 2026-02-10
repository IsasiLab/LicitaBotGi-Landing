# 🚨 CÓMO INSERTAR EL FOOTER EN WORDPRESS (PASO A PASO)

## ⚠️ IMPORTANTE: Tipo de bloque correcto

El footer NO se ve porque **necesitas usar el bloque correcto**. Sigue estos pasos EXACTAMENTE:

---

## 📋 MÉTODO 1: Bloque HTML Personalizado (RECOMENDADO)

### ✅ Paso 1: Editar la página en WordPress

1. Ve a tu WordPress Dashboard
2. Páginas → Selecciona la página (ej: HOME)
3. Click en **"Editar"**

### ✅ Paso 2: Ir al FINAL de la página

1. **Desplázate hasta el FINAL** del contenido
2. Click en el botón **"+" (Añadir bloque)**
3. Busca: **"HTML personalizado"** o **"Custom HTML"**
4. Click en ese bloque

### ✅ Paso 3: Copiar el código del footer

1. Abre el archivo: `wordpress_footer_isasilab.html`
2. Selecciona **TODO** el contenido (Ctrl+A)
3. Copia (Ctrl+C)

### ✅ Paso 4: Pegarlo en WordPress

1. Ve al bloque "HTML personalizado" que creaste
2. **Pega el código** (Ctrl+V)
3. **Actualizar página** (botón azul arriba a la derecha)

### ✅ Paso 5: Ver resultado

1. Click en **"Vista previa"** o **"Ver página"**
2. Desplázate hasta el final de la página
3. Deberías ver el footer con:
   - Logo IsasiLab3D arriba
   - 4 columnas (Servicios, Recursos, Contacto, IsasiLab)
   - Fondo negro con bordes verdes
   - Iconos emoji en todos los enlaces

---

## 🖼️ PROBLEMA: No se ve la imagen IsasiLab3D

### Solución A: Subir la imagen a Medios de WordPress

Si la imagen de GitHub no carga:

1. Ve a **Medios → Añadir nuevo**
2. Sube el archivo **IsasiLab3D.jpg** desde tu PC
3. Copia la **URL de la imagen** (ej: `https://isasilab3d.com/wp-content/uploads/2026/02/IsasiLab3D.jpg`)
4. En el código del footer, busca:
   ```html
   <img src="https://raw.githubusercontent.com/IsasiLab/FacturaeManager-Landing/main/assets/IsasiLab3D.jpg" alt="IsasiLab - Diseño 3D, Software y Cloud">
   ```
5. **Reemplaza** con tu URL:
   ```html
   <img src="https://isasilab3d.com/wp-content/uploads/2026/02/IsasiLab3D.jpg" alt="IsasiLab - Diseño 3D, Software y Cloud">
   ```

### Solución B: Usar imagen desde tu hosting

1. Accede a tu hosting (cPanel, FTP, etc.)
2. Sube `IsasiLab3D.jpg` a: `/public_html/assets/`
3. Usa la URL: `https://isasilab3d.com/assets/IsasiLab3D.jpg`

---

## 🐛 PROBLEMA: Se ve desordenado

### Causa: El theme de WordPress tiene CSS que interfiere

### Solución: El código ya está preparado con `!important`

El archivo `wordpress_footer_isasilab.html` **ya tiene** todas las propiedades con `!important` para forzar los estilos.

Si aún así se ve mal:

#### Opción 1: Modo texto del editor clásico

Si tu WordPress tiene **Editor Clásico**:

1. Ve a: **Herramientas → Opciones de pantalla** (arriba a la derecha)
2. Activa: **"Editor clásico"**
3. En la página, cambia a **Modo "Texto"** (arriba a la derecha, junto a "Visual")
4. Pega el código del footer al final
5. **NO vuelvas a modo "Visual"**, guarda directamente

#### Opción 2: Plugin Code Snippets

Si nada funciona:

1. Instala plugin: **"Code Snippets"**
2. Ve a: **Snippets → Añadir nuevo**
3. Título: "Footer IsasiLab"
4. Pega el código del footer
5. Tipo: **PHP Snippet**
6. Código:
   ```php
   <?php
   add_action('wp_footer', function() {
       // Aquí pega TODO el código del footer (incluido el <style>)
   });
   ?>
   ```
7. Activar snippet

---

## 🔍 VERIFICAR QUE TODO ESTÁ CORRECTO

### ✅ Checklist visual:

- [ ] **Logo IsasiLab3D** visible arriba del footer
- [ ] **Fondo negro** en todo el footer
- [ ] **Borde verde** en la parte superior
- [ ] **4 columnas** bien alineadas (en PC)
- [ ] **Iconos emoji** en cada enlace (🎨 📋 💼 ☁️ 🤖)
- [ ] **Redes sociales** (4 círculos verdes: 💻 📧 📞 🎨)
- [ ] **Copyright** al final: "© 2026 ISASILAB"
- [ ] **Botón "VOLVER ARRIBA"** funcional

### ❌ Si algo falla:

**Logo no se ve**:
- Sube la imagen a Medios de WordPress
- Usa URL completa `https://tudominio.com/...`

**Todo desordenado**:
- Verifica que usaste **"HTML personalizado"** (NO "Código")
- Limpia caché de WordPress
- Limpia caché del navegador (Ctrl+Shift+Supr)

**Colores raros**:
- El theme de WordPress está interfiriendo
- Usa el método del plugin "Code Snippets"

**No se ve nada**:
- El bloque está vacío, vuelve a pegar el código
- O pegaste en el lugar equivocado (debe ir al FINAL)

---

## 🎯 RESUMEN RÁPIDO

```
1. WordPress → Editar página
2. Ir al FINAL del contenido
3. Click en "+" (Añadir bloque)
4. Buscar: "HTML personalizado"
5. Pegar TODO el código del footer
6. Actualizar página
7. Ver resultado (debe verse el logo + 4 columnas verde Matrix)
```

---

## 📞 SI SIGUES CON PROBLEMAS

**Comparte conmigo**:
1. Captura de pantalla de cómo se ve
2. Captura del bloque WordPress donde lo pegaste
3. URL de la página para revisar

**Información útil para diagnosticar**:
- ¿Qué theme de WordPress usas? (ej: Astra, GeneratePress, etc.)
- ¿Qué editor? (Gutenberg / Elementor / Divi / etc.)
- ¿Te sale algún error en la consola del navegador? (F12 → Consola)

---

🎉 **Con estos pasos debería funcionar perfectamente**
