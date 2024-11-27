# **Funciones**

Las funciones en JavaScript son bloques de código reutilizables que realizan una tarea específica. Pueden recibir datos (parámetros) y devolver resultados.

---

## **9.1 ¿Qué es una Función?**

Una función es un conjunto de instrucciones que se puede ejecutar cuando se llama.

### **Sintaxis Básica**

```javascript
function nombreFuncion() {
  // Código a ejecutar
}
```

**Ejemplo:**

```javascript
function saludar() {
  console.log("¡Hola, mundo!");
}

saludar(); // Llama a la función. Salida: ¡Hola, mundo!
```

---

## **9.2 Funciones con Parámetros**

Los parámetros permiten que las funciones trabajen con datos específicos.

### **Ejemplo con Parámetros**

```javascript
function saludar(nombre) {
  console.log(`¡Hola, ${nombre}!`);
}

saludar("Ana"); // Salida: ¡Hola, Ana!
```

---

## **9.3 Funciones que Devuelven Valores**

Las funciones pueden devolver valores usando `return`.

### **Ejemplo**

```javascript
function sumar(a, b) {
  return a + b;
}

const resultado = sumar(5, 10);
console.log(resultado); // Salida: 15
```

---

## **9.4 Funciones Anónimas**

Son funciones sin nombre que se asignan a una variable.

### **Ejemplo**

```javascript
const multiplicar = function (a, b) {
  return a * b;
};

console.log(multiplicar(4, 5)); // Salida: 20
```

---

## **9.5 Funciones Flecha**

Una sintaxis más compacta para definir funciones.

### **Ejemplo**

```javascript
const restar = (a, b) => a - b;

console.log(restar(10, 4)); // Salida: 6
```

---

## **9.6 Funciones de Orden Superior**

Las funciones pueden recibir otras funciones como argumentos o devolver funciones.

### **Ejemplo**

```javascript
function aplicarOperacion(a, b, operacion) {
  return operacion(a, b);
}

const dividir = (a, b) => a / b;

console.log(aplicarOperacion(20, 5, dividir)); // Salida: 4
```

---

## **9.7 Función Recursiva**

Una función que se llama a sí misma para resolver problemas repetitivos.

### **Ejemplo**

```javascript
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}

console.log(factorial(5)); // Salida: 120
```

---

## **9.8 Funciones Incorporadas**

JavaScript incluye varias funciones listas para usar.

### **Ejemplos**

1. **`parseInt` y `parseFloat`:** Convertir cadenas en números.
2. **`isNaN`:** Verificar si un valor no es un número.
3. **`setTimeout`:** Ejecutar una función después de un retraso.

```javascript
setTimeout(() => {
  console.log("Esto se ejecuta después de 3 segundos");
}, 3000);
```

---

### 🌐 Navegación

- <-- Anterior : [Arrays y Arrays Asociativos](Arrays%20y%20Arrays%20Asociativos.md)  
- --> Siguiente : [POO en JavaScript](POO%20en%20JavaScript.md)  