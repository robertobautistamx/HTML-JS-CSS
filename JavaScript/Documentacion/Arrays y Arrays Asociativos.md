# **Arrays y Arrays Asociativos**

Los arrays son estructuras de datos fundamentales en JavaScript que permiten almacenar múltiples valores en una sola variable. Los arrays asociativos, aunque no son oficialmente arrays en JavaScript, funcionan de manera similar a objetos.

---

## **7. Arrays**

### **¿Qué es un Array?**

Un array es una colección ordenada de valores, donde cada valor (elemento) tiene un índice numérico.

### **Sintaxis Básica**

```javascript
const frutas = ["Manzana", "Banana", "Cereza"];
console.log(frutas[0]); // Salida: Manzana
```

### **Características**

1. **Índice:** Cada elemento tiene un índice numérico, comenzando desde `0`.
2. **Longitud:** Puedes obtener el número de elementos con `.length`.

```javascript
console.log(frutas.length); // Salida: 3
```

3. **Métodos Comunes:**
   - **`push`**: Agrega un elemento al final.
   - **`pop`**: Elimina el último elemento.
   - **`shift`**: Elimina el primer elemento.
   - **`unshift`**: Agrega un elemento al principio.

```javascript
frutas.push("Durazno"); // ["Manzana", "Banana", "Cereza", "Durazno"]
frutas.pop();           // ["Manzana", "Banana", "Cereza"]
```

---

## **Arrays Asociativos**

En JavaScript, los arrays asociativos no existen como tal, pero puedes usar objetos para almacenar datos con claves personalizadas.

### **Ejemplo Básico**

```javascript
const persona = {
  nombre: "Juan",
  edad: 25,
  profesion: "Ingeniero"
};

console.log(persona["nombre"]); // Salida: Juan
console.log(persona.edad);      // Salida: 25
```

### **Diferencia con Arrays**

- Un array usa índices numéricos.
- Un objeto usa claves (también llamadas propiedades).

---

# **Bucles e Iteraciones**

Los bucles permiten repetir un bloque de código varias veces, ya sea con base en una condición o una cantidad específica de repeticiones.

---

## **8.1 While**

El bucle `while` ejecuta un bloque de código mientras la condición sea verdadera.

### **Sintaxis**

```javascript
let contador = 0;

while (contador < 5) {
  console.log("El contador es:", contador);
  contador++;
}
```

---

## **8.2 For**

El bucle `for` es ideal para iterar un número específico de veces.

### **Sintaxis**

```javascript
for (let i = 0; i < 5; i++) {
  console.log(`Iteración número: ${i}`);
}
```

---

## **8.3 Iterar sobre un Array**

Puedes usar un bucle para recorrer los elementos de un array.

```javascript
const colores = ["Rojo", "Verde", "Azul"];

for (let i = 0; i < colores.length; i++) {
  console.log(`Color: ${colores[i]}`);
}
```

---

## **8.4 For...of**

Una forma más moderna de recorrer arrays.

```javascript
for (const color of colores) {
  console.log(`Color: ${color}`);
}
```

---

## **8.5 For...in**

Se usa principalmente para recorrer propiedades de un objeto.

```javascript
const persona = { nombre: "Ana", edad: 30 };

for (const clave in persona) {
  console.log(`${clave}: ${persona[clave]}`);
}
```

---

### 🌐 Navegación

- <-- Anterior : [Templates de Strings y Backticks](Templates%20de%20Strings%20y%20Backticks.md)  
- --> Siguiente : [Funciones](Funciones.md)  