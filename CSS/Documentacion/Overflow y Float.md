# **Overflow y Float en CSS**

CSS ofrece propiedades como `overflow` y `float` que controlan cómo se muestra el contenido cuando excede los límites de un contenedor y cómo se posicionan elementos como imágenes o texto dentro del flujo del documento.

---

## **1. Overflow**

La propiedad `overflow` controla qué sucede cuando el contenido de un elemento se desborda de su contenedor.

### **Valores Comunes de `overflow`:**

1. **`visible` (por defecto):** 
   - El contenido que excede los límites del contenedor será visible.

   ```css
   .visible {
     overflow: visible;
     background-color: lightblue;
     width: 200px;
     height: 100px;
   }
   ```

2. **`hidden`:**
   - Oculta cualquier contenido que exceda los límites del contenedor.

   ```css
   .hidden {
     overflow: hidden;
     background-color: lightcoral;
     width: 200px;
     height: 100px;
   }
   ```

3. **`scroll`:**
   - Fuerza la aparición de barras de desplazamiento, independientemente de si el contenido excede el contenedor.

   ```css
   .scroll {
     overflow: scroll;
     background-color: lightgreen;
     width: 200px;
     height: 100px;
   }
   ```

4. **`auto`:**
   - Muestra barras de desplazamiento solo si el contenido se desborda.

   ```css
   .auto {
     overflow: auto;
     background-color: lightgoldenrodyellow;
     width: 200px;
     height: 100px;
   }
   ```

### **Direcciones Específicas:**
- **`overflow-x`**: Controla el desbordamiento horizontal.
- **`overflow-y`**: Controla el desbordamiento vertical.

---

### **Ejemplo de Overflow**

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Overflow</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="visible">Contenido visible que excede el contenedor</div>
  <div class="hidden">Contenido oculto que excede el contenedor</div>
  <div class="scroll">Contenido con barra de scroll</div>
  <div class="auto">Contenido con scroll automático</div>
</body>
</html>
```

### **style.css**

```css
div {
  margin: 10px 0;
  padding: 10px;
  border: 1px solid black;
}
.visible {
  overflow: visible;
  background-color: lightblue;
  width: 200px;
  height: 100px;
}
.hidden {
  overflow: hidden;
  background-color: lightcoral;
  width: 200px;
  height: 100px;
}
.scroll {
  overflow: scroll;
  background-color: lightgreen;
  width: 200px;
  height: 100px;
}
.auto {
  overflow: auto;
  background-color: lightgoldenrodyellow;
  width: 200px;
  height: 100px;
}
```

---

## **2. Float**

La propiedad `float` permite posicionar elementos, como imágenes, dentro de un contenedor para que el texto fluya a su alrededor.

### **Valores Comunes de `float`:**
1. **`left`:** Coloca el elemento flotante a la izquierda.
2. **`right`:** Coloca el elemento flotante a la derecha.
3. **`none` (por defecto):** El elemento no flota y se comporta normalmente.

---

### **Ejemplo de Float con Imágenes**

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Float</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <img src="example.jpg" alt="Imagen flotante" class="float-left">
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas commodo lacus sit amet libero venenatis, 
      non blandit lorem venenatis. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
    </p>
  </div>
</body>
</html>
```

### **style.css**

```css
.container {
  width: 80%;
  margin: 0 auto;
  line-height: 1.6;
}

.float-left {
  float: left;
  margin-right: 10px;
  width: 150px;
}

p {
  text-align: justify;
}
```

---

## **Combinación de Overflow y Float**

Puedes usar ambas propiedades juntas para crear efectos avanzados. Por ejemplo, fijar una imagen flotante dentro de un contenedor con overflow.

```css
.container {
  overflow: hidden; /* Asegura que los elementos flotantes no afecten el contenedor */
}

.float-left {
  float: left;
  margin-right: 10px;
}
```

---

## **Aplicaciones Comunes**

1. **Overflow:**
   - Barras de scroll en tablas largas o imágenes grandes.
   - Control de contenido desbordante en layouts responsivos.

2. **Float:**
   - Posicionar imágenes junto al texto.
   - Crear layouts básicos antes de flexbox o grid.

---

### 🌐 Navegación

- <-- Anterior : [Display](Display.md)
- --> Siguiente : [Pseudo-Elementos](Pseudo-Elementos.md)
  
