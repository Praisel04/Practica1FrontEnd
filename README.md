# 🕹️ Práctica 2 – Dinamismo con JavaScript y el DOM  
**Asignatura:** Desarrollo Front-End  
**Curso:** 2025–2026  
**Autores:** *Iván Seco Martín* y *Iván Ruano Prieto*  

---

## 🎯 Objetivo  
Ampliar el trabajo de la práctica anterior incorporando **JavaScript y manipulación del DOM** para mejorar la **interactividad, usabilidad y dinamismo** del formulario de registro de *Gaming Store*.

El proyecto incluye validación de contraseñas en tiempo real y un botón interactivo de mostrar/ocultar contraseña, todo implementado siguiendo las **buenas prácticas modernas de programación JavaScript**.

---

## 🧩 Estructura del proyecto
```
/css/
└── p1fe.css → estilos personalizados y CSS del botón de ojo
/js/
└── validacion.js → lógica JavaScript (validación + toggle)
index.html → estructura HTML del formulario
README.md → este documento
```

---

## ⚙️ Funcionalidades implementadas

### 1️⃣ Validación de contraseña (evento `input`)
- Usa **expresiones regulares** para verificar:
  - Mínimo 8 caracteres  
  - Una mayúscula  
  - Un número  
  - Un símbolo especial  

- Muestra un mensaje dinámico con color verde o rojo bajo el campo según la validez.  
- El mensaje se actualiza en tiempo real sin recargar la página.

#### 🔹 Evidencias del DOM:
- Creación dinámica del mensaje de ayuda con `document.createElement()`.
- Modificación del contenido con `textContent`.
- Cambio de estilos (`style.color`) en función del resultado.

---

### 2️⃣ Botón de “mostrar/ocultar contraseña” (evento `click`)
- Situado dentro del campo de texto, con icono de **ojo cerrado/abierto**.  
- Cambia de estado visual y funcional sin mover el layout.  
- Usa `classList.toggle()` para alternar entre clases `eye-open` y `eye-closed`.

#### 🔹 Evidencias del DOM:
- Manipulación de atributos (`type`, `aria-label`).
- Modificación de clases CSS dinámicamente.
- Uso de `classList.toggle()` (requisito del PDF).

---

### 3️⃣ Envío del formulario (evento `submit`)
- Si la contraseña no cumple los requisitos, el formulario **no se envía**.  
- Muestra un mensaje de error accesible con color rojo.  
- En caso correcto, muestra un `alert` de confirmación de registro exitoso.

---

## 🧠 Buenas prácticas aplicadas

- Uso de **`const`** y **`let`** en lugar de `var`.  
- Función pura `validarPassword(password)` con valor de retorno booleano.  
- Código modular, comentado y con nombres de variables descriptivos.  
- Sin manejadores inline (`onclick`), todo con `addEventListener`.  
- Sin uso de métodos obsoletos (`document.write`, `innerHTML` inseguro, etc.).  
- Atributos ARIA y estructura semántica HTML correcta.  
- Carga del script con `defer` para mejorar el rendimiento y cumplir las normas modernas.

---

## 📘 Aprendizajes

Durante esta práctica aprendimos:
- Cómo usar **eventos** de JavaScript para detectar acciones del usuario.  
- A manipular el **DOM** para crear, modificar y eliminar elementos en tiempo real.  
- La importancia de las **buenas prácticas modernas**: separar HTML, CSS y JS, evitar inline handlers y escribir código limpio y semántico.  
- Cómo aplicar principios de **usabilidad y accesibilidad**, por ejemplo al mantener un botón dentro del campo sin que se desplace al mostrar mensajes.

---
