# **Position en CSS**

La propiedad **`position`** en CSS se utiliza para definir cómo un elemento debe ubicarse dentro de su contenedor o en la página web. Además, permite controlar la posición exacta de un elemento mediante las propiedades **`top`**, **`left`**, **`bottom`**, y **`right`**, en combinación con el contexto de apilamiento (**z-index**).

---

## **Posicionamiento y Uso**

### **Tipos de Posicionamiento**

Existen diferentes valores para la propiedad `position`, que se explicarán más adelante en archivos dedicados para cada uno. Sin embargo, a continuación, se presenta un resumen breve:

- **[`static`]() (por defecto):** El elemento sigue el flujo normal del documento.
- **[`relative`]() :** Posiciona el elemento relativo a su posición normal.
- **[`absolute`]() :** Posiciona el elemento relativo a su primer contenedor posicionado.
- **[`fixed`]() :** Posiciona el elemento relativo a la ventana del navegador.
- **[`sticky`]() :** Combina lo mejor de `relative` y `fixed`, dependiendo del scroll.

---

## **Control de Posición con `top`, `left`, `bottom`, y `right`**

Estas propiedades se utilizan para mover elementos en la página. Su funcionamiento depende del tipo de posición aplicado:

1. **`top`**: Mueve el elemento hacia abajo desde el borde superior del contenedor.
2. **`left`**: Mueve el elemento hacia la derecha desde el borde izquierdo del contenedor.
3. **`bottom`**: Mueve el elemento hacia arriba desde el borde inferior del contenedor.
4. **`right`**: Mueve el elemento hacia la izquierda desde el borde derecho del contenedor.

**Nota sobre la jerarquía:**
- Generalmente, **`top`** y **`left`** son los más utilizados porque, en interfaces web, se prioriza el movimiento desde la esquina superior izquierda como punto de referencia.
- **`bottom`** y **`right`** se usan cuando es necesario trabajar desde los bordes inferiores o derechos.

**Ejemplo Básico de Control de Posición:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Position: Relative</title>
  <style>
    .contenedor {
      width: 300px;
      height: 300px;
      background-color: lightgray;
      position: relative;
    }
    .caja {
      width: 100px;
      height: 100px;
      background-color: lightblue;
      position: absolute;
      top: 50px; /* Mueve hacia abajo */
      left: 100px; /* Mueve hacia la derecha */
    }
  </style>
</head>
<body>
  <div class="contenedor">
    <div class="caja"></div>
  </div>
</body>
</html>
```

---

## **Z-Index**

La propiedad **`z-index`** controla el orden de apilamiento de los elementos. En otras palabras, define qué elementos estarán al frente o detrás en la interfaz visual.

### **Comportamiento por Defecto**

- Los elementos se apilan en el orden en que están en el DOM, es decir, los que están declarados más abajo estarán por encima.

### **Asignación Manual con `z-index`**

- Puedes asignar manualmente un valor a `z-index` para controlar el orden.
- Es buena práctica dejar un espacio entre valores (ejemplo: usar 10, 20, 30) para permitir la inserción de nuevos elementos sin necesidad de reajustar todo.

```css
.elemento1 {
  position: relative;
  z-index: 10; /* Elemento detrás */
}

.elemento2 {
  position: relative;
  z-index: 20; /* Elemento al frente */
}
```

### **Ejemplo Básico de Z-Index:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Z-Index</title>
  <style>
    .caja1 {
      width: 150px;
      height: 150px;
      background-color: lightblue;
      position: relative;
      z-index: 10; /* Apilado detrás */
    }
    .caja2 {
      width: 150px;
      height: 150px;
      background-color: lightcoral;
      position: relative;
      z-index: 20; /* Apilado al frente */
      margin-top: -100px; /* Superposición visual */
    }
  </style>
</head>
<body>
  <div class="caja1"></div>
  <div class="caja2"></div>
</body>
</html>
```

---

## **Conflicto Hijo-Padre con Z-Index**

Por defecto, un hijo con un `z-index` mayor siempre estará sobre el padre. Sin embargo, para colocar un padre por encima de un hijo, puedes usar el siguiente truco:

1. Asigna al hijo un `z-index: -1`.
2. No declares `z-index` en el padre (debe quedar sin valor asignado).

**Ejemplo Resolviendo Conflicto Hijo-Padre:**

#### **index.html**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Conflicto Hijo-Padre</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="padre">
    <div class="hijo"></div>
  </div>
</body>
</html>
```

---

#### **style.css**

```css
.padre {
  width: 200px;
  height: 200px;
  background-color: lightgray;
  position: relative;
}

.hijo {
  width: 100px;
  height: 100px;
  background-color: lightblue;
  position: absolute;
  z-index: -1; /* Hijo detrás del padre */
}
```

--- 

Para futuras ocasiones, seguiré este formato. Esto hace que sea más claro y modular al momento de trabajar con ejemplos.
---

### 🌐 Navegación

- <-- Anterior: [Transform y Outline](Transform%20y%20Outline.md)  
- --> Siguiente : [Position Relative](Position%20Relative.md)
