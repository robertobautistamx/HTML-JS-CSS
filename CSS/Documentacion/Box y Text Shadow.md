# **Box Shadow y Text Shadow en CSS**

CSS nos permite agregar sombras tanto a las cajas como al texto, lo que añade profundidad y mejora visual a los elementos.

---

## **1. Box Shadow**

El **box-shadow** agrega sombra alrededor de los bordes de un elemento en forma de caja.

### **Sintaxis de `box-shadow`**

```css
box-shadow: desplazamiento-x desplazamiento-y desenfoque extensión color;
```

- **`desplazamiento-x` y `desplazamiento-y`:**  
  Determinan el desplazamiento horizontal y vertical de la sombra.  
  - Valores positivos: sombra hacia la derecha y abajo.  
  - Valores negativos: sombra hacia la izquierda y arriba.

- **`desenfoque` (opcional):**  
  Define qué tan suave es el borde de la sombra.  
  - Valor más alto = sombra más difusa.  
  - Si se omite, la sombra tendrá bordes nítidos.

- **`extensión` (opcional):**  
  Ajusta el tamaño de la sombra.  
  - Valores positivos: agrandan la sombra.  
  - Valores negativos: encogen la sombra.

- **`color`:**  
  Define el color de la sombra. Puede usar valores en hexadecimales, RGB, HSL o palabras clave como `black`.

---

### **Ejemplo Básico**

```css
.caja {
  width: 200px;
  height: 100px;
  background-color: lightblue;
  box-shadow: 10px 10px 15px 5px rgba(0, 0, 0, 0.5); /* Sombra negra con transparencia */
}
```

- **`10px 10px`**: Desplaza la sombra hacia abajo y la derecha.  
- **`15px`**: Suaviza el borde.  
- **`5px`**: Extiende el tamaño de la sombra.  
- **`rgba(0, 0, 0, 0.5)`**: Sombra negra semitransparente.

---

### **Duplicar Sombras**

Puedes agregar múltiples sombras separándolas con comas:

```css
.caja {
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5), -5px -5px 10px rgba(0, 0, 255, 0.5);
}
```

- La primera sombra se desplaza hacia abajo/derecha y es negra.  
- La segunda sombra se desplaza hacia arriba/izquierda y es azul.

---

## **2. Text Shadow**

El **text-shadow** aplica sombras exclusivamente al texto.

### **Sintaxis de `text-shadow`**

```css
text-shadow: desplazamiento-x desplazamiento-y desenfoque color;
```

- **`desplazamiento-x` y `desplazamiento-y`:**  
  Similar a box-shadow, define la posición horizontal y vertical de la sombra.

- **`desenfoque` (opcional):**  
  Define el nivel de suavidad del borde.  

- **`color`:**  
  Establece el color de la sombra.

---

### **Ejemplo Básico**

```css
.texto {
  font-size: 24px;
  color: darkblue;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5); /* Sombra negra semitransparente */
}
```

- **`2px 2px`**: Desplaza la sombra hacia abajo/derecha.  
- **`5px`**: Suaviza el borde de la sombra.  
- **`rgba(0, 0, 0, 0.5)`**: Sombra negra semitransparente.

---

### **Duplicar Sombras de Texto**

Al igual que box-shadow, puedes agregar múltiples sombras separándolas con comas:

```css
.texto {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5), -2px -2px 3px rgba(255, 0, 0, 0.5);
}
```

- La primera sombra es negra y está desplazada abajo/derecha.  
- La segunda sombra es roja y está desplazada arriba/izquierda.

---

## **Ejemplo Completo**

**Archivo: `index.html`**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Shadow y Text Shadow</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="caja">Caja con sombra</div>
  <p class="texto">Texto con sombra</p>
</body>
</html>
```

**Archivo: `style.css`**

```css
.caja {
  width: 250px;
  height: 150px;
  background-color: lightcoral;
  box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.3), -5px -5px 15px rgba(0, 0, 255, 0.3);
}

.texto {
  font-size: 30px;
  color: navy;
  text-shadow: 4px 4px 8px rgba(0, 0, 0, 0.6), -2px -2px 6px rgba(255, 0, 0, 0.4);
}
```

---

## 🌐 Navegación

- <-- Anterior: [Box Model](Box%20Model.md)
- --> Siguiente: [Transformaciones y Rotaciones](Transform%20y%20Outline.md)  
