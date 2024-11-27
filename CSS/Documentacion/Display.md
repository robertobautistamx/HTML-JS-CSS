# **Display en CSS**

La propiedad `display` en CSS define cómo un elemento se comporta visualmente en el flujo del documento. Determina si un elemento se muestra como un bloque, en línea, o en otros modelos más avanzados como `flex` o `grid`.

---

## **1. Display: Block**

Un elemento con `display: block` ocupa todo el ancho disponible, comenzando en una nueva línea. Por defecto, etiquetas como `<div>`, `<h1>`, y `<p>` son de tipo block.

### **Características**

- Ocupa toda la línea.
- Puede tener propiedades como `width`, `height`, `margin`, y `padding`.

### **Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Block</title>
  <style>
    .block {
      display: block;
      background-color: lightblue;
      margin: 10px 0;
      padding: 10px;
    }
  </style>
</head>
<body>
  <div class="block">Soy un elemento block</div>
  <div class="block">Ocupo todo el ancho disponible</div>
</body>
</html>
```

---

## **2. Display: Inline**

Un elemento con `display: inline` no comienza en una nueva línea y solo ocupa el espacio necesario para su contenido. Por defecto, etiquetas como `<span>`, `<a>`, y `<strong>` son de tipo inline.

### **Características**

- No acepta propiedades como `width` o `height`.
- Se comporta como parte del flujo de texto.

### **Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Inline</title>
  <style>
    .inline {
      display: inline;
      background-color: lightcoral;
      padding: 5px;
    }
  </style>
</head>
<body>
  <p>
    Este es un texto con <span class="inline">elementos</span> en línea.
  </p>
</body>
</html>
```

---

## **3. Display: Inline-Block**

`display: inline-block` combina características de `inline` y `block`. Permite que un elemento se comporte como un bloque pero que esté en línea con otros elementos.

### **Características**

- Acepta `width` y `height`.
- Permite alinear múltiples elementos en una línea.

### **Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Inline-Block</title>
  <style>
    .inline-block {
      display: inline-block;
      background-color: lightgreen;
      width: 100px;
      height: 50px;
      margin: 5px;
      text-align: center;
      line-height: 50px;
    }
  </style>
</head>
<body>
  <div class="inline-block">1</div>
  <div class="inline-block">2</div>
  <div class="inline-block">3</div>
</body>
</html>
```

---

## **4. Display: Flex**

`display: flex` permite al contenedor organizar a sus hijos de manera flexible, distribuyendo el espacio de manera eficiente.

### **Características**

- Se utiliza para alineación y distribución de elementos.
- Ejes principales: horizontal (`flex-direction: row;`) y vertical (`flex-direction: column;`).

### **Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Flex</title>
  <style>
    .flex-container {
      display: flex;
      justify-content: space-around;
      align-items: center;
      height: 100px;
      background-color: lightgray;
    }
    .flex-item {
      background-color: skyblue;
      padding: 10px;
    }
  </style>
</head>
<body>
  <div class="flex-container">
    <div class="flex-item">A</div>
    <div class="flex-item">B</div>
    <div class="flex-item">C</div>
  </div>
</body>
</html>
```

---

## **5. Display: Grid**

`display: grid` organiza elementos en filas y columnas, permitiendo un diseño estructurado y flexible.

### **Características**

- Divide el espacio en una cuadrícula.
- Define filas y columnas con `grid-template-rows` y `grid-template-columns`.

### **Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Grid</title>
  <style>
    .grid-container {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 10px;
      background-color: lightgray;
      padding: 10px;
    }
    .grid-item {
      background-color: peachpuff;
      padding: 20px;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
    <div class="grid-item">4</div>
    <div class="grid-item">5</div>
    <div class="grid-item">6</div>
  </div>
</body>
</html>
```

---

## **6. Display: Inline-Flex**

`display: inline-flex` funciona como `flex`, pero el contenedor se comporta como un elemento `inline`.

### **Ejemplo**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Inline-Flex</title>
  <style>
    .inline-flex-container {
      display: inline-flex;
      background-color: lightgray;
      padding: 10px;
    }
    .inline-flex-item {
      background-color: lightseagreen;
      margin: 5px;
      padding: 10px;
      color: white;
    }
  </style>
</head>
<body>
  <div class="inline-flex-container">
    <div class="inline-flex-item">A</div>
    <div class="inline-flex-item">B</div>
    <div class="inline-flex-item">C</div>
  </div>
</body>
</html>
```

---

### 🌐 Navegación

- <-- Anterior : [Position Sticky](Position%20Sticky.md)
- --> Siguiente : [Overflow y Float](Overflow%20y%20Float.md)
  
