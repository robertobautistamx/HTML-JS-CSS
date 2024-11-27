# **Atributos Globales y Atributos de Input**

Los atributos globales son aquellos que pueden aplicarse a cualquier elemento HTML, mientras que los atributos de input son específicos para la etiqueta `<input>` y otros elementos de formulario.

---

## **17.1 Atributos Globales**

Los atributos globales pueden ser utilizados en cualquier elemento HTML para agregar funcionalidades, estilos o información adicional.

### **Atributos Globales Comunes**

1. **`id`:** Identificador único para el elemento.
   ```html
   <h1 id="titulo">Hola Mundo</h1>
   ```
   - Usado para identificar elementos de manera única.

2. **`class`:** Clase o grupo al que pertenece el elemento.
   ```html
   <p class="texto">Texto con estilo</p>
   ```
   - Permite aplicar estilos o seleccionar múltiples elementos.

3. **`style`:** Estilo en línea para el elemento.
   ```html
   <div style="color: red;">Texto en rojo</div>
   ```
   - Evita usarlo excesivamente; prefiera archivos CSS.

4. **`hidden`:** Oculta el elemento en la página.
   ```html
   <p hidden>Este texto está oculto</p>
   ```

5. **`title`:** Muestra información adicional cuando el usuario pasa el cursor.
   ```html
   <button title="Haz clic aquí">Clic</button>
   ```

6. **`data-*`:** Atributos personalizados para almacenar datos específicos.
   ```html
   <div data-usuario="1234">Usuario</div>
   ```
   - Muy útil para JavaScript y manipulación dinámica.

---

## **17.2 Atributos de Input**

Los atributos de input definen cómo un campo de entrada interactúa con el usuario.

### **Atributos Comunes para Inputs**

1. **`type`:** Especifica el tipo de entrada.
   ```html
   <input type="text" placeholder="Escribe aquí">
   ```

2. **`placeholder`:** Texto visible dentro del campo hasta que el usuario escribe.
   ```html
   <input type="email" placeholder="Correo electrónico">
   ```

3. **`value`:** Establece el valor inicial del campo.
   ```html
   <input type="text" value="Hola">
   ```

4. **`required`:** Indica que el campo es obligatorio.
   ```html
   <input type="password" required>
   ```

5. **`disabled`:** Desactiva el campo, impidiendo interacción.
   ```html
   <input type="text" disabled>
   ```

6. **`readonly`:** Campo de solo lectura; no permite edición.
   ```html
   <input type="text" value="Solo lectura" readonly>
   ```

7. **`min` y `max`:** Define valores mínimo y máximo para números.
   ```html
   <input type="number" min="1" max="10">
   ```

8. **`pattern`:** Define un patrón de validación con expresiones regulares.
   ```html
   <input type="text" pattern="[A-Za-z]{3,}">
   ```

9. **`checked`:** Marca una casilla o radio por defecto.
   ```html
   <input type="checkbox" checked>
   ```

---

# **Propiedad Style, Clases y Métodos de `classList`**

La manipulación de estilos, clases y el uso de `classList` es crucial para modificar dinámicamente la apariencia y comportamiento de los elementos en la página.

---

## **18.1 Propiedad `style`**

La propiedad `style` permite modificar estilos en línea directamente desde JavaScript.

### **Ejemplo de `style`**
```html
<div id="caja">Caja de ejemplo</div>
<script>
  const caja = document.getElementById("caja");
  caja.style.backgroundColor = "lightblue"; // Cambia el fondo
  caja.style.border = "2px solid black"; // Añade un borde
</script>
```

---

## **18.2 Clases en HTML**

Las clases permiten aplicar estilos predefinidos y agrupar elementos.

### **Uso de Clases**
```html
<div class="caja azul">Caja Azul</div>
<div class="caja roja">Caja Roja</div>
<style>
  .caja { padding: 20px; border: 2px solid black; }
  .azul { background-color: blue; color: white; }
  .roja { background-color: red; color: white; }
</style>
```

---

## **18.3 Métodos de `classList`**

El objeto `classList` permite manipular dinámicamente las clases de un elemento.

### **Métodos Comunes**

1. **`add`:** Añade una clase.
   ```javascript
   caja.classList.add("nueva-clase");
   ```

2. **`remove`:** Elimina una clase.
   ```javascript
   caja.classList.remove("azul");
   ```

3. **`toggle`:** Alterna una clase (la añade si no está, la elimina si ya está).
   ```javascript
   caja.classList.toggle("activo");
   ```

4. **`contains`:** Verifica si un elemento tiene una clase específica.
   ```javascript
   console.log(caja.classList.contains("activo")); // true o false
   ```

---

## **Ejemplo Completo**

### **HTML (`index.html`)**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Clases y Estilos</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div id="caja" class="caja azul">Caja de ejemplo</div>
  <button id="cambiar">Cambiar Clase</button>
  <script src="script.js"></script>
</body>
</html>
```

### **CSS (`styles.css`)**
```css
.caja {
  padding: 20px;
  border: 2px solid black;
  color: white;
}

.azul {
  background-color: blue;
}

.roja {
  background-color: red;
}
```

### **JavaScript (`script.js`)**
```javascript
const caja = document.getElementById("caja");
const boton = document.getElementById("cambiar");

boton.addEventListener("click", () => {
  caja.classList.toggle("roja"); // Alterna entre azul y roja
});
```

---

### 🌐 Navegación

- <-- Anterior : [Métodos de Selección y Atributos de Elementos](Metodos%20de%20Seleccion%20y%20Atributos%20de%20Elementos.md)  
- --> Siguiente : [Obtención y Modificación de Elementos](Obtencion%20y%20Modificacion%20de%20Elementos.md)  