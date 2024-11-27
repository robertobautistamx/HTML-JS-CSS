# **Templates de Strings y Backticks**

Los templates de strings y el uso de backticks (`` ` ``) son una característica avanzada de JavaScript que facilita la creación y manipulación de cadenas. 

---

## **5. Templates de Strings y Uso de Backticks**

Los templates de strings permiten incluir expresiones e interpolar variables directamente en cadenas de texto sin necesidad de concatenarlas manualmente.

### **Sintaxis Básica con Backticks**

- Se usan **backticks** (`` ` ``) en lugar de comillas simples o dobles para definir la cadena.
- Permiten insertar variables y expresiones utilizando `${}`.

```javascript
const nombre = "Juan";
const edad = 25;

const mensaje = `Hola, mi nombre es ${nombre} y tengo ${edad} años.`;
console.log(mensaje); // Salida: Hola, mi nombre es Juan y tengo 25 años.
```

### **Ventajas**

1. **Legibilidad:**
   - Simplifica el código y lo hace más limpio al evitar concatenaciones largas.

2. **Interpolación:**
   - Puedes insertar expresiones complejas dentro de `${}`.

```javascript
const a = 5;
const b = 10;
console.log(`El resultado de ${a} + ${b} es ${a + b}.`); // Salida: El resultado de 5 + 10 es 15.
```

3. **Multilínea:**
   - Permite escribir cadenas de varias líneas sin usar caracteres de escape como `\n`.

```javascript
const mensaje = `Hola,
Este es un mensaje
en varias líneas.`;
console.log(mensaje);
```

---

## **6. Camel Case**

**Camel Case** es una convención para nombrar variables, funciones o identificadores. 

### **Reglas del Camel Case**

1. La primera palabra comienza con minúscula.
2. Cada palabra subsiguiente comienza con mayúscula.
3. No incluye espacios, guiones ni subrayados.

### **Ejemplo:**

```javascript
let nombreCompleto = "Juan Pérez";
let numeroDeEstudiantes = 30;
```

### **Ventajas del Camel Case**

1. **Legibilidad:**
   - Hace que los nombres de las variables sean más fáciles de leer.

2. **Consistencia:**
   - Es el estándar más utilizado en JavaScript para variables y funciones.

### **¿Dónde Usarlo?**

1. **Variables:**
   ```javascript
   let miNombre = "Ana";
   let numeroDeClases = 10;
   ```

2. **Funciones:**
   ```javascript
   function obtenerNombreCompleto(nombre, apellido) {
       return `${nombre} ${apellido}`;
   }
   console.log(obtenerNombreCompleto("Juan", "Pérez"));
   ```

3. **Nombres de objetos y propiedades:**
   ```javascript
   const persona = {
       nombreCompleto: "Juan Pérez",
       edad: 25,
       tieneLicencia: true
   };
   ```

---

### 🌐 Navegación

- <-- Anterior : [Introducción a JavaScript](Introducción%20a%20JavaScript.md)  
- --> Siguiente : [Arrays y Arrays Asociativos](Arrays%20y%20Arrays%20Asociativos.md)  