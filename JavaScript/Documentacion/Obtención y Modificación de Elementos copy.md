# **Obtención y Modificación de Elementos**

En JavaScript, se pueden obtener y modificar elementos HTML utilizando métodos del Document Object Model (DOM). Esto permite interactuar y alterar dinámicamente la estructura y apariencia de una página web.

---

## **19. Obtención y Modificación de Elementos**

### **Métodos para Obtener Elementos**

1. **`getElementById`**
   - Obtiene un elemento con un identificador específico.
   ```javascript
   const elemento = document.getElementById("miElemento");
   console.log(elemento); // Muestra el elemento en la consola
   ```

2. **`getElementsByClassName`**
   - Devuelve una colección de elementos que comparten una clase.
   ```javascript
   const elementos = document.getElementsByClassName("miClase");
   console.log(elementos); // HTMLCollection
   ```

3. **`getElementsByTagName`**
   - Obtiene todos los elementos de un tipo específico.
   ```javascript
   const parrafos = document.getElementsByTagName("p");
   console.log(parrafos); // HTMLCollection de párrafos
   ```

4. **`querySelector`**
   - Selecciona el primer elemento que coincide con un selector CSS.
   ```javascript
   const elemento = document.querySelector(".miClase");
   console.log(elemento);
   ```

5. **`querySelectorAll`**
   - Selecciona todos los elementos que coinciden con un selector CSS.
   ```javascript
   const elementos = document.querySelectorAll("p.miClase");
   console.log(elementos); // NodeList
   ```

---

### **Modificación de Elementos**

1. **Modificar el Contenido de Texto**
   - Usando `textContent`.
   ```javascript
   const elemento = document.getElementById("miElemento");
   elemento.textContent = "Nuevo contenido de texto";
   ```

2. **Modificar el Contenido HTML**
   - Usando `innerHTML`.
   ```javascript
   const elemento = document.getElementById("miElemento");
   elemento.innerHTML = "<strong>Nuevo contenido HTML</strong>";
   ```

3. **Modificar Atributos**
   - Usando `setAttribute`.
   ```javascript
   const imagen = document.querySelector("img");
   imagen.setAttribute("src", "nueva-imagen.jpg");
   ```

4. **Modificar Estilos**
   - Usando `style`.
   ```javascript
   const elemento = document.getElementById("miElemento");
   elemento.style.color = "blue";
   ```

---

## **20. Creación de Elementos**

JavaScript permite crear nuevos elementos HTML para insertarlos en la página.

### **Pasos para Crear e Insertar Elementos**

1. **Crear un Elemento**
   - Usando `document.createElement`.
   ```javascript
   const nuevoParrafo = document.createElement("p");
   nuevoParrafo.textContent = "Este es un nuevo párrafo";
   ```

2. **Añadir el Elemento al DOM**
   - Usando `appendChild` o `prepend`.
   ```javascript
   const contenedor = document.getElementById("contenedor");
   contenedor.appendChild(nuevoParrafo);
   ```

3. **Insertar Antes de un Elemento Específico**
   - Usando `insertBefore`.
   ```javascript
   const referencia = document.getElementById("referencia");
   contenedor.insertBefore(nuevoParrafo, referencia);
   ```

4. **Insertar con `innerHTML`**
   - Aunque no es recomendado para seguridad, puede usarse para agregar HTML.
   ```javascript
   const contenedor = document.getElementById("contenedor");
   contenedor.innerHTML += "<p>Otro párrafo creado</p>";
   ```

---

### **Ejemplo Completo**

### **HTML (`index.html`)**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Creación y Modificación de Elementos</title>
</head>
<body>
  <div id="contenedor">
    <p id="referencia">Párrafo existente</p>
  </div>
  <button id="boton">Añadir Párrafo</button>
  <script src="script.js"></script>
</body>
</html>
```

### **JavaScript (`script.js`)**
```javascript
// Obtener contenedor y botón
const contenedor = document.getElementById("contenedor");
const boton = document.getElementById("boton");

// Agregar evento al botón
boton.addEventListener("click", () => {
  // Crear un nuevo párrafo
  const nuevoParrafo = document.createElement("p");
  nuevoParrafo.textContent = "Este es un nuevo párrafo añadido dinámicamente";

  // Insertar antes del elemento de referencia
  const referencia = document.getElementById("referencia");
  contenedor.insertBefore(nuevoParrafo, referencia);
});
```

---

### 🌐 Navegación

- <-- Anterior : [Atributos Globales y Atributos de Input](Atributos%20Globales%20y%20Atributos%20de%20Input.md)  
- --> Siguiente : [Obtención y Modificación de Hijos, Padres y Hermanos](Obtencion%20y%20Modificacion%20de%20Childs.md)  