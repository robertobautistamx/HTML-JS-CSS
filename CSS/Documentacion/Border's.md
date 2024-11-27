# **Bordes en CSS**

Los bordes (`border`) en CSS son las líneas que rodean un elemento y se pueden personalizar con diferentes estilos, grosores y colores.

---

## **1. Estructura Básica de los Bordes**

Un borde en CSS se define con la propiedad `border`, que incluye tres atributos principales:

1. **Ancho del borde (`border-width`)**: Define el grosor del borde.
2. **Estilo del borde (`border-style`)**: Define cómo se verá el borde (sólido, punteado, etc.).
3. **Color del borde (`border-color`)**: Define el color del borde.

```css
.caja {
  border: 2px solid black; /* Borde sólido negro de 2px */
}
```

---

## **2. Tipos de Bordes (`border-style`)**

### **1. `solid` (Sólido)**

Un borde completamente sólido.

```css
.caja-solid {
  border: 3px solid black;
}
```

### **2. `dashed` (Punteado)**

Un borde compuesto de líneas discontinuas.

```css
.caja-dashed {
  border: 3px dashed black;
}
```

### **3. `dotted` (Punteado circular)**

Un borde compuesto de puntos.

```css
.caja-dotted {
  border: 3px dotted black;
}
```

### **4. `double` (Doble línea)**

Un borde con dos líneas paralelas. El espacio entre líneas depende del grosor del borde.

```css
.caja-double {
  border: 6px double black;
}
```

### **5. `outset`**

El borde parece levantado, dando un efecto 3D.

```css
.caja-outset {
  border: 3px outset black;
}
```

### **6. `ridge`**

Similar a `outset`, pero con un efecto más definido.

```css
.caja-ridge {
  border: 3px ridge black;
}
```

### **7. `none` (Sin borde)**

Quita completamente el borde.

```css
.caja-none {
  border: none;
}
```

---

## **3. Atributos del Borde**

### **Ancho del Borde (`border-width`)**

Define el grosor del borde:

```css
.caja-border-width {
  border-width: 5px; /* Grosor del borde */
  border-style: solid; /* Estilo necesario para que el borde sea visible */
  border-color: black; /* Color del borde */
}
```

### **Estilo del Borde (`border-style`)**

Define el estilo del borde, como se explicó en la sección anterior.

### **Color del Borde (`border-color`)**

Define el color del borde:

```css
.caja-border-color {
  border: 2px solid;
  border-color: red; /* Color del borde */
}
```

---

## **4. Aplicación a Lados Específicos**

Puedes aplicar bordes a lados específicos con las propiedades:

- `border-top`
- `border-right`
- `border-bottom`
- `border-left`

```css
.caja-bordes-independientes {
  border-top: 3px solid red;    /* Borde superior */
  border-right: 3px dashed blue; /* Borde derecho */
  border-bottom: 3px dotted green; /* Borde inferior */
  border-left: 3px double black; /* Borde izquierdo */
}
```

---

## **Ejemplo Completo**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bordes en CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="caja caja-solid">Borde Sólido</div>
  <div class="caja caja-dashed">Borde Discontinuo</div>
  <div class="caja caja-dotted">Borde Punteado</div>
  <div class="caja caja-double">Borde Doble</div>
  <div class="caja caja-outset">Borde Outset</div>
  <div class="caja caja-ridge">Borde Ridge</div>
  <div class="caja caja-bordes-independientes">Bordes Independientes</div>
</body>
</html>
```

---

### **style.css**
```css
.caja {
  width: 200px;
  height: 100px;
  margin: 10px;
  padding: 10px;
  text-align: center;
  font-family: Arial, sans-serif;
}

.caja-solid {
  border: 3px solid black;
}

.caja-dashed {
  border: 3px dashed black;
}

.caja-dotted {
  border: 3px dotted black;
}

.caja-double {
  border: 6px double black;
}

.caja-outset {
  border: 3px outset black;
}

.caja-ridge {
  border: 3px ridge black;
}

.caja-bordes-independientes {
  border-top: 3px solid red;
  border-right: 3px dashed blue;
  border-bottom: 3px dotted green;
  border-left: 3px double black;
}
``` 

---

## **Tabla de Tipos de Bordes**

| **Tipo de Borde**  | **Descripción**                                        |
|--------------------|-------------------------------------------------------|
| `solid`            | Línea sólida.                                         |
| `dashed`           | Línea discontinua.                                    |
| `dotted`           | Línea de puntos.                                      |
| `double`           | Dos líneas paralelas.                                 |
| `outset`           | Borde con efecto levantado en 3D.                     |
| `ridge`            | Borde con efecto 3D más definido.                     |
| `none`             | Sin borde visible.                                    |

---

### 🌐 Navegación

- <-- Anterior : [Propiedades de las Cajas](Propiedades%20de%20las%20cajas.md)
- --> Siguiente : [Box Model](Box%20Model.md)
