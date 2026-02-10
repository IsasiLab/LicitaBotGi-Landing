# 🎯 INTEGRACIÓN WORDPRESS - TEMA BIZBOOST

## ✨ ¿Qué has recibido?

Un código HTML **100% adaptado** a tu tema **BizBoost** con:

- ✅ **Colores exactos**: #2292b1, #25c5c9, #1b3385 (del tema)
- ✅ **Fondo oscuro**: #0A0C11 (negro oscuro de BizBoost)  
- ✅ **Fuente Poppins**: La misma que usa tu tema
- ✅ **Espaciado responsive**: clamp() igual que BizBoost
- ✅ **Ancho correcto**: 1400px (wide size del tema)

**Archivo que debes usar**: `wordpress_seccion_software_integrada.html`

---

## 📋 INSTALACIÓN EN 5 PASOS

### **1. Accede a WordPress**
```
URL: www.isasilab3d.com/wp-admin
→ Introduce credenciales
→ Menú: Páginas → Inicio → Editar
```

### **2. Añade Bloque HTML**
**Gutenberg** (editor bloques):
- Click "+" → Buscar "HTML Personalizado"

**Editor Clásico**:
- Pestaña "Texto" (NO "Visual")

### **3. Copia y Pega**
```
1. Abre: wordpress_seccion_software_integrada.html
2. Ctrl+A (seleccionar todo)
3. Ctrl+C (copiar)
4. En WordPress → Ctrl+V (pegar)
```

### **4. Ubica la Sección**
**Opción A** (Recomendada): Después de estadísticas (95 proyectos, 2310 clientes...)  
**Opción B**: Al final, antes del footer

### **5. Publica**
```
Vista Previa → Verificar → Publicar/Actualizar
```

✅ **TERMINADO** - La sección ya está integrada

---

## 🎨 PERSONALIZAR (Opcional)

### Cambiar Imagen LicitaBotGi

**Sube imagen a WordPress**:
1. Medios → Añadir nuevo → Sube captura de LicitaBotGi
2. Copia URL (ej: `https://isasilab3d.com/wp-content/uploads/2026/02/screenshot.jpg`)

**Reemplaza el código**:
Busca este bloque:
```html
<div style="text-align: center; padding: clamp(30px, 4vw, 45px); background: linear-gradient(to right, #1b3385 0%, #25c5c9 100%); border-radius: 12px; margin-bottom: 30px; box-shadow: 0 8px 25px rgba(37,197,201,0.2);">
    <div style="font-size: clamp(3rem, 5vw, 4.5rem); margin-bottom: 12px; filter: drop-shadow(2px 2px 6px rgba(0,0,0,0.4));">🚀</div>
    ...
</div>
```

Reemplázalo por:
```html
<img src="https://isasilab3d.com/wp-content/uploads/2026/02/screenshot.jpg" 
     alt="LicitaBotGi - Licitaciones con IA" 
     style="width: 100%; max-width: 700px; height: auto; border-radius: 12px; box-shadow: 0 10px 40px rgba(0,0,0,0.4); margin-bottom: 30px; display: block; margin-left: auto; margin-right: auto;">
```

### Ajustar Espaciado

**Más/menos espacio arriba/abajo**:
```html
<!-- ACTUAL -->
margin: clamp(42px, 7.5vw, 140px) 0 clamp(12px, 5.5vw, 70px);

<!-- MÁS ESPACIO -->
margin: clamp(60px, 10vw, 180px) 0 clamp(30px, 8vw, 100px);

<!-- MENOS ESPACIO -->
margin: clamp(20px, 4vw, 60px) 0 clamp(5px, 2vw, 30px);
```

### Añadir Más Software (Futuro)

Cuando tengas un segundo producto, duplica este código:
```html
<div style="background: #222222; padding: clamp(25px, 3vw, 35px); border-radius: 15px; box-shadow: 0 10px 40px rgba(0,0,0,0.3); border: 2px solid #323438; position: relative; overflow: hidden;">
    <!-- Barra superior -->
    <div style="position: absolute; top: 0; left: 0; right: 0; height: 5px; background: linear-gradient(to right, #1b3385 0%, #25c5c9 100%);"></div>
    
    <!-- Icono -->
    <div style="text-align: center; font-size: clamp(3rem, 5vw, 4rem); margin-bottom: 20px;">💡</div>
    
    <!-- Título -->
    <h3 style="font-size: clamp(24px, 2vw, 28px); margin-bottom: 15px; color: #ffffff; font-family: var(--wp--preset--font-family--poppins), 'Poppins', sans-serif; font-weight: 700;">
        Nombre del Nuevo Software
    </h3>
    
    <!-- Descripción -->
    <p style="color: #abadb3; line-height: 1.75; margin-bottom: 20px; font-family: var(--wp--preset--font-family--poppins), 'Poppins', sans-serif;">
        Descripción breve del software
    </p>
    
    <!-- Precio -->
    <div style="text-align: center; margin: 25px 0;">
        <span style="font-size: clamp(1.8rem, 3vw, 2.2rem); font-weight: 700; color: #2292b1;">149€</span>
        <span style="font-size: 1rem; color: #666666;"> / licencia</span>
    </div>
    
    <!-- Botón -->
    <div style="text-align: center;">
        <a href="URL_NUEVA_LANDING" target="_blank"
           style="display: inline-block; background: linear-gradient(to right, #1b3385 0%, #25c5c9 100%); color: #ffffff; padding: 12px 35px; border-radius: 50px; text-decoration: none; font-weight: 700; font-family: var(--wp--preset--font-family--poppins), 'Poppins', sans-serif;">
            Ver Detalles →
        </a>
    </div>
</div>
```

---

## 🔍 VERIFICAR RESPONSIVE

### Desktop (> 1024px)
- [x] LicitaBotGi ocupa ancho completo (destacado)
- [x] Placeholders en 2 columnas lado a lado
- [x] Precio 99€ grande y visible
- [x] Fondo oscuro #0A0C11
- [x] Cards con fondo #222222

### Tablet (768px - 1024px)
- [x] Cards adaptan tamaño
- [x] Texto legible
- [x] Botones fáciles de clickear

### Móvil (< 768px)
- [x] Cards apilan verticalmente
- [x] Precio visible sin zoom
- [x] Botón grande (fácil de tocar)
- [x] Checkmarks ✓ alineados

**Cómo probar**:
```
F12 → Ctrl+Shift+M → Probar diferentes tamaños
```

---

## ❌ SOLUCIÓN DE PROBLEMAS

### El código aparece como texto
**Solución**: Usa bloque "HTML Personalizado" (Gutenberg) o pestaña "Texto" (Clásico)

### Los colores son claros en lugar de oscuros
**Solución**: 
1. Añade `!important` a los estilos principales
2. Limpia cache (Ctrl+F5 o plugin de cache)
3. Prueba en modo incógnito

### La sección es muy ancha/estrecha
**Solución**: Cambia `max-width: 1400px` por:
- `1200px` (más estrecho)
- `1600px` (más ancho)  
- `100%` (ancho completo)

### No se ve en móvil
**Solución**:
1. Verifica viewport meta tag en `<head>`
2. Limpia cache browser
3. Prueba modo incógnito

---

## ✅ CHECKLIST FINAL

Antes de dar por finalizado:

- [ ] Sección visible en página inicio
- [ ] Fondo oscuro #0A0C11 aplicado
- [ ] Cards fondo #222222 (gris oscuro)
- [ ] Texto blanco #ffffff legible
- [ ] Gradiente azul visible (#1b3385 → #25c5c9)
- [ ] Fuente Poppins aplicada
- [ ] Precio 99€ en #2292b1 (azul turquesa)
- [ ] Checkmarks ✓ en #25c5c9 (azul verde)
- [ ] Botón funciona (abre landing LicitaBotGi)
- [ ] Responsive en móvil (cards apilan)
- [ ] Hover effects funcionan
- [ ] Contenido 3D NO afectado

---

## 🎯 COLORES DEL TEMA BIZBOOST

Para referencia rápida:

| Elemento | Color | Uso |
|----------|-------|-----|
| Background | `#0A0C11` | Fondo principal sección |
| Card BG | `#222222` | Fondo de cards |
| Primary | `#2292b1` | Precio, acentos |
| Blue-Green | `#25c5c9` | Checkmarks, gradiente |
| Patrick Blue | `#1b3385` | Gradiente inicio |
| Text | `#ffffff` | Títulos, textos destacados |
| Body Text | `#abadb3` | Párrafos, descripciones |
| Border | `#323438` | Bordes de cards |
| Meta | `#666666` | Texto secundario (/ licencia) |

---

## 📞 PRÓXIMOS PASOS

1. ✅ **Publicar** la sección
2. 📸 **Captura** screenshot de LicitaBotGi → Reemplazar emoji
3. 📱 **Instagram**: Actualizar bio "@isasilab3d"
   - Antes: "🎨 Diseño 3D personalizado"
   - Después: "🎨 Diseño 3D + 💻 Software Empresarial"
4. 📧 **Monitorear** isasiapp2023@gmail.com
5. 📈 **Seguir** ESTRATEGIA_MARKETING_PASIVO.md

¡Tu sección está lista!
