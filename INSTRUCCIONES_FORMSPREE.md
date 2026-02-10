# 📧 INSTRUCCIONES FORMSPREE PARA PÁGINA DE RESEÑAS

**Usuario:** Gabriel Isasi Fernández  
**Email registrado en Formspree:** (tu email de la cuenta)

---

## 🚀 Pasos para Configurar el Formulario

### **1. Crear Nuevo Formulario en Formspree**

1. Accede a tu cuenta: [https://formspree.io/forms](https://formspree.io/forms)
2. Haz clic en **"+ New Form"** o **"Nuevo Formulario"**
3. Dale un nombre descriptivo: **"Reseñas IsasiLab"**
4. Selecciona el plan **Free** (50 envíos/mes)
5. Haz clic en **"Create Form"**

### **2. Obtener el Endpoint del Formulario**

Después de crear el formulario, verás un código similar a:

```
https://formspree.io/f/XXXXXXXX
```

**Ejemplo:**
```
https://formspree.io/f/mbjwpzkv
```

**⚠️ IMPORTANTE:** Copia ese código completo. Ese es tu **endpoint único**.

---

## 🔧 Configurar wordpress_pagina_resenas.html

### **Paso 3: Editar el Archivo HTML**

Abre el archivo `wordpress_pagina_resenas.html` y busca la **línea 372**:

```html
<form id="formResena" action="TU_SCRIPT_BACKEND_AQUI" method="POST">
```

**Reemplaza** `TU_SCRIPT_BACKEND_AQUI` por tu endpoint:

```html
<form id="formResena" action="https://formspree.io/f/XXXXXXXX" method="POST">
```

**Ejemplo real:**
```html
<form id="formResena" action="https://formspree.io/f/mbjwpzkv" method="POST">
```

### **Paso 4: Verificar los Campos del Formulario**

Asegúrate de que los campos tengan los atributos `name` correctos:

```html
<input type="text" id="nombre" name="nombre" required>
<input type="email" id="email" name="email" required>
<input type="hidden" id="rating-value" name="rating" required>
<input type="text" id="titulo" name="titulo" required>
<textarea id="comentario" name="comentario" required></textarea>
```

✅ **Ya están configurados correctamente** en el archivo actual.

---

## 📧 Configurar Notificaciones de Email

### **Paso 5: Email de Notificaciones**

1. En tu panel de Formspree, haz clic en el formulario "Reseñas IsasiLab"
2. Ve a **"Settings"** (Configuración)
3. Busca **"Email Notifications"**
4. Añade tu email: **gabriel@isasilab.com** (o el que uses)
5. Activa **"Send me an email when someone submits this form"**

Ahora **recibirás un email cada vez que alguien envíe una reseña**.

---

## ⚙️ Configuración Adicional (Opcional)

### **Personalizar Email de Confirmación**

Por defecto, Formspree envía un email al usuario confirmando su envío. Puedes personalizarlo:

1. En el panel del formulario, ve a **"Settings"**
2. Busca **"Autoresponder"**
3. Activa **"Send an autoresponder email"**
4. Personaliza el mensaje:

```
¡Gracias por tu reseña, {nombre}!

Hemos recibido tu valoración y tu opinión es muy importante para nosotros.

En breve revisaremos tu comentario y lo publicaremos en nuestra página.

Saludos,
Equipo IsasiLab
```

### **Añadir Validación Anti-Spam**

1. En **"Settings"**, busca **"Spam Filtering"**
2. Activa **"reCAPTCHA"** (recomendado)
3. Formspree configura automáticamente Google reCAPTCHA v3 invisible

---

## 🧪 Probar el Formulario

### **Paso 6: Test Local**

1. Abre `wordpress_pagina_resenas.html` en tu navegador local
2. Rellena todos los campos del formulario
3. Selecciona una valoración (estrellas)
4. Haz clic en **"ENVIAR RESEÑA"**

**Primera vez:**
- Formspree te pedirá **confirmar tu email**
- Revisa tu bandeja de entrada
- Haz clic en el enlace de confirmación

**Después de confirmar:**
- El formulario funcionará automáticamente
- Recibirás un email con cada reseña nueva

---

## 📊 Ver Reseñas Enviadas

### **Paso 7: Dashboard de Formspree**

1. Ve a [https://formspree.io/forms](https://formspree.io/forms)
2. Haz clic en **"Reseñas IsasiLab"**
3. Verás todas las reseñas enviadas con:
   - Nombre del usuario
   - Email
   - Valoración (1-5 estrellas)
   - Título
   - Comentario completo
   - Fecha y hora de envío

### **Exportar Datos**

- Puedes exportar todas las reseñas en formato **CSV** o **JSON**
- Botón **"Export"** en el dashboard

---

## 🔒 Límites del Plan Free

| Característica | Plan Free |
|----------------|-----------|
| Envíos/mes | 50 |
| Spam filtering | ✅ Incluido |
| Email notifications | ✅ Incluido |
| Autoresponder | ✅ Incluido |
| Export CSV/JSON | ✅ Incluido |
| File uploads | ❌ No |
| Custom redirects | ❌ No |

**Si superas 50 envíos:**
- Plan Paid: $10/mes (1.000 envíos)
- Plan Professional: $40/mes (10.000 envíos)

---

## 🛠️ Alternativa: Formulario con Redirect

### **Opción A: Redirect Después de Enviar**

Si quieres redirigir al usuario a una página de "Gracias" después del envío:

```html
<form action="https://formspree.io/f/XXXXXXXX" method="POST">
    <!-- Campos del formulario -->
    
    <!-- Campo oculto para redirect -->
    <input type="hidden" name="_next" value="https://isasilab3d.com/gracias-resena">
</form>
```

### **Opción B: Ajax Submit (Sin Recargar)**

Si prefieres enviar el formulario sin recargar la página:

```javascript
// Al final del <script> en wordpress_pagina_resenas.html
document.getElementById('formResena').addEventListener('submit', async function(e) {
    e.preventDefault();
    
    const formData = new FormData(this);
    
    try {
        const response = await fetch('https://formspree.io/f/XXXXXXXX', {
            method: 'POST',
            body: formData,
            headers: {
                'Accept': 'application/json'
            }
        });
        
        if (response.ok) {
            alert('¡Reseña enviada con éxito! Gracias por tu opinión.');
            this.reset();
            // Reset estrellas
            document.querySelectorAll('.star').forEach(s => s.classList.remove('active'));
        } else {
            alert('Error al enviar. Por favor, inténtalo de nuevo.');
        }
    } catch (error) {
        alert('Error de conexión. Verifica tu internet.');
    }
});
```

---

## 🆘 Solución de Problemas

### **Error: "Email not confirmed"**
- **Solución:** Revisa tu email y confirma la dirección con el enlace de Formspree

### **Error: "Form not found"**
- **Solución:** Verifica que el endpoint esté correcto (copia/pega desde Formspree)

### **No recibo emails**
- **Solución:** 
  1. Verifica que las notificaciones estén activadas en Settings
  2. Revisa carpeta SPAM
  3. Añade `noreply@formspree.io` a tus contactos

### **Formulario no envía**
- **Solución:**
  1. Abre la consola del navegador (F12)
  2. Busca errores JavaScript
  3. Verifica que todos los campos `required` estén rellenos
  4. Comprueba que hayas seleccionado una valoración (estrellas)

---

## 📋 Checklist Final

- [ ] Cuenta de Formspree creada
- [ ] Formulario "Reseñas IsasiLab" creado
- [ ] Endpoint copiado correctamente
- [ ] `wordpress_pagina_resenas.html` actualizado (línea 372)
- [ ] Email de notificaciones configurado
- [ ] Autoresponder personalizado (opcional)
- [ ] Test realizado con envío de prueba
- [ ] Email de confirmación recibido
- [ ] Página subida a WordPress
- [ ] Slug `/resenas` configurado
- [ ] Enlaces desde HOME actualizados

---

## 📞 Contacto

**Formspree Support:**  
- Email: support@formspree.io  
- Docs: https://help.formspree.io

**IsasiLab:**  
- Web: https://isasilab3d.com  
- Email: gabriel@isasilab.com

---

**¡Listo para recibir reseñas!** 🎉
