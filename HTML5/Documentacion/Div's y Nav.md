# Uso y Funcionamiento de `<div>` y `<nav>` en HTML

## **Div (`<div>`)**

### **¿Qué es un `<div>`?**
La etiqueta `<div>` (abreviatura de "division") es un contenedor genérico en HTML. Sirve para agrupar otros elementos y organizar el contenido en bloques. No tiene significado semántico específico, pero es extremadamente útil para estructurar el contenido de una página.

---

### **¿Para qué sirve `<div>`?**
1. **Agrupar elementos relacionados**:  
   Permite reunir elementos que comparten una funcionalidad o propósito común. Por ejemplo, un grupo de imágenes o un bloque de texto.
   
2. **Organizar la estructura de la página**:  
   Ayuda a dividir el contenido en secciones lógicas para facilitar el diseño y mantenimiento del código.

3. **Crear bloques personalizables**:  
   Aunque `<div>` no tiene estilo por defecto, se puede personalizar (usualmente con CSS) para aplicar diseño o comportamiento a bloques específicos.

---

### **¿Cuándo usar `<div>`?**
- Cuando no existe una etiqueta semántica adecuada para el propósito del contenido.  
- Para dividir y estructurar grandes secciones de contenido.  
- Como contenedor general para agrupar elementos que comparten un propósito en común.

---

### **Ejemplo de Uso Básico de `<div>`**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Div</title>
</head>
<body>
  <div>
    <h1>Título Principal</h1>
    <p>Este es un párrafo dentro de un div.</p>
  </div>

  <div>
    <h2>Sección Relacionada</h2>
    <p>Otro contenido relacionado dentro de un segundo div.</p>
  </div>
</body>
</html>
```

### **Ejemplo de Agrupación de Elementos con `<div>`**

```html
<div>
  <h1>Galería de Imágenes</h1>
  <img src="imagen1.jpg" alt="Imagen 1">
  <img src="imagen2.jpg" alt="Imagen 2">
  <img src="imagen3.jpg" alt="Imagen 3">
</div>
```

---

El `<div>` actúa como un contenedor que agrupa las imágenes y su encabezado, proporcionando una estructura lógica.

Por sí mismo, un `<div>` no aporta información sobre el propósito o contenido que agrupa. Esto significa que los lectores de pantalla no interpretan el contenido de manera significativa.

**Uso correcto:**

Se debe usar solo cuando no haya una etiqueta más específica o semántica que cumpla el propósito.

---

## **Nav (`<nav>`)**

### **¿Qué es un `<nav>`?**
 
La etiqueta `<nav>` es un contenedor semántico que se utiliza para definir secciones de navegación. Representa un bloque de enlaces que permiten al usuario moverse entre diferentes partes de un sitio web o dentro de la misma página.

---

### **¿Para qué sirve `<nav>`?**

  1. **Crear menús de navegación**:
     Específicamente diseñado para contener enlaces que permiten navegar por un sitio web.

  2. **Mejorar la accesibilidad:**
      Al ser una etiqueta semántica, los navegadores y lectores de pantalla la reconocen como una sección de navegación, lo que mejora la experiencia de usuario.

  3. **Organizar enlaces importantes:**
      Agrupa enlaces relevantes como un menú principal, una barra lateral o un índice interno.

---

### **¿Cuándo usar `<nav>`?**
  - Cuando estás creando un menú de navegación principal o secundario.
  - Para agrupar enlaces que llevan a diferentes secciones del sitio web o a otras páginas.
  - No debe usarse para agrupar enlaces que no sean de navegación, como en un pie de página con enlaces de contacto.

---

#### **Ejemplo de Uso Básico de `<nav>`**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Nav</title>
</head>
<body>
  <nav>
    <ul>
      <li><a href="index.html">Inicio</a></li>
      <li><a href="about.html">Sobre Nosotros</a></li>
      <li><a href="services.html">Servicios</a></li>
      <li><a href="contact.html">Contacto</a></li>
    </ul>
  </nav>
</body>
</html>
```

El `<nav>` agrupa un conjunto de enlaces que forman un menú de navegación. Este menú permite al usuario desplazarse entre diferentes páginas del sitio.

---

### **Ejemplo de Navegación Interna con `<nav>`**

```html
<nav>
  <ul>
    <li><a href="#seccion1">Sección 1</a></li>
    <li><a href="#seccion2">Sección 2</a></li>
    <li><a href="#seccion3">Sección 3</a></li>
  </ul>
</nav>

<section id="seccion1">
  <h2>Contenido de la Sección 1</h2>
  <p>Esta es la primera sección del contenido.</p>
</section>
<section id="seccion2">
  <h2>Contenido de la Sección 2</h2>
  <p>Esta es la segunda sección del contenido.</p>
</section>
<section id="seccion3">
  <h2>Contenido de la Sección 3</h2>
  <p>Esta es la tercera sección del contenido.</p>
</section>
```

El `<nav>` contiene enlaces que permiten navegar dentro de diferentes secciones de la misma página utilizando anclajes.

---

### **Aspectos Semánticos de `<nav>`**

Los navegadores y herramientas de accesibilidad interpretan <nav> como una sección de navegación.

**Uso correcto:**

Debe contener exclusivamente enlaces de navegación. No se debe usar para agrupar cualquier conjunto de enlaces (por ejemplo, enlaces de redes sociales en un pie de página).

---

### 🌐 Navegación

- <-- Anterior : [Multimedia](Multimedia.md)
- --> Siguiente : [Metadatos](Metadatos.md)
