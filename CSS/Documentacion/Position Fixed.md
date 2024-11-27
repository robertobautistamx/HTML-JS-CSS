## **Position Fixed**

La propiedad `position: fixed;` permite fijar un elemento en una posición específica de la ventana del navegador. Esto significa que el elemento no se moverá al hacer scroll en la página. Es útil para elementos como menús de navegación, botones de acción o anuncios.

---

### **Características Principales**

1. **Permanente en la Pantalla:**
   - Un elemento con `position: fixed` no se mueve al desplazarse por la página. Su posición es relativa al área visible del navegador.

2. **Referencia de Posicionamiento:**
   - Los valores `top`, `right`, `bottom`, y `left` se usan para ubicar el elemento dentro de la ventana.

3. **Ejemplo Común:**
   - Navegación fija en la parte superior de la pantalla.

---

### **Ejemplo: Navegación Fija con `position: fixed`**

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Navegación Fija</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <nav>
    <ul>
      <li class="list-nav"><a href="#">Inicio</a></li>
      <li class="list-nav"><a href="#">Servicios</a></li>
      <li class="list-nav"><a href="#">Contacto</a></li>
    </ul>
  </nav>
  <p class="container">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam numquam amet eaque labore eligendi doloremque harum quasi consectetur explicabo distinctio dolor ad ut, non deserunt animi asperiores. Ab, rerum iste...
    (Agrega aquí texto suficiente para probar el desplazamiento con scroll)
  </p>
</body>
</html>
```

---

### **style.css**

```css
/* Aplicar estilo general */
* {
  font-family: "Roboto", sans-serif;
}

body {
  padding-top: 50px; /* Espacio para que el contenido no se superponga con la navegación fija */
}

/* Estilo de la navegación fija */
nav {
  position: fixed;
  top: 0; /* Fijar en la parte superior */
  width: 100%; /* Ancho completo */
  background-color: red; /* Color de fondo */
  z-index: 10; /* Asegurar que esté por encima del contenido */
}

/* Estilo de las listas en la navegación */
.list-nav {
  display: inline-block;
  list-style-type: none;
  margin: 0 15px;
}

.list-nav a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}
```

---

### **Explicación del Ejemplo**

1. **Navegación Fija (`nav`):**
   - Se usa `position: fixed;` para mantener el menú en la parte superior de la ventana.
   - `top: 0;` asegura que esté pegado al borde superior.
   - `z-index: 10;` asegura que el menú quede por encima del resto del contenido.

2. **Separación del Contenido:**
   - `padding-top: 50px;` en el `<body>` evita que el contenido se superponga con el menú fijo.

3. **Estilo de los Enlaces:**
   - Los elementos de la lista (`<li>`) están alineados horizontalmente con `display: inline-block;`.
   - Los enlaces (`<a>`) tienen un diseño limpio sin subrayados ni colores predeterminados.

---

### 🌐 Navegación

- <-- Anterior : [Position Absolute](Position%20Absolute.md)
- --> Siguiente : [Position Sticky](Position%20Sticky.md)
