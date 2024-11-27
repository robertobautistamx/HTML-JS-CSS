# **Position Sticky**

La propiedad `position: sticky;` combina características de `relative` y `fixed`. Permite que un elemento actúe como parte del flujo normal del documento (`relative`), pero se fija en una posición específica dentro de su contenedor cuando se alcanza un punto definido con `top`, `left`, `bottom` o `right`.

---

## **Características Principales**

1. **Híbrido entre `relative` y `fixed`:**
   - Inicialmente, el elemento está posicionado de forma normal (`relative`).
   - Se "pega" (sticky) en la posición definida por las propiedades como `top` cuando se alcanza esa posición al hacer scroll.

2. **Depende del Contenedor Padre:**
   - El comportamiento sticky solo funciona dentro del área visible del contenedor padre.
   - Cuando el padre termina (scroll fuera de su área), el elemento sticky también deja de ser visible.

3. **Útil para Barras de Navegación o Títulos:**
   - Ayuda a mantener elementos visibles mientras se navega por una sección específica de la página.

---

## **Sintaxis Básica**

```css
.elemento-sticky {
  position: sticky;
  top: 10px; /* El elemento se pega 10px debajo del borde superior */
}
```

---

## **Ejemplo: Título Sticky dentro de una Sección**

### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Position Sticky</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <section>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore laboriosam 
      deserunt doloribus porro deleniti distinctio architecto molestias omnis 
      similique voluptate molestiae repudiandae perspiciatis.
      (Añade mucho más texto aquí para probar el desplazamiento)
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore laboriosam 
      deserunt doloribus porro deleniti distinctio architecto molestias omnis 
      similique voluptate molestiae repudiandae perspiciatis.
      (Añade mucho más texto aquí para probar el desplazamiento)
    </p>
    <h2 class="titulo-sticky">Título Sticky</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore laboriosam 
      deserunt doloribus porro deleniti distinctio architecto molestias omnis 
      similique voluptate molestiae repudiandae perspiciatis.
      (Añade mucho más texto aquí para probar el desplazamiento)
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore laboriosam 
      deserunt doloribus porro deleniti distinctio architecto molestias omnis 
      similique voluptate molestiae repudiandae perspiciatis.
      (Añade más texto aquí para probar el desplazamiento)
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore laboriosam 
      deserunt doloribus porro deleniti distinctio architecto molestias omnis 
      similique voluptate molestiae repudiandae perspiciatis.
      (Añade mucho más texto aquí para probar el desplazamiento)
    </p>
  </section>
</body>
</html>
```

---

### **style.css**

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 20px;
  line-height: 1.6;
}

/* Contenedor general */
section {
  width: 80%;
  margin: 0 auto;
  max-height: 400px; /* Altura limitada para mostrar el efecto */
  overflow-y: scroll; /* Permitir desplazamiento dentro de la sección */
  border: 1px solid #ccc;
  padding: 20px;
}

/* Elemento sticky */
.titulo-sticky {
  position: sticky;
  top: 0; /* Se pega en el borde superior del contenedor */
  background-color: #f4f4f4;
  padding: 10px;
  font-weight: bold;
  border-bottom: 2px solid #ddd;
}
```

---

## **Explicación del Ejemplo**

1. **`position: sticky`:**
   - Se utiliza en el título (`h2`) para que se mantenga visible cuando el usuario desplaza el contenido.

2. **`top: 0;`:**
   - Define que el elemento se pegará al borde superior del contenedor.

3. **Contenedor con Scroll:**
   - La sección tiene `overflow-y: scroll;` y un límite de altura (`max-height`), lo que permite ver el efecto sticky cuando se desplaza dentro de ella.

---

## **Casos de Uso Comunes**

1. **Títulos de Sección:**
   - Mantener los encabezados visibles al leer largos bloques de texto.

2. **Navegación en Subcontenedores:**
   - Fijar elementos importantes dentro de secciones específicas.

3. **Indicadores de Progreso:**
   - Usar sticky para mostrar elementos que acompañen el desplazamiento en secciones.

---

### 🌐 Navegación

- <-- Anterior : [Position Fixed](Position%20Fixed.md)
- --> Siguiente : [Display](Display.md)
