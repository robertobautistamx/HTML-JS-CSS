# **Console (Consola de JavaScript)**

La consola es una herramienta que permite interactuar con el navegador para depurar y probar código JavaScript.

---

## **13.1 Introducción a la Consola**

La consola es parte de las herramientas de desarrollo del navegador. En JavaScript, el objeto `console` ofrece varios métodos para mostrar información en esta área.

### **Abrir la Consola**

1. **Atajo de teclado:**
   - En Windows/Linux: `Ctrl + Shift + I`
   - En macOS: `Cmd + Option + I`
2. Ve a la pestaña **"Consola"**.

---

## **13.2 Métodos Comunes**

### **`console.log`**

Imprime mensajes de texto o variables en la consola.

```javascript
console.log("Hola, mundo"); // Salida: Hola, mundo
```

### **`console.error`**

Muestra mensajes de error.

```javascript
console.error("Esto es un error"); // Salida en rojo
```

### **`console.warn`**

Muestra advertencias.

```javascript
console.warn("Esto es una advertencia"); // Salida en amarillo
```

### **`console.info`**

Muestra mensajes informativos.

```javascript
console.info("Información útil"); // Salida: Información útil
```

---

## **13.3 Limpieza de la Consola**

### **`console.clear`**

Limpia todos los mensajes previos en la consola.

```javascript
console.clear(); // Borra la consola
```

---

# **Métodos de Registro, Conteo, Agrupación y Temporización en Console**

---

## **14.1 Registro Avanzado**

### **`console.table`**

Muestra datos en formato tabular.

```javascript
const personas = [
  { nombre: "Ana", edad: 25 },
  { nombre: "Juan", edad: 30 }
];

console.table(personas);
/* Salida:
┌─────────┬─────────┬──────┐
│ (index) │ nombre  │ edad │
├─────────┼─────────┼──────┤
│    0    │  'Ana'  │  25  │
│    1    │ 'Juan'  │  30  │
└─────────┴─────────┴──────┘
*/
```

---

## **14.2 Conteo**

### **`console.count`**

Cuenta cuántas veces se ejecuta un código.

```javascript
console.count("Clic en botón");
console.count("Clic en botón");
// Salida:
// Clic en botón: 1
// Clic en botón: 2
```

---

## **14.3 Agrupación de Mensajes**

### **`console.group` y `console.groupEnd`**

Agrupa mensajes de consola bajo un mismo bloque.

```javascript
console.group("Información de Usuario");
console.log("Nombre: Ana");
console.log("Edad: 25");
console.groupEnd();
```

**Salida:**

```
Información de Usuario
  Nombre: Ana
  Edad: 25
```

---

## **14.4 Temporización**

### **`console.time` y `console.timeEnd`**

Mide el tiempo que tarda en ejecutarse un bloque de código.

```javascript
console.time("Carga de datos");
for (let i = 0; i < 1000; i++) {
  // Simula una operación
}
console.timeEnd("Carga de datos");
// Salida: Carga de datos: [Tiempo en ms]
```

---

### 🌐 Navegación

- <-- Anterior : [POO en JavaScript](POO%20en%20JavaScript.md)  
- --> Siguiente : [El DOM (Document Object Model)](El%20DOM%20(Document%20Object%20Model).md)  