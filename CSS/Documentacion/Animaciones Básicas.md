# **Animaciones Básicas en CSS**

Las animaciones en CSS permiten crear movimientos o transiciones fluidas de propiedades de un elemento a lo largo del tiempo, mejorando la interacción y experiencia del usuario en una página web.

---

## **1. Introducción a las Animaciones en CSS**

Las animaciones se definen usando la regla `@keyframes`, que especifica los cambios de estilo en diferentes etapas. Para activar una animación, se usa la propiedad `animation` o sus subpropiedades.

### **Propiedades Principales de Animación:**

| **Propiedad**         | **Descripción**                                                      |
|------------------------|----------------------------------------------------------------------|
| `animation-name`       | Define el nombre de la animación (coincide con el de `@keyframes`). |
| `animation-duration`   | Tiempo que tarda la animación en completarse.                      |
| `animation-timing-function` | Define la velocidad de cambio de la animación (lineal, acelerada, etc.). |
| `animation-delay`      | Tiempo que espera antes de comenzar la animación.                  |
| `animation-iteration-count` | Número de veces que la animación se repite (o `infinite`).    |
| `animation-direction`  | Dirección de reproducción (`normal`, `reverse`, etc.).             |
| `animation-fill-mode`  | Estilos aplicados antes o después de la animación.                 |
| `animation`            | Shorthand para definir todas las propiedades anteriores.          |

---

## **2. Sintaxis Básica**

### **Ejemplo 1: Animación de Movimiento**

### **index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animación Básica</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="cuadro"></div>
</body>
</html>
```

### **style.css**
```css
@keyframes mover {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(200px);
  }
  100% {
    transform: translateX(0);
  }
}

.cuadro {
  width: 50px;
  height: 50px;
  background-color: red;
  animation: mover 2s ease-in-out infinite;
}
```

**Resultado:**  
Un cuadro rojo que se mueve horizontalmente hacia la derecha y regresa a su posición inicial, repitiéndose indefinidamente.

---

## **3. Transiciones con `animation-timing-function`**

La propiedad `animation-timing-function` controla la velocidad de cambio de la animación.

### Valores Comunes:

- `linear`: La animación ocurre a una velocidad constante.
- `ease`: La animación acelera al principio y desacelera al final.
- `ease-in`: La animación acelera al principio.
- `ease-out`: La animación desacelera al final.
- `steps(n)`: Divide la animación en `n` pasos.

### **Ejemplo 2: Diferentes Tiempos de Animación**

### **style.css**
```css
@keyframes rotar {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.circulo {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: blue;
  margin: 10px;
}

.lineal {
  animation: rotar 3s linear infinite;
}

.ease {
  animation: rotar 3s ease infinite;
}

.steps {
  animation: rotar 3s steps(6) infinite;
}
```

**HTML:**
```html
<div class="circulo lineal"></div>
<div class="circulo ease"></div>
<div class="circulo steps"></div>
```

**Resultado:**  
Tres círculos con diferentes estilos de rotación: uno constante (`linear`), uno suave (`ease`) y uno por pasos (`steps`).

---

## **4. `animation-fill-mode`**

Controla los estilos aplicados antes y después de la animación.

### Valores Comunes:

- `none`: No aplica estilos fuera de la animación.
- `forwards`: Mantiene los estilos del último fotograma después de la animación.
- `backwards`: Aplica los estilos del primer fotograma antes de comenzar la animación.
- `both`: Combina `forwards` y `backwards`.

### **Ejemplo 3: Uso de `animation-fill-mode`**

```css
@keyframes crecer {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(1.5);
  }
}

.caja {
  width: 100px;
  height: 100px;
  background-color: purple;
  margin: 10px;
}

.sin-fill {
  animation: crecer 2s none;
}

.forwards {
  animation: crecer 2s forwards;
}

.backwards {
  animation: crecer 2s backwards;
}
```

**HTML:**
```html
<div class="caja sin-fill"></div>
<div class="caja forwards"></div>
<div class="caja backwards"></div>
```

---

## **5. Animaciones Complejas con Múltiples Efectos**

### **Ejemplo 4: Animación Combinada**

### **style.css**
```css
@keyframes combinado {
  0% {
    transform: translateX(0) scale(1);
    background-color: red;
  }
  50% {
    transform: translateX(150px) scale(1.2);
    background-color: yellow;
  }
  100% {
    transform: translateX(0) scale(1);
    background-color: red;
  }
}

.cuadro-combinado {
  width: 100px;
  height: 100px;
  animation: combinado 3s ease-in-out infinite;
}
```

**HTML:**
```html
<div class="cuadro-combinado"></div>
```

**Resultado:**  
Un cuadro que cambia de tamaño, posición y color en un ciclo infinito.

---

## **6. Recomendaciones de Uso**

1. **Optimización:**  
   - Usa animaciones ligeras para evitar sobrecargar la página, especialmente en dispositivos móviles.
   
2. **Accesibilidad:**  
   - Evita animaciones que puedan causar molestias visuales, como flashes rápidos.

3. **Responsividad:**  
   - Adapta las animaciones según el tamaño de la pantalla usando media queries.

---

### 🌐 Navegación

- <-- Anterior : [Pseudo-Clases](Pseudo-Clases.md)
- --> Siguiente : [Transiciones en CSS](Transitions.md)
