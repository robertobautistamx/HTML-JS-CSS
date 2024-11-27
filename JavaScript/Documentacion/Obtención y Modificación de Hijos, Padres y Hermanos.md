# **Obtención y Modificación de Hijos, Padres y Hermanos**

En esta sección aprenderemos cómo interactuar con los elementos relacionados entre sí en el DOM, como los hijos, padres y hermanos de un elemento. También exploraremos la propiedad de nodos para comprender mejor la estructura del árbol del DOM.

---

## **21. Obtención y Modificación de Hijos (`Childs`)**

Los hijos son los elementos anidados directamente dentro de un contenedor en el DOM.

### **Propiedades y Métodos Comunes**

1. **`children`**
   - Devuelve una colección HTML de los elementos hijos.
   ```javascript
   const contenedor = document.getElementById("contenedor");
   console.log(contenedor.children); // Colección de hijos
   ```

2. **`firstElementChild`**
   - Obtiene el primer elemento hijo.
   ```javascript
   const primerHijo = contenedor.firstElementChild;
   console.log(primerHijo);
   ```

3. **`lastElementChild`**
   - Obtiene el último elemento hijo.
   ```javascript
   const ultimoHijo = contenedor.lastElementChild;
   console.log(ultimoHijo);
   ```

4. **`childElementCount`**
   - Cuenta el número de hijos directos.
   ```javascript
   console.log(contenedor.childElementCount); // Número de hijos
   ```

### **Ejemplo**
```html
<div id="contenedor">
  <p>Primer Hijo</p>
  <p>Segundo Hijo</p>
  <p>Tercer Hijo</p>
</div>
<script>
  const contenedor = document.getElementById("contenedor");
  console.log(contenedor.children); // Devuelve todos los hijos
</script>
```

---

## **22. Propiedades de Padres (`Parents`)**

Los padres son los elementos que contienen a otros elementos en el DOM.

### **Propiedades y Métodos Comunes**

1. **`parentElement`**
   - Devuelve el elemento padre del actual.
   ```javascript
   const hijo = document.querySelector("p");
   console.log(hijo.parentElement); // Elemento contenedor
   ```

2. **`closest(selector)`**
   - Busca el ancestro más cercano que coincide con un selector.
   ```javascript
   const hijo = document.querySelector("p");
   console.log(hijo.closest("div")); // Devuelve el padre más cercano
   ```

### **Ejemplo**
```html
<div id="padre">
  <p>Hijo</p>
</div>
<script>
  const hijo = document.querySelector("p");
  console.log(hijo.parentElement); // Devuelve el div con id "padre"
</script>
```

---

## **23. Propiedades de Hermanos (`Siblings`)**

Los hermanos son elementos que comparten el mismo padre.

### **Propiedades y Métodos Comunes**

1. **`nextElementSibling`**
   - Devuelve el siguiente hermano elemento.
   ```javascript
   const primerHijo = document.querySelector("p");
   console.log(primerHijo.nextElementSibling); // Segundo hijo
   ```

2. **`previousElementSibling`**
   - Devuelve el hermano elemento anterior.
   ```javascript
   const segundoHijo = document.querySelectorAll("p")[1];
   console.log(segundoHijo.previousElementSibling); // Primer hijo
   ```

### **Ejemplo**
```html
<div id="contenedor">
  <p>Primer Hijo</p>
  <p>Segundo Hijo</p>
  <p>Tercer Hijo</p>
</div>
<script>
  const primerHijo = document.querySelector("p");
  console.log(primerHijo.nextElementSibling); // Devuelve el segundo hijo
</script>
```

---

## **24. Nodos: Una Propiedad Extra**

El DOM no solo incluye elementos, sino también nodos como texto y comentarios.

### **Propiedades Comunes**

1. **`childNodes`**
   - Devuelve todos los nodos hijos, incluidos texto y comentarios.
   ```javascript
   const contenedor = document.getElementById("contenedor");
   console.log(contenedor.childNodes); // Incluye nodos de texto
   ```

2. **`nodeType`**
   - Devuelve el tipo de nodo.
     - `1` para elementos.
     - `3` para texto.
     - `8` para comentarios.
   ```javascript
   const nodo = document.querySelector("p");
   console.log(nodo.nodeType); // Tipo de nodo
   ```

3. **`nodeName`**
   - Devuelve el nombre del nodo.
   ```javascript
   const nodo = document.querySelector("p");
   console.log(nodo.nodeName); // Nombre del nodo
   ```

### **Ejemplo**
```html
<div id="contenedor">
  <p>Texto con un nodo</p>
  <!-- Comentario -->
</div>
<script>
  const contenedor = document.getElementById("contenedor");
  console.log(contenedor.childNodes); // Incluye texto y comentarios
</script>
```

---

### 🌐 Navegación

- <-- Anterior : [Obtención y Modificación de Elementos](Obtencion%20y%20Modificacion%20de%20Elementos.md)  
- --> Siguiente : [](.md)  