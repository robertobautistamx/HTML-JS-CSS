# Listas en HTML

Las listas son una forma común de estructurar elementos relacionados, ya sea en un orden específico o de manera desordenada. HTML ofrece etiquetas específicas para representarlas.

---

## **1. `<li>` (List Item)**

El elemento `<li>` representa un **elemento de lista**. Se utiliza dentro de `<ul>` (listas desordenadas) o `<ol>` (listas ordenadas) para definir cada uno de los elementos de la lista.

### **Ejemplo de Uso Básico**
```html
<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ul>
```

### **Notas:**
- Cada `<li>` es un elemento independiente dentro de la lista.
- Los navegadores suelen aplicar estilos por defecto (como viñetas o números) a los elementos `<li>` dependiendo del tipo de lista.

---

## **2. `<ul>` (Listas Desordenadas)**

La etiqueta `<ul>` define una **lista desordenada**, donde los elementos no tienen un orden jerárquico. Los navegadores suelen representarlas con viñetas como estilos predeterminados.

### **Ejemplo de Lista Desordenada**
```html
<ul>
  <li>Manzanas</li>
  <li>Naranjas</li>
  <li>Plátanos</li>
</ul>
```

**Resultado:**
- Manzanas
- Naranjas
- Plátanos

---

## **3. `<ol>` (Listas Ordenadas)**

La etiqueta `<ol>` define una **lista ordenada**, donde los elementos tienen un orden lógico, como números o letras.

### **Ejemplo de Lista Ordenada**
```html
<ol>
  <li>Primer paso</li>
  <li>Segundo paso</li>
  <li>Tercer paso</li>
</ol>
```

**Resultado:**
1. Primer paso
2. Segundo paso
3. Tercer paso

---

## **4. Listas Anidadas**

Las listas anidadas son listas dentro de otras listas. Esto es útil para mostrar relaciones jerárquicas entre elementos.

### **Ejemplo de Listas Anidadas**
```html
<ul>
  <li>Animales
    <ul>
      <li>Mamíferos</li>
      <li>Aves</li>
    </ul>
  </li>
  <li>Plantas</li>
</ul>
```

**Resultado:**
- Animales
  - Mamíferos
  - Aves
- Plantas

**Notas:**
- Una lista anidada puede ser tanto `<ul>` como `<ol>` dentro de otra lista.
- Cada nivel de anidación puede tener su propio estilo visual (viñetas o numeración).

---

## **Resumen de Listas**

| Etiqueta  | Descripción                                 | Estilo Predeterminado                  |
|-----------|---------------------------------------------|-----------------------------------------|
| `<ul>`    | Lista desordenada                          | Viñetas                                 |
| `<ol>`    | Lista ordenada                             | Números, letras o números romanos       |
| `<li>`    | Elemento dentro de una lista               | Basado en el tipo de lista contenedora  |

Las listas son una herramienta fundamental para estructurar información de forma clara y organizada en HTML.

---

### 🌐 Navegación

- <-- Anterior : [Introducción y Conceptos Basicos](Introducción%20y%20Conceptos%20Basicos.md)
- --> Siguiente : [Semantica en HTML](Semantica%20en%20HTML.md)
