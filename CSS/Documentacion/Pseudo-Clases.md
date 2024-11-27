# **Pseudo-Clases en CSS**

Las **pseudo-clases** permiten aplicar estilos a los elementos HTML en función de su estado o interacción con el usuario. Son herramientas esenciales para crear diseños interactivos y dinámicos, mejorando la experiencia del usuario.

---

## **1. `:hover`**

### **Descripción:**
La pseudo-clase `:hover` aplica estilos a un elemento cuando el usuario posiciona el cursor sobre él.

### **Usos Comunes:**
- Resaltar enlaces o botones cuando el usuario los apunta con el cursor.
- Crear efectos visuales en elementos interactivos.

### **Ejemplo:**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>:hover</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <button class="boton-hover">Pasa el mouse aquí</button>
</body>
</html>
```

### **style.css**
```css
.boton-hover {
  background-color: lightblue;
  color: black;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
}

.boton-hover:hover {
  background-color: darkblue;
  color: white;
}
```

### **Resultado:**
El botón cambiará de color cuando el cursor pase sobre él.

---

## **2. `:link` y `:visited`**

### **Descripción:**
- **`:link`**: Aplica estilos a enlaces que aún no han sido visitados por el usuario.
- **`:visited`**: Aplica estilos a enlaces que ya han sido visitados.

### **Usos Comunes:**
- Diferenciar visualmente entre enlaces visitados y no visitados.

### **Ejemplo:**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>:link y :visited</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <a href="https://www.google.com" class="enlace">Ir a Google</a>
</body>
</html>
```

### **style.css**
```css
.enlace:link {
  color: blue;
  text-decoration: none;
}

.enlace:visited {
  color: purple;
}
```

### **Resultado:**
El enlace aparecerá en azul si no ha sido visitado y cambiará a morado después de que el usuario haga clic en él.

---

## **3. `:active`**

### **Descripción:**
La pseudo-clase `:active` aplica estilos a un elemento en el momento en que el usuario hace clic sobre él.

### **Usos Comunes:**
- Cambiar el aspecto de botones o enlaces mientras se están presionando.

### **Ejemplo:**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>:active</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <button class="boton-activo">Haz clic aquí</button>
</body>
</html>
```

### **style.css**
```css
.boton-activo {
  background-color: lightgreen;
  color: black;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
}

.boton-activo:active {
  background-color: darkgreen;
  color: white;
  transform: scale(0.95); /* Efecto de "presionar" */
}
```

### **Resultado:**
El botón cambiará de color y tamaño mientras está siendo presionado.

---

## **4. `:focus`**

### **Descripción:**
La pseudo-clase `:focus` aplica estilos a un elemento cuando está enfocado, generalmente al usar el teclado o después de hacer clic en él.

### **Usos Comunes:**
- Resaltar campos de formulario al ser seleccionados.
- Mejorar la accesibilidad al proporcionar retroalimentación visual para usuarios que navegan con teclado.

### **Ejemplo:**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>:focus</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <input type="text" class="campo-focus" placeholder="Escribe aquí...">
</body>
</html>
```

### **style.css**
```css
.campo-focus {
  border: 2px solid gray;
  padding: 5px;
  outline: none;
}

.campo-focus:focus {
  border: 2px solid blue;
  background-color: lightblue;
}
```

### **Resultado:**
El campo de texto cambiará su borde y color de fondo cuando sea seleccionado.

---

## **Combinación de Pseudo-Clases**

Puedes combinar pseudo-clases para crear comportamientos dinámicos y visuales más complejos. Por ejemplo:

### **Ejemplo Combinado**
```css
.enlace:link:hover {
  color: orange;
  text-decoration: underline;
}

.enlace:visited:hover {
  color: red;
  text-decoration: line-through;
}
```

---

### 🌐 Navegación

- <-- Anterior : [Pseudo-Elementos](Pseudo-Elementos.md)
- --> Siguiente : [Animaciones Básicas](Animaciones%20Básicas.md)
