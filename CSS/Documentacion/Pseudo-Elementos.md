# **Pseudo-Elementos en CSS**

Los **pseudo-elementos** en CSS permiten aplicar estilos a partes específicas de un elemento, como texto o contenido antes o después de un elemento, sin modificar directamente el HTML. Son especialmente útiles en el diseño responsivo, ya que no ocupan espacio real y se adaptan al tamaño del contenedor.

---

## **Características Clave de los Pseudo-Elementos**

1. Permiten seleccionar partes específicas del contenido.
2. No ocupan espacio real dentro del flujo del documento.
3. Funcionan en todos los tipos de `display` excepto en `inline`.

---

## **1. Pseudo-Elementos Comunes**

### **1.1 `::placeholder`**

Aplica estilos al texto de marcador de posición en campos de entrada (`<input>` y `<textarea>`).

**Ejemplo:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>::placeholder</title>
  <style>
    input::placeholder {
      color: gray;
      font-style: italic;
    }
  </style>
</head>
<body>
  <input type="text" placeholder="Escribe tu nombre...">
</body>
</html>
```

---

### **1.2 `::selection`**

Aplica estilos al texto seleccionado por el usuario.

**Ejemplo:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>::selection</title>
  <style>
    ::selection {
      background-color: lightblue;
      color: white;
    }
  </style>
</head>
<body>
  <p>Selecciona este texto para ver el efecto de estilo aplicado.</p>
</body>
</html>
```

---

## **2. `::before` y `::after`**

Estos pseudo-elementos se utilizan para insertar contenido antes (`::before`) o después (`::after`) de un elemento.

### **Usos Comunes:**
- Añadir iconos, decoraciones o texto adicional.
- Crear efectos visuales sin alterar el HTML.
- Facilitar el diseño responsivo.

### **Ejemplo:**

Este ejemplo muestra cómo usar `::before` para un bloque rojo y `::after` para un bloque verde.

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>::before y ::after</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="contenedor">Contenido principal</div>
</body>
</html>
```

### **style.css**

```css
.contenedor {
  background-color: lightgray;
  padding: 20px;
  text-align: center;
  position: relative;
}

.contenedor::before {
  content: "";
  display: block;
  width: 50px;
  height: 50px;
  background-color: red;
  position: absolute;
  top: -10px;
  left: -10px;
}

.contenedor::after {
  content: "";
  display: block;
  width: 50px;
  height: 50px;
  background-color: green;
  position: absolute;
  bottom: -10px;
  right: -10px;
}
```

---

## **Importancia en el Diseño Responsivo**

1. **Flexibilidad Visual:**
   - Los pseudo-elementos se adaptan al tamaño del contenedor, lo que facilita la creación de diseños responsivos sin agregar elementos extra al HTML.

2. **Optimización de Recursos:**
   - Al no ocupar espacio real, ayudan a reducir el impacto en el flujo del documento.

3. **Estética Dinámica:**
   - Permiten agregar decoraciones, indicadores o efectos de selección personalizados, mejorando la experiencia del usuario.

---

### 🌐 Navegación

- <-- Anterior : [Overflow y Float](Overflow%20y%20Float.md)
- --> Siguiente : [Pseudo-Clases](Pseudo-Clases.md)
