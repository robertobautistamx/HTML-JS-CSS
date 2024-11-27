# **El DOM (Document Object Model)**

El DOM (Document Object Model) es una interfaz de programación que representa la estructura de un documento HTML o XML como un árbol jerárquico de nodos. Esto permite que JavaScript interactúe y modifique el contenido, estructura y estilo de la página.

---

## **15.1 Introducción al DOM**

El DOM convierte el documento HTML en una estructura navegable y manipulable:

1. **HTML Original**:
   ```html
   <html>
     <body>
       <h1>Bienvenido</h1>
       <p>Este es un párrafo.</p>
     </body>
   </html>
   ```

2. **Estructura del DOM**:
   ```
   - Document
     - html
       - head
       - body
         - h1
         - p
   ```

### **Partes del DOM**

- **Nodo**: Cada elemento HTML, atributo o texto es un nodo.
- **Elemento**: Representa las etiquetas HTML (por ejemplo, `<div>`, `<p>`).
- **Atributo**: Propiedades como `class` o `id`.
- **Texto**: Contenido dentro de las etiquetas HTML.

---

## **15.2 ¿Por qué es importante el DOM?**

- **Interacción Dinámica**: Permite modificar el contenido y los estilos de una página después de que se haya cargado.
- **Eventos**: Permite escuchar y responder a acciones del usuario (clics, teclas, etc.).
- **Accesibilidad**: Ayuda a mejorar la experiencia del usuario mediante ajustes dinámicos.

---

## **15.3 Métodos Básicos para Interactuar con el DOM**

### **Acceso al DOM**

1. **`document`**:
   - Representa el documento HTML completo.
   - Ejemplo:
     ```javascript
     console.log(document.title); // Obtiene el título de la página
     ```

2. **`window`**:
   - Representa la ventana del navegador.
   - Ejemplo:
     ```javascript
     console.log(window.innerWidth); // Ancho de la ventana
     ```

---

## **15.4 Manipulación Básica del DOM**

### **Cambiar Contenido de Texto**

```javascript
document.querySelector("h1").textContent = "Nuevo Título";
```

### **Cambiar Estilos**

```javascript
document.querySelector("p").style.color = "blue";
```

### **Agregar un Elemento**

```javascript
const nuevoParrafo = document.createElement("p");
nuevoParrafo.textContent = "Este es un nuevo párrafo.";
document.body.appendChild(nuevoParrafo);
```

### **Eliminar un Elemento**

```javascript
const elementoAEliminar = document.querySelector("h1");
elementoAEliminar.remove();
```

---

## **15.5 Ejemplo Completo**

### **HTML (`index.html`)**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo del DOM</title>
</head>
<body>
  <h1 id="titulo">Título Original</h1>
  <p class="texto">Este es un párrafo.</p>
  <button id="cambiarTitulo">Cambiar Título</button>
</body>
</html>
```

### **JavaScript (`script.js`)**
```javascript
document.getElementById("cambiarTitulo").addEventListener("click", () => {
  const titulo = document.getElementById("titulo");
  titulo.textContent = "Título Modificado";
  titulo.style.color = "red";
});
```

En este ejemplo:
- Al hacer clic en el botón, el texto del título cambia a "Título Modificado".
- El color del título se cambia a rojo.

---

### 🌐 Navegación

- <-- Anterior : [Console (Consola de JavaScript)](Console%20(Consola%20de%20JavaScript).md)  
- --> Siguiente : [Métodos de Selección y Métodos de Atributos de Elementos](Metodos%20de%20Seleccion%20y%20metodos%20de%20atributos%20de%20elementos%20y%20un%20elemento.md)  