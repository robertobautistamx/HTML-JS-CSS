# **Transform y Outline en CSS**

En CSS, las propiedades **transform** y **outline** ofrecen formas de mejorar el diseño visual y funcionalidad de los elementos HTML. Transform se usa para modificar la apariencia y posición de un elemento, mientras que outline se utiliza para resaltar elementos.

---

## **1. Transform**

La propiedad **transform** permite aplicar transformaciones a los elementos, como rotación, escalado, traslación y distorsión.

### **Sintaxis de `transform`**

```css
transform: tipo-de-transformación(valor);
```

- **`tipo-de-transformación`**: Define la acción que se realizará (como `rotate`, `scale`, `translate`, etc.).
- **`valor`**: Especifica cuánto se aplicará la transformación (en grados, píxeles, etc.).

---

### **Rotar un Elemento (`rotate`)**

La función **`rotate`** gira un elemento alrededor de su punto central.

```css
.rotar {
  transform: rotate(45deg); /* Gira el elemento 45 grados */
}
```

- **`45deg`**: Especifica el ángulo de rotación en grados.  
  - Valores positivos: Rotación en sentido horario.  
  - Valores negativos: Rotación en sentido antihorario.

### **Usos Comunes de `rotate`**

1. **Botones Animados**: Crear efectos visuales en botones al hacer hover.
2. **Iconos**: Girar iconos para representar acción (como un icono de recarga).
3. **Relojes y Medidores**: Mover manecillas o indicadores en animaciones.

**Ejemplo Básico de Rotación:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Rotate</title>
  <style>
    .rotar {
      width: 100px;
      height: 100px;
      background-color: lightcoral;
      transform: rotate(30deg); /* Gira 30 grados */
    }
  </style>
</head>
<body>
  <div class="rotar"></div>
</body>
</html>
```

---

## **2. Outline**

La propiedad **outline** crea un borde resaltado alrededor de un elemento, pero con características diferentes al `border`.

### **Diferencias entre `outline` y `border`**

| **Propiedad**  | **Outline**                                                | **Border**                               |
|-----------------|-----------------------------------------------------------|------------------------------------------|
| **Posición**    | Se dibuja fuera del borde del elemento.                   | Forma parte del tamaño total del elemento. |
| **Espaciado**   | No afecta el espaciado interno ni externo.                | Afecta el tamaño del elemento (box model). |
| **Estilo**      | No admite esquinas redondeadas (`border-radius`).          | Admite bordes redondeados.                |
| **Uso común**   | Se utiliza para resaltar elementos (como al hacer focus). | Se utiliza para definir límites visuales. |

---

### **Declaración Básica de `outline`**

```css
.outline {
  outline: 2px solid red; /* Resaltador rojo */
}
```

- **`2px`**: Grosor del resaltador.  
- **`solid`**: Estilo del resaltador (puede ser `dashed`, `dotted`, etc.).  
- **`red`**: Color del resaltador.

---

### **Ejemplo Comparativo de `outline` y `border`**

**HTML:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Outline y Border</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="border">Border</div>
  <div class="outline">Outline</div>
</body>
</html>
```

**CSS:**

```css
.border {
  width: 200px;
  height: 100px;
  background-color: lightblue;
  border: 4px solid black; /* Agrega un borde */
}

.outline {
  width: 200px;
  height: 100px;
  background-color: lightgreen;
  outline: 4px solid red; /* Agrega un resaltador */
}
```

---

### 🌐 Navegación

- <-- Anterior: [Box y Text Shadow](Box%20y%20Text%20Shadow.md)  
- --> Siguiente: [Position's y Z-INDEX.md](Position's%20y%20Z-INDEX.md)  
