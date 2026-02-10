# 📋 FORMULARIO DE CONTACTO ISASILAB

## ✅ ¿Qué tienes?

Un formulario HTML completo con:
- 📝 **Dos secciones**: Diseño 3D y Software
- 📸 **Upload de imágenes** (para diseños 3D)
- 🎨 **Diseño adaptado a BizBoost** (dark theme)
- 📧 **Envío automático a tu email**: isasiapp2023@gmail.com
- 🚫 **Anti-spam incluido**
- 📱 **100% responsive** (móvil, tablet, desktop)
- 🆓 **Sin plugins** - Solo HTML + servicio gratuito

---

## 🚀 INSTALACIÓN (5 minutos)

### **Opción 1: Página dedicada "Contacto"**

1. **Ir a WordPress**
   - Accede a tu panel: www.isasilab3d.com/wp-admin
   - Ve a: **Páginas → Añadir nueva**

2. **Crear página**
   - Título: "Solicitar Proyecto" o "Contacto"
   - Añade bloque: **HTML Personalizado**
   - Abre el archivo: `formulario_contacto_isasilab.html`
   - **Ctrl+A** (seleccionar todo) → **Ctrl+C** (copiar)
   - Pega en el bloque HTML: **Ctrl+V**

3. **Publicar**
   - Click en **Publicar**
   - Añade al menú: **Apariencia → Menús**

### **Opción 2: Añadir a página existente**

1. **Editar página existente**
   - Ve a: **Páginas → Todas las páginas**
   - Edita donde quieras el formulario (Home, Servicios, etc.)

2. **Añadir bloque HTML**
   - Añade bloque: **HTML Personalizado**
   - Pega el código completo del archivo

3. **Posición recomendada**
   - Al final de la página
   - O después de "Software Empresarial"
   - O crear sección separada "Contacto"

---

## ⚙️ CONFIGURACIÓN (Primera vez - IMPORTANTE)

### **Activar FormSubmit**

La **primera vez** que recibas un formulario:

1. **Recibirás email en**: isasiapp2023@gmail.com
2. **Asunto**: "Activate Form"
3. **Click en el botón azul**: "Activate Form"
4. **Listo** - Ya funciona automáticamente

🔹 Solo necesitas hacer esto **UNA VEZ**
---

## 📧 ¿Cómo funciona el envío?

```
Usuario rellena formulario
        ↓
Click "Enviar Solicitud"
        ↓
FormSubmit.co procesa
        ↓
Email llega a: isasiapp2023@gmail.com
        ↓
Tú respondes en 24-48h
```

### **Formato del email que recibirás:**

```
De: FormSubmit <noreply@formsubmit.co>
Asunto: Nueva Solicitud de Proyecto - IsasiLab

Nombre: Juan Pérez
Email: juan@ejemplo.com
Teléfono: +34 600 000 000
Tipo de proyecto: Diseño 3D
Tipo de diseño 3D: Litofanía
Necesita impresión: Diseño + impresión 3D
Descripción: [texto del usuario]
Presupuesto: 100€ - 300€

[Archivos adjuntos si los hay]
```

---

## 🎯 CARACTERÍSTICAS DEL FORMULARIO

### **Sección: Diseño 3D** 🎨

Cuando el usuario selecciona "Diseño 3D", aparece:
- ✅ Tipo de diseño (Litofanía, Pieza técnica, DICOM, etc.)
- ✅ Upload de imágenes (máx 3 archivos, 10MB cada uno)
- ✅ ¿Necesita impresión 3D?

### **Sección: Software** 💻

Cuando el usuario selecciona "Software", aparece:
- ✅ ¿Qué software? (LicitaBotGi, desarrollo personalizado, consultoría)
- ✅ Tamaño empresa (autónomo, 1-10, 11-50, +50 empleados)
- ✅ ¿Cuándo lo necesita? (urgencia)

### **Campos comunes:**
- Nombre, email, teléfono
- Descripción del proyecto
- Presupuesto estimado (opcional)

---

## 🛠️ PERSONALIZACIÓN

### **1. Cambiar email destino**

**En Formspree panel** (más fácil):
1. Login: https://formspree.io
2. Selecciona tu formulario
3. Settings → Email Address
4. Cambia el email
5. Guarda

**O en el código**:
Crea nuevo formulario en Formspree con el nuevo email y usa ese Form ID.

### **2. Añadir página de "Gracias"**
Archivo: `formulario_contacto_isasilab.html`

```html
<!-- Línea 50 - CAMBIAR AQUÍ -->
<form action="https://formsubmit.co/TU_NUEVO_EMAIL" method="POST">
```

### **2. Añadir página de "Gracias"**

1. Crea página WordPress: "Gracias por contactarnos"
2. Añade este campo después de la línea 54:

```html
<input type="hidden" name="_next" value="https://isasilab3d.com/gracias">
```
| Botón | Gradiente BizBoost | Tu gradiente |

### **4. Añadir más campos**

Ejemplo: añadir campo "Empresa"

```html
<div style="margin-bottom: 20px;">
    <label style="display: block; color: #ffffff; margin-bottom: 8px;">
        Nombre de tu empresa
    </label>
    <input type="text" name="empresa" 
           style="[copiar estilos de otros inputs]"
           placeholder="Ej: Mi Empresa S.L.">
</div>
```

### **5. Quitar campos**

Simplemente elimina el `<div>...</div>` completo del campo.

---

## 🧪 PRUEBA ANTES DE PUBLICAR

### **Checklist de prueba:**

1. ✅ **Enviar formulario de prueba** (rellena todos los campos)
2. ✅ **Verificar email recibido** en isasiapp2023@gmail.com
3. ✅ **Activar FormSubmit** (primera vez - click en email)
4. ✅ **Probar con adjuntos** (subir imagen)
5. ✅ **Verificar recepción de archivos**
6. ✅ **Probar en móvil** (responsive)
7. ✅ **Verificar ambas secciones** (Diseño 3D y Software)

---

## 📱 RESPONSIVE

El formulario se adapta automáticamente:

- **Desktop (>1024px)**: Formulario centrado 800px
- **Tablet (768-1024px)**: Formulario adaptado
- **Móvil (<768px)**: Formulario full width con padding

**Verificar responsive:**
1. F12 (inspeccionar)
2. Ctrl+Shift+M (device toolbar)
3. Probar: iPhone, iPad, Desktop

---

## ❓ PROBLEMAS COMUNES

### **1. Error 404 al enviar**

**Causa**: No configuraste Formspree o el Form ID es incorrecto.

**Solución**:
- Verifica que creaste cuenta en Formspree
- Verifica que creaste el formulario
- Verifica que el Form ID está correcto (empieza con 'x')
- URL debe ser: `https://formspree.io/f/xTU_FORM_ID`

**Alternativa rápida**:
Usa FormSubmit con hash (línea 42):
```html
action="https://formsubmit.co/0e3b8a1c8f7d9a2b5c4e6f1a3d2b9c7e"
```

### **2. No recibo emails**

**Solución**:
- Verifica carpeta SPAM en isasiapp2023@gmail.com
- Verifica email configurado en Formspree panel
- Añade notifications@formspree.io a contactos seguros
- VerificNo recibo emails**

**Solución:**
- Verifica carpeta SPAM en isasiapp2023@gmail.com
- Verifica que activaste FormSubmit (email "Activate Form")
- Añade formsubmit.co a contactos seguros
### **5. Botón no envía**

**Solución:**
- Verifica que campos obligatorios tienen asterisco (*)
- Verifica email válido
- Verifica JavaScript habilitado
- Prueba en otro navegador

---

## 🎯 DÓNDE PONER EL FORMULARIO

### **Recomendaciones:**

1. **Página dedicada** (MEJOR)
   - Crear: "Solicitar Proyecto" o "Contacto"
   - Añadir al menú principal
   - URL: isasilab3d.com/contacto

2. **Al final del Home**
   - Después de sección Software
   - Antes del footer

3. **Página "Servicios"**
   - Después de mostrar servicios
   - Call to action: "¿Tienes un proyecto?"

4. **Sidebar** (NO recomendado)
   - Formulario muy largo para sidebar
   - Mejor usar versión resumida

---

## 📊 MÉTRICAS Y SEGUIMIENTO

### **Qué monitorear:**

1. **Tasa de conversión**
   - Visitas vs envíos de formulario
   - Usa Google Analytics (si está instalado)

2. **Tipo de proyectos**
   - ¿Recibo más consultas de Diseño 3D o Software?
   - Ajusta marketing según demanda

3. **Tiempo de respuesta**
   - Objetivo: responder en 24h
   - Mejor: responder en 12h
   - Crea plantillas de respuesta rápida

4. **Tasa de cierre**
   - De 10 consultas, ¿cuántas se convierten en venta?
   - Si <30%, revisa precios o respuestas

---

## 🚀 NEXT STEPS

### **Después de instalar:**

1. **Probar** (enviar formulario de prueba)
2. **Activar FormSubmit** (click en email)
3. **Promocionar formulario**:
   - Instagram: "¿Tienes un proyecto? Link en bio"
   - Post: Captura del formulario + beneficios
4. **Preparar respuestas rápidas**:
   - Template para Diseño 3D
   - Template para Software
5. **Configurar notificaciones**:
   - Email en móvil (push notifications)
   - Responder rápido = más ventas

### **Mejoras futuras:**

- [ ] Añadir FAQ antes del formulario
- [ ] Añadir testimonios (cuando tengas)
- [ ] Añadir ejemplos de proyectos anteriores
- [ ] Crear página "Gracias" personalizada
- [ ] Integrar con CRM (si crece el volumen)

---

## 📞 SOPORTE

Si tienes problemas:

1. **Revisa este documento** (90% respuestas aquí)
2. **Verifica checklist de prueba**
3. **Documentación FormSubmit**: https://formsubmit.co
4. **Foros WordPress**: wordpress.org/support

---

## 📄 ARCHIVOS DEL PROYECTO

```
LicitaBotGi-Landing/
├── formulario_contacto_isasilab.html ← ARCHIVO PRINCIPAL
├── INSTRUCCIONES_FORMULARIO.md ← ESTE ARCHIVO
├── wordpress_seccion_software_integrada.html
├── INSTRUCCIONES_BIZBOOST_RAPIDO.md
├── RESUMEN_BIZBOOST.md
└── README_WEBSITE.md
```

---

## ✅ RESUMEN RÁPIDO

**Para instalar:**
1. WordPress → Páginas → Añadir nueva
2. Título: "Solicitar Proyecto"
3. Bloque: HTML Personalizado
4. Copiar/pegar código completo
5. Publicar

**Primera vez:**
- Enviar formulario de prueba
- Activar FormSubmit (email)
- Ya funciona automáticamente

**Email destino:**
- isasiapp2023@gmail.com
- Cambiar en línea 50 si necesitas

**Features:**
- ✅ Diseño 3D (con upload imágenes)
- ✅ Software (LicitaBotGi + otros)
- ✅ Responsive
- ✅ Anti-spam
- ✅ Gratuito

---

🎉 **¡Listo para recibir proyectos!**
