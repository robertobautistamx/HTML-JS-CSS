# **Transiciones en CSS**

Las transiciones en CSS permiten cambiar suavemente entre valores de propiedades en un período de tiempo definido. Esto mejora la interacción visual en elementos de una página web.

---

## **1. Introducción a las Transiciones**

Una transición conecta dos estados de una propiedad con un efecto suave. Para utilizar transiciones, necesitamos definir dos elementos clave:

1. **Propiedad a animar**: La propiedad CSS que queremos que cambie.
2. **Duración**: El tiempo que tarda en completarse la transición.

---

## **2. Propiedades Principales de Transición**

| **Propiedad**       | **Descripción**                                                      |
|---------------------|----------------------------------------------------------------------|
| `transition-property` | Especifica la(s) propiedad(es) que tendrán la transición.         |
| `transition-duration` | Define el tiempo que dura la transición.                          |
| `transition-timing-function` | Controla la velocidad de cambio (similar a animaciones).  |
| `transition-delay`   | Establece un tiempo antes de que inicie la transición.             |
| `transition`         | Shorthand para todas las propiedades anteriores.                  |

---

## **3. Ejemplo Básico de Transición**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Transiciones CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <button class="boton">Haz clic</button>
</body>
</html>
```

### **style.css**
```css
.boton {
  background-color: lightblue;
  color: white;
  padding: 10px 20px;
  border: none;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.5s ease, transform 0.5s ease;
}

.boton:hover {
  background-color: darkblue;
  transform: scale(1.1);
}
```

**Resultado:**  
El botón cambia su color de fondo y se agranda ligeramente al pasar el mouse sobre él.

---

## **4. Diferencias con Animaciones**

| **Aspecto**         | **Transiciones**                                | **Animaciones**                                |
|---------------------|-------------------------------------------------|------------------------------------------------|
| **Definición**      | Necesitan un estado inicial y final.            | Se definen múltiples etapas (`@keyframes`).   |
| **Activación**      | Se activan por eventos como `:hover` o `:focus`. | Pueden ejecutarse automáticamente.            |
| **Control Temporal**| Limitado a cambios entre dos estados.           | Permite control avanzado sobre cada etapa.    |

---

## **5. Ejemplo con `transition-delay`**

```html
<div class="caja">Espera...</div>
```

```css
.caja {
  width: 100px;
  height: 100px;
  background-color: coral;
  transition: background-color 2s ease 1s;
}

.caja:hover {
  background-color: teal;
}
```

**Resultado:**  
La transición de color comienza 1 segundo después de pasar el mouse sobre la caja.

---

## **6. Transiciones en Múltiples Propiedades**

### **Ejemplo:**

```html
<div class="card">Tarjeta</div>
```

```css
.card {
  width: 150px;
  height: 150px;
  background-color: lightgray;
  transition: transform 0.5s, box-shadow 0.5s;
}

.card:hover {
  transform: rotate(15deg) scale(1.1);
  box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.5);
}
```

**Resultado:**  
La tarjeta rota, se agranda y se le aplica una sombra al pasar el mouse.

---

## **7. Recomendaciones de Uso**

1. **Simplicidad:**  
   - No abuses de las transiciones para no sobrecargar la experiencia visual.

2. **Accesibilidad:**  
   - Usa transiciones suaves que no afecten a personas sensibles a movimientos rápidos.

3. **Compatibilidad:**  
   - Asegúrate de que las propiedades sean compatibles en los navegadores objetivo.

---

### 🌐 Navegación

- <--> Volver al inicio : [Introducción y Especificidad](Introducción%20y%20Especificidad.md)
- --> Anterior : [Animaciones Básicas](Animaciones%20Básicas.md)
- --> Siguiente : [](.md)
