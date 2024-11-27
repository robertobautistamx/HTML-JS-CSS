# **Introducción a JavaScript**

JavaScript es uno de los lenguajes de programación más utilizados para desarrollar páginas web interactivas y dinámicas. Se ejecuta en el navegador del cliente, lo que lo convierte en una herramienta fundamental para la experiencia del usuario.

---

## **1. Usos de JavaScript**

### **¿Qué es JavaScript?**

JavaScript es un lenguaje de programación que permite agregar interactividad, manipular elementos del DOM, realizar cálculos, y comunicarse con servidores a través de APIs.

### **¿Para qué se usa JavaScript?**

1. **Interactividad en Páginas Web:**
   - Crear menús desplegables.
   - Validar formularios.
   - Reproducir animaciones.
   - Mostrar notificaciones.

2. **Manipulación del DOM:**
   - Modificar, eliminar o crear elementos HTML dinámicamente.
   - Cambiar estilos de los elementos.

3. **Comunicación Cliente-Servidor:**
   - Realizar peticiones HTTP usando `fetch()` o librerías como Axios.
   - Implementar APIs RESTful para obtener o enviar datos.

4. **Desarrollo Completo:**
   - **Frontend:** Usando frameworks como React, Vue o Angular.
   - **Backend:** Con Node.js para aplicaciones del lado del servidor.

---

## **2. Formas de Incluir JavaScript**

JavaScript se puede incluir en un proyecto de diferentes maneras, dependiendo de la organización y propósito del código.

### **2.1 Script Inline**

Se escribe directamente dentro de una etiqueta `<script>` en el archivo HTML.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Inline</title>
</head>
<body>
  <h1>Hola Mundo</h1>
  <script>
    alert("¡Hola desde JavaScript Inline!");
  </script>
</body>
</html>
```

---

### **2.2 Script en el `<head>`**

Se coloca el código JavaScript dentro de una etiqueta `<script>` en la sección `<head>` del documento HTML.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript en Head</title>
  <script>
    console.log("JavaScript cargado desde el Head");
  </script>
</head>
<body>
  <h1>Hola Mundo</h1>
</body>
</html>
```

**Nota:** Si el script interactúa con elementos HTML, usa el evento `DOMContentLoaded` para asegurar que la página se haya cargado completamente antes de ejecutar el código.

---

### **2.3 Script en el `<body>`**

Se coloca al final de la sección `<body>` para garantizar que los elementos HTML estén disponibles al momento de ejecutar el código.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript en Body</title>
</head>
<body>
  <h1>Hola Mundo</h1>
  <script>
    console.log("JavaScript cargado desde el Body");
  </script>
</body>
</html>
```

---

### **2.4 Script Externo**

Se utiliza un archivo separado con la extensión `.js`. Esto mejora la organización y reusabilidad del código.

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Externo</title>
  <script src="script.js" defer></script>
</head>
<body>
  <h1>Hola Mundo</h1>
</body>
</html>
```

### **script.js**
```javascript
console.log("JavaScript cargado desde un archivo externo.");
```

**Nota:** Usa el atributo `defer` para cargar el script después de que el HTML se haya procesado, o `async` para cargarlo en paralelo con el HTML.

---

### **Ventajas de Usar Archivos Externos**

1. **Organización:** Separa la estructura (`HTML`), estilos (`CSS`) y lógica (`JavaScript`).
2. **Reusabilidad:** Puedes usar el mismo archivo JavaScript en diferentes páginas.
3. **Mantenimiento:** Facilita la lectura y depuración del código.

---

### 🌐 Navegación

- --> Siguiente : [Templates de Strings y Backticks](Templates%20de%20Strings%20y%20Backticks.md)  