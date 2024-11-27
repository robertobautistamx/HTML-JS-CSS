# Formularios y Enlaces en HTML

## Formularios

Los formularios son una de las herramientas más importantes en HTML, ya que permiten a los usuarios enviar datos a un servidor para procesarlos.

---

### Estructura Básica de un Formulario

```html
<form action="/enviar-datos" method="POST">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" placeholder="Ingresa tu nombre">

  <label for="email">Correo Electrónico:</label>
  <input type="email" id="email" name="email" placeholder="Ingresa tu correo">

  <label for="mensaje">Mensaje:</label>
  <textarea id="mensaje" name="mensaje" placeholder="Escribe tu mensaje"></textarea>

  <button type="submit">Enviar</button>
</form>
```

#### Atributos del Formulario

`action`: Define la URL a donde se enviarán los datos del formulario.

```html
<form action="/enviar-datos">
method: Especifica el método HTTP que se utilizará para enviar los datos:
```

`GET`: Envía los datos en la URL.

`POST`: Envía los datos de forma segura en el cuerpo de la solicitud.

```html
<form method="POST">
<form method="GET">
```

`name`: Asigna un nombre al campo para identificarlo en el servidor.

```html
<input name="nombre">
```

`id` y `for`: Relacionan etiquetas <label> con campos del formulario.

```html
<label for="nombre">Nombre:</label>
<input id="nombre">
```

`placeholder`: Muestra un texto de ayuda dentro del campo.

```html
<input placeholder="Ingresa tu nombre">
```

`required`: Hace que el campo sea obligatorio.

```html
<input required>
```

---

## Tipos de Elementos en un Formulario HTML

Un formulario HTML incluye varios tipos de elementos para recopilar datos de los usuarios. Estos elementos son altamente personalizables y permiten interactuar de diversas maneras.


### 1. **Campos de Entrada (`<input>`)**

El elemento `<input>` es el más versátil y se usa para diversos propósitos según el valor de su atributo `type`.

### Tipos Comunes de `<input>`:

- **Texto (`type="text"`)**  

  Permite ingresar texto corto, como nombres o títulos.  
  ```html
  <input type="text" name="nombre" placeholder="Ingresa tu nombre">
  ```
  
- **Contraseña (`type="password"`)**

  Los caracteres ingresados se ocultan con asteriscos o puntos.

```html
<input type="password" name="clave" placeholder="Ingresa tu contraseña">
```

- **Correo Electrónico (`type="email"`)**

  Verifica que el usuario introduzca un formato válido de correo.

```html
<input type="email" name="correo" placeholder="Ingresa tu correo">
```

- **Número (`type="number"`)**

  Permite ingresar solo valores numéricos.

```html
<input type="number" name="edad" min="0" max="100">
```

- **Teléfono (`type="tel"`)**

  Acepta números telefónicos en varios formatos.

```html
<input type="tel" name="telefono" placeholder="123-456-7890">
```

- **Fecha (`type="date"`)**

  Proporciona un selector de fecha.

```html
<input type="date" name="fecha-nacimiento">
```

- **Archivo (`type="file"`)**
  
  Permite subir archivos.

```html
<input type="file" name="documento">
```

- **Casilla de Verificación (`type="checkbox"`)**
  
  Permite seleccionar varias opciones simultáneamente.

```html
<input type="checkbox" name="intereses" value="musica"> Música
<input type="checkbox" name="intereses" value="deportes"> Deportes
```

- **Botón de Radio (`type="radio"`)**

  Permite seleccionar solo una opción dentro de un grupo.

```html
<input type="radio" name="genero" value="masculino"> Masculino
<input type="radio" name="genero" value="femenino"> Femenino
```

- **Color (`type="color"`)**
  
  Abre un selector de color.

```html
<input type="color" name="color-favorito">
```

---

## Enlaces

Los enlaces permiten a los usuarios navegar entre páginas o recursos en un sitio web.

### Estructura Básica de un Enlace

```html
<a href="https://www.example.com" target="_blank" title="Visita Example">Ir a Example</a>
```

### Atributos Comunes en Enlaces

`<href>`: Define la URL a la que redirige el enlace.

```html
<a href="https://www.example.com">Ir a Example</a>
```

`target`: Especifica dónde abrir el enlace.

`_self`: (Por defecto) Abre el enlace en la misma pestaña.

`_blank`: Abre el enlace en una nueva pestaña.

```html
<a href="https://www.example.com" target="_blank">Abrir en nueva pestaña</a>
```

`title`: Muestra un texto emergente al pasar el cursor sobre el enlace.

```html
<a href="https://www.example.com" title="Ir a Example">Ir a Example</a>
```

---

## Enlaces Relativos y Absolutos

- ### Relativo
  
  Dirige a una página dentro del mismo sitio.

```html
<a href="pagina.html">Ir a Página</a>
```

- ### Absoluto

  Dirige a una URL completa.

```html
Copiar código
<a href="https://www.example.com">Ir a Example</a>
```

- ### Enlaces Internos (Anclas)
  
  Se utilizan para navegar dentro de la misma página.

```html
<a href="#seccion1">Ir a Sección 1</a>
<h2 id="seccion1">Sección 1</h2>
<p>Contenido de la sección 1.</p>
```

---

### 🌐 Navegación

- <-- Anterior : [Semantica en HTML](Semantica%20en%20HTML.md)
- --> Siguiente : [Multimedia](Multimedia.md)
