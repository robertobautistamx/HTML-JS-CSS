# Medidas en CSS: Fijas y Relativas

Cuando trabajamos con CSS, es fundamental entender cómo manejar las medidas para diseñar interfaces. Las medidas pueden ser **fijas** o **relativas**, y cada una tiene sus propias características y usos.

---

## **1. Medidas Fijas**

Las medidas fijas tienen un valor constante, independientemente del tamaño del dispositivo o la pantalla en la que se visualice el contenido.

### **Unidades Fijas Comunes**

- **`px` (píxeles):** Unidad más utilizada en medidas fijas. Representa un punto en la pantalla y no varía con el tamaño de la pantalla.
- **`cm` (centímetros):** Usada principalmente para diseño orientado a impresión.
- **`mm` (milímetros):** Similar al uso de `cm`, se utiliza para impresión.
- **`in` (pulgadas):** Representa medidas en pulgadas.
- **`pt` (puntos):** Utilizado en tipografía, donde 1 punto equivale a 1/72 de pulgada.
- **`pc` (picas):** Otra unidad tipográfica, 1 pica equivale a 12 puntos.

### **Ejemplo de Medidas Fijas**

#### **Archivo `index.html`**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Medidas Fijas</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="contenedor-fijo">Este contenedor tiene medidas fijas.</div>
</body>
</html>
```

#### **Archivo `style.css`**
```css
.contenedor-fijo {
  width: 300px; /* Ancho fijo en píxeles */
  height: 200px; /* Alto fijo en píxeles */
  background-color: lightblue;
  border: 2px solid blue;
}
```

### **Problemas con Medidas Fijas**

1. **Falta de Adaptabilidad:** No se ajustan al tamaño del dispositivo. Por ejemplo, un ancho de `300px` podría ser demasiado grande para un teléfono móvil.
2. **Diseño Poco Flexible:** Dificultan la creación de diseños responsivos.
3. **Problemas de Accesibilidad:** Los usuarios con configuraciones de pantalla personalizadas (por ejemplo, zoom) podrían tener dificultades para interactuar con la página.

---

## **2. Medidas Relativas**

Las medidas relativas son esenciales para el diseño responsivo porque se adaptan dinámicamente al tamaño del contenedor, pantalla o contenido donde se aplican. A diferencia de las medidas fijas, las relativas permiten crear diseños más flexibles y accesibles, ajustándose automáticamente a diferentes dispositivos y resoluciones.

---

### **Unidades Relativas Comunes**

#### **1. `%` (Porcentaje)**

El porcentaje se basa en el tamaño del contenedor padre. Esto significa que el tamaño del elemento se calcula como un porcentaje del ancho, alto o alguna otra dimensión del contenedor.

**Ejemplo:**
```html
<div class="contenedor">
  <div class="hijo">Contenido ajustado al 50% del ancho del contenedor.</div>
</div>
```

```css
.contenedor {
  width: 400px;
  height: 200px;
  border: 2px solid black;
}

.hijo {
  width: 50%; /* Mitad del ancho del contenedor */
  height: 50%; /* Mitad del alto del contenedor */
  background-color: lightblue;
}
```

**Uso Común:** Crear elementos que se ajusten proporcionalmente al espacio disponible, como imágenes o contenedores secundarios.

---

#### **2. `em`**

La unidad `em` se basa en el tamaño de la fuente del elemento padre. Si el tamaño de la fuente del padre es de `16px`, entonces `1em` equivale a `16px`.

**Ejemplo:**
```html
<div class="padre">
  <p class="hijo">Este texto tiene un tamaño relativo al padre.</p>
</div>
```

```css
.padre {
  font-size: 20px;
}

.hijo {
  font-size: 0.8em; /* 80% del tamaño de la fuente del padre */
}
```

**Uso Común:** Aplicar tamaños de fuente relativos, paddings o márgenes basados en la fuente del padre.

---

#### **3. `rem`**

La unidad `rem` se basa en el tamaño de la fuente raíz (`html`). Si no se especifica lo contrario, el tamaño base suele ser de `16px`.

**Ejemplo:**
```html
<p class="texto">Este texto tiene un tamaño relativo al elemento raíz.</p>
```

```css
html {
  font-size: 16px;
}

.texto {
  font-size: 1.5rem; /* 24px, basado en la fuente raíz */
}
```

**Diferencia entre `em` y `rem`:** Mientras que `em` depende del elemento padre, `rem` siempre se refiere a la raíz, asegurando consistencia en todo el diseño.

---

#### **4. `vw` (Viewport Width)**

`vw` representa un porcentaje del ancho de la ventana del navegador (viewport). `1vw` equivale al 1% del ancho total de la ventana.

**Ejemplo:**
```html
<p class="texto-anchura">Texto ajustado al ancho del viewport.</p>
```

```css
.texto-anchura {
  font-size: 5vw; /* Tamaño dinámico basado en el ancho de la ventana */
}
```

**Uso Común:** Elementos que se escalan proporcionalmente al ancho de la pantalla.

---

#### **5. `vh` (Viewport Height)**

`vh` funciona de manera similar a `vw`, pero se basa en la altura de la ventana. `1vh` equivale al 1% de la altura total del viewport.

**Ejemplo:**
```html
<div class="contenedor-altura">Este contenedor ocupa el 50% de la altura de la ventana.</div>
```

```css
.contenedor-altura {
  height: 50vh;
  background-color: lightgreen;
}
```

**Uso Común:** Crear elementos que ocupen un porcentaje específico de la altura visible de la pantalla.

---

#### **6. `vmin` y `vmax`**

- **`vmin`:** Basado en el menor valor entre `vw` y `vh`.
- **`vmax`:** Basado en el mayor valor entre `vw` y `vh`.

**Ejemplo:**
```html
<div class="cuadro-vmin">Este cuadro usa vmin.</div>
<div class="cuadro-vmax">Este cuadro usa vmax.</div>
```

```css
.cuadro-vmin {
  width: 50vmin; /* 50% del menor entre ancho y alto del viewport */
  height: 50vmin;
  background-color: lightcoral;
}

.cuadro-vmax {
  width: 50vmax; /* 50% del mayor entre ancho y alto del viewport */
  height: 50vmax;
  background-color: lightyellow;
}
```

**Uso Común:** Diseños dinámicos que necesitan reaccionar al tamaño del viewport en cualquier orientación.

---

### **Ventajas de las Medidas Relativas**

1. **Diseño Responsivo:** Las unidades relativas permiten que el diseño se adapte automáticamente a diferentes dispositivos.
2. **Flexibilidad:** Facilitan cambios globales en el diseño al modificar solo un tamaño base (`rem` o `%`).
3. **Accesibilidad:** Mejoran la experiencia del usuario al ajustarse a configuraciones personalizadas como el zoom del navegador.

---

### **Recomendaciones**

- Usa `rem` para establecer tamaños base consistentes.
- Usa `%`, `vw` y `vh` para diseños fluidos y adaptables.
- Mezcla unidades relativas con medidas fijas solo cuando sea necesario, como en elementos muy pequeños o específicos.

## **3. Importancia del Diseño Responsivo**

Un diseño responsivo asegura que tu sitio web se vea y funcione bien en dispositivos de todos los tamaños, desde teléfonos hasta monitores grandes. Usar medidas relativas es esencial para:

1. **Adaptabilidad:** Los elementos se ajustan automáticamente al tamaño del dispositivo.
2. **Mejor Experiencia de Usuario:** El contenido es accesible y fácil de leer en cualquier pantalla.
3. **SEO (Optimización para Motores de Búsqueda):** Los motores de búsqueda priorizan sitios web que son amigables para móviles.

---

## **Comparación: Medidas Fijas vs. Relativas**

| **Característica**           | **Medidas Fijas**         | **Medidas Relativas**               |
|-------------------------------|---------------------------|--------------------------------------|
| **Flexibilidad**             | Rígida                   | Altamente flexible                  |
| **Adaptabilidad a pantallas**| Baja                     | Alta                                |
| **Uso Común**                | Elementos específicos     | Diseño responsivo y global          |
| **Ejemplo**                  | `width: 300px;`          | `width: 50%;` o `width: 10vw;`      |

---

## **Recomendaciones**

1. Evita usar medidas fijas para elementos importantes o de gran tamaño.
2. Usa medidas relativas para garantizar que tu diseño sea responsivo.
3. Mezcla ambas estrategias solo cuando sea necesario (por ejemplo, medidas fijas para bordes pequeños y relativas para anchos o alturas).


---


### 🌐 Navegación

- <-- Anterior : [Metodología BEM](Metodología%20BEM.md)
- --> Siguiente : [Propiedades del Texto](Propiedades%20del%20Texto.md)
