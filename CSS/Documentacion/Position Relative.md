# **Position: Relative**

`position: relative` es una propiedad en CSS que permite posicionar un elemento respecto a su posición original en el flujo del documento. A diferencia de otras posiciones, mantiene su espacio en el diseño y no afecta el posicionamiento de los elementos cercanos, pero el contenido dentro de la caja puede moverse de forma controlada.

---

## **Características Clave de `position: relative`**

1. **Conserva su Espacio Original:**
   - Aunque el elemento se mueva visualmente, su espacio original en el flujo del documento sigue estando reservado.
   - Los elementos vecinos no ocupan el espacio original, lo que evita cambios inesperados en el diseño.

2. **Referencia su Posición Original:**
   - Los valores de desplazamiento (`top`, `left`, `bottom`, `right`) afectan su posición con respecto a donde estaría normalmente.

3. **Puede Superponerse a Otros Elementos:**
   - En combinación con el uso de `z-index`, el elemento con `position: relative` puede superponerse a otros elementos.

4. **Uso en Relación con Hijos:**
   - Si un elemento padre tiene `position: relative`, los elementos hijos con `position: absolute` tomarán como referencia al padre para su posicionamiento.

---

## **Sintaxis de Ejemplo**

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Position Relative</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="contenedor">
    <div class="caja normal">Caja Normal</div>
    <div class="caja relativa">Caja Relative</div>
    <div class="caja normal">Caja Normal</div>
  </div>
</body>
</html>
```

---

### **style.css**

```css
.contenedor {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

.caja {
  width: 150px;
  height: 100px;
  margin: 10px;
  background-color: lightgray;
  text-align: center;
  line-height: 100px;
  font-family: Arial, sans-serif;
}

.caja.relativa {
  position: relative;
  top: -20px; /* Se mueve 20px hacia arriba desde su posición original */
  left: 30px; /* Se mueve 30px hacia la derecha desde su posición original */
  background-color: lightblue;
  z-index: 1; /* Superpone la caja relativa a las normales */
}
```

---

## **Detalles del Ejemplo**

1. **Caja Normal:**
   - Representa elementos con el flujo estándar del documento.

2. **Caja Relative:**
   - Se mueve hacia arriba 20px y hacia la derecha 30px desde su posición original.
   - Conserva su espacio original, pero se superpone visualmente a los demás elementos debido al `z-index`.

---

## **Aplicaciones Comunes de `position: relative`**

1. **Posicionar Hijos Absolutos:**
   - Sirve como referencia para elementos hijos con `position: absolute`.

2. **Superposición Controlada:**
   - Combinar con `z-index` para crear diseños con capas o efectos visuales específicos.

3. **Ajustes Visuales Precisos:**
   - Útil para pequeños ajustes sin modificar el flujo del diseño.

--- 

### 🌐 Navegación

- <-- Anterior : [Position's y Z-INDEX](Position's%20y%20Z-INDEX.md)
- --> Siguiente : [Position Absolute](Position%20Absolute.md)
  
