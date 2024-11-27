## **Position Absolute**

La propiedad `position: absolute;` permite que un elemento se posicione de manera precisa dentro de su contenedor de referencia más cercano con una posición definida (`relative`, `absolute`, `fixed`, o `sticky`). Si no hay un contenedor posicionado, se tomará el elemento raíz (`<html>`) como referencia.

### **Características Principales**

1. **Espacio No Reservado:** El elemento deja de ocupar el espacio en el flujo del documento.
2. **Referencias con `top`, `right`, `bottom` y `left`:** Se utilizan para posicionar el elemento en su contenedor de referencia.
3. **Flexibilidad Visual:** El elemento puede superponerse fácilmente sobre otros.

---

### **Ejemplo: Contenedor con 4 Esquinas y una Caja al Centro**

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Position Absolute</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="contenedor">
    <div class="esquina esquina1">Esquina 1</div>
    <div class="esquina esquina2">Esquina 2</div>
    <div class="esquina esquina3">Esquina 3</div>
    <div class="esquina esquina4">Esquina 4</div>
    <div class="centro">Centro</div>
  </div>
</body>
</html>
```

---

### **style.css**

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f5f5f5;
}

.contenedor {
  position: relative;
  width: 300px;
  height: 300px;
  background-color: #e0e0e0;
  border: 2px solid #ccc;
}

.esquina {
  position: absolute;
  width: 50px;
  height: 50px;
  background-color: #8bc34a;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12px;
}

.esquina1 {
  top: 0;
  left: 0;
}

.esquina2 {
  top: 0;
  right: 0;
}

.esquina3 {
  bottom: 0;
  left: 0;
}

.esquina4 {
  bottom: 0;
  right: 0;
}

.centro {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100px;
  height: 100px;
  background-color: #03a9f4;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 14px;
  transform: translate(-50%, -50%);
}
```

---

### **Descripción del Ejemplo**

1. **Esquinas (`.esquina`):**
   - Cada esquina de la caja contenedora tiene una caja posicionada con `top` y `left/right` según corresponda.
   - Los valores de `top`, `bottom`, `left` y `right` son utilizados para definir su posición dentro del contenedor.

2. **Centro (`.centro`):**
   - Posicionado en el centro absoluto del contenedor utilizando `top: 50%;` y `left: 50%;`.
   - La propiedad `transform: translate(-50%, -50%);` ajusta el punto de referencia al centro del elemento en lugar de su esquina superior izquierda.

---

### 🌐 Navegación

- <-- Anterior : [Position Relative](Position%20Relative.md)
- --> Siguiente : [Position Fixed](Position%20Fixed.md)
  
