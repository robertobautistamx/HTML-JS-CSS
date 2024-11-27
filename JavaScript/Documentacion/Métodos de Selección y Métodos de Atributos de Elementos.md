# **Métodos de Selección y Métodos de Atributos de Elementos**

JavaScript ofrece una variedad de métodos para seleccionar elementos en el DOM, lo que nos permite manipular su contenido, atributos y estilo. A continuación, exploramos los métodos más comunes y sus aplicaciones.

---

## **16.1 Métodos de Selección**

### **1. `getElementById`**
Selecciona un elemento por su atributo `id`.

```javascript
const titulo = document.getElementById("titulo");
console.log(titulo.textContent); // Muestra el contenido del elemento con id="titulo"
```

### **2. `getElementsByClassName`**
Selecciona todos los elementos que comparten una misma clase.

```javascript
const items = document.getElementsByClassName("item");
console.log(items[0].textContent); // Muestra el contenido del primer elemento con la clase "item"
```

### **3. `getElementsByTagName`**
Selecciona todos los elementos de un tipo específico de etiqueta.

```javascript
const parrafos = document.getElementsByTagName("p");
console.log(parrafos.length); // Muestra cuántos elementos `<p>` hay en la página
```

### **4. `querySelector`**
Selecciona el primer elemento que coincida con un selector CSS.

```javascript
const primerItem = document.querySelector(".item");
console.log(primerItem.textContent); // Muestra el contenido del primer elemento con la clase "item"
```

### **5. `querySelectorAll`**
Selecciona todos los elementos que coincidan con un selector CSS, devolviendo un `NodeList`.

```javascript
const todosLosItems = document.querySelectorAll(".item");
todosLosItems.forEach((item) => {
  console.log(item.textContent); // Muestra el contenido de cada elemento con la clase "item"
});
```

---

## **16.2 Métodos de Atributos**

Los atributos de los elementos HTML pueden ser obtenidos, modificados o eliminados con JavaScript.

### **1. `getAttribute`**
Obtiene el valor de un atributo.

```javascript
const link = document.querySelector("a");
console.log(link.getAttribute("href")); // Muestra el valor del atributo "href"
```

### **2. `setAttribute`**
Establece o modifica el valor de un atributo.

```javascript
const boton = document.querySelector("button");
boton.setAttribute("disabled", "true"); // Desactiva el botón
```

### **3. `hasAttribute`**
Verifica si un elemento tiene un atributo específico.

```javascript
const imagen = document.querySelector("img");
console.log(imagen.hasAttribute("alt")); // Devuelve true si el atributo "alt" está presente
```

### **4. `removeAttribute`**
Elimina un atributo de un elemento.

```javascript
const input = document.querySelector("input");
input.removeAttribute("placeholder"); // Elimina el atributo "placeholder"
```

---

## **16.3 Ejemplo Completo**

### **HTML (`index.html`)**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Selección y Atributos</title>
</head>
<body>
  <h1 id="titulo">Título Principal</h1>
  <ul>
    <li class="item">Elemento 1</li>
    <li class="item">Elemento 2</li>
    <li class="item">Elemento 3</li>
  </ul>
  <a href="https://www.google.com" target="_blank">Ir a Google</a>
  <button id="boton">Haz clic aquí</button>
  <img src="imagen.jpg" alt="Descripción de la imagen">
  <script src="script.js"></script>
</body>
</html>
```

### **JavaScript (`script.js`)**

```javascript
// Selección
const titulo = document.getElementById("titulo");
const items = document.querySelectorAll(".item");
const link = document.querySelector("a");
const boton = document.getElementById("boton");
const imagen = document.querySelector("img");

// Modificación
titulo.textContent = "Nuevo Título";
items.forEach((item, index) => {
  item.textContent = `Nuevo Elemento ${index + 1}`;
});
link.setAttribute("href", "https://developer.mozilla.org/es/");

// Atributos
console.log(imagen.getAttribute("alt")); // Muestra "Descripción de la imagen"
boton.setAttribute("disabled", "true"); // Desactiva el botón
```

---

### 🌐 Navegación

- <-- Anterior : [El DOM (Document Object Model)](El%20DOM%20(Document%20Object%20Model).md)  
- --> Siguiente : [Atributos globales, atributos de input](Atributos%20globales,%20atributos%20de%20input.md)  