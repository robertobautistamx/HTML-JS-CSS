# **POO en JavaScript**

La Programación Orientada a Objetos (POO) en JavaScript permite estructurar el código en torno a objetos que contienen propiedades y métodos, facilitando la organización y reutilización.

---

## **10.1 ¿Qué es un Objeto?**

Un objeto es una colección de propiedades (datos) y métodos (funciones asociadas).

### **Ejemplo Básico de un Objeto**

```javascript
const persona = {
  nombre: "Ana",
  edad: 25,
  saludar: function () {
    console.log(`Hola, mi nombre es ${this.nombre}`);
  }
};

console.log(persona.nombre); // Salida: Ana
persona.saludar();           // Salida: Hola, mi nombre es Ana
```

---

## **10.2 Clases**

Las clases son plantillas para crear objetos. Se introdujeron en ES6 para simplificar la creación de objetos.

### **Ejemplo de una Clase**

```javascript
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
}

const juan = new Persona("Juan", 30);
juan.saludar(); // Salida: Hola, mi nombre es Juan y tengo 30 años.
```

---

## **10.3 Herencia**

Permite que una clase herede propiedades y métodos de otra.

### **Ejemplo de Herencia**

```javascript
class Animal {
  constructor(nombre) {
    this.nombre = nombre;
  }

  hacerSonido() {
    console.log(`${this.nombre} está haciendo un sonido.`);
  }
}

class Perro extends Animal {
  ladrar() {
    console.log(`${this.nombre} está ladrando.`);
  }
}

const fido = new Perro("Fido");
fido.hacerSonido(); // Salida: Fido está haciendo un sonido.
fido.ladrar();      // Salida: Fido está ladrando.
```

---

## **10.4 Encapsulación**

Protege datos sensibles al usar propiedades privadas.

### **Ejemplo**

```javascript
class CuentaBancaria {
  #saldo; // Propiedad privada

  constructor(saldoInicial) {
    this.#saldo = saldoInicial;
  }

  depositar(cantidad) {
    this.#saldo += cantidad;
    console.log(`Depósito exitoso. Saldo actual: ${this.#saldo}`);
  }

  obtenerSaldo() {
    return this.#saldo;
  }
}

const cuenta = new CuentaBancaria(1000);
cuenta.depositar(500); // Salida: Depósito exitoso. Saldo actual: 1500
console.log(cuenta.obtenerSaldo()); // Salida: 1500
```

---

# **Métodos de Cadenas y Métodos de Arrays**

---

## **11.1 Métodos de Cadenas**

### **Propiedades Comunes**

1. **`length`:** Devuelve la longitud de una cadena.
   ```javascript
   const texto = "Hola Mundo";
   console.log(texto.length); // Salida: 10
   ```

### **Métodos Comunes**

1. **`toUpperCase` y `toLowerCase`:** Cambian el texto a mayúsculas o minúsculas.
   ```javascript
   console.log(texto.toUpperCase()); // Salida: HOLA MUNDO
   ```

2. **`slice`:** Extrae una parte de la cadena.
   ```javascript
   console.log(texto.slice(0, 4)); // Salida: Hola
   ```

3. **`replace`:** Reemplaza texto.
   ```javascript
   console.log(texto.replace("Mundo", "Amigo")); // Salida: Hola Amigo
   ```

4. **`split`:** Divide la cadena en un array.
   ```javascript
   console.log(texto.split(" ")); // Salida: ["Hola", "Mundo"]
   ```

---

## **11.2 Métodos de Arrays**

### **Métodos Comunes**

1. **`map`:** Itera sobre el array y transforma cada elemento.
   ```javascript
   const numeros = [1, 2, 3];
   console.log(numeros.map(x => x * 2)); // Salida: [2, 4, 6]
   ```

2. **`filter`:** Filtra elementos que cumplen una condición.
   ```javascript
   console.log(numeros.filter(x => x > 1)); // Salida: [2, 3]
   ```

3. **`reduce`:** Reduce el array a un único valor.
   ```javascript
   console.log(numeros.reduce((a, b) => a + b, 0)); // Salida: 6
   ```

4. **`push` y `pop`:** Agregan o eliminan elementos al final.
   ```javascript
   numeros.push(4); // [1, 2, 3, 4]
   numeros.pop();   // [1, 2, 3]
   ```

---

# **Objeto Math**

El objeto `Math` proporciona funciones matemáticas y propiedades.

---

## **12.1 Propiedades Comunes**

1. **`Math.PI`:** Valor de π.
   ```javascript
   console.log(Math.PI); // Salida: 3.141592653589793
   ```

2. **`Math.E`:** Base del logaritmo natural.
   ```javascript
   console.log(Math.E); // Salida: 2.718281828459045
   ```

---

## **12.2 Métodos Comunes**

1. **`Math.round`:** Redondea al entero más cercano.
   ```javascript
   console.log(Math.round(4.7)); // Salida: 5
   ```

2. **`Math.ceil` y `Math.floor`:** Redondeo hacia arriba o abajo.
   ```javascript
   console.log(Math.ceil(4.1));  // Salida: 5
   console.log(Math.floor(4.9)); // Salida: 4
   ```

3. **`Math.random`:** Genera un número aleatorio entre 0 y 1.
   ```javascript
   console.log(Math.random()); // Salida: Un número aleatorio
   ```

4. **`Math.max` y `Math.min`:** Encuentran el valor máximo o mínimo.
   ```javascript
   console.log(Math.max(1, 5, 10)); // Salida: 10
   ```

---

### 🌐 Navegación

- <-- Anterior : [Funciones](Funciones.md)  
- --> Siguiente : [Console (Consola de JavaScript)](Console%20(Consola%20de%20JavaScript).md)  