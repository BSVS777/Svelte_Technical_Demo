````md
<div align="center">

# ⚡ Svelte Lab Manager

### Demo técnica de reactividad, componentes y renderizado dinámico con Svelte 5

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=FF3E00&center=true&vCenter=true&width=700&lines=Reactividad+con+%24state;Valores+derivados+con+%24derived;Componentes+reutilizables;Demo+t%C3%A9cnica+en+vivo" alt="Typing SVG" />

<br />

![Svelte](https://img.shields.io/badge/Svelte-5-FF3E00?style=for-the-badge&logo=svelte&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-8-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES2024-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Status](https://img.shields.io/badge/Status-Demo%20Funcional-22C55E?style=for-the-badge)

</div>

---

## 📌 Descripción del proyecto

**Svelte Lab Manager** es una aplicación web sencilla desarrollada con **Svelte 5** para demostrar los conceptos principales del framework de forma práctica, clara y ejecutable en vivo.

La aplicación funciona como un pequeño gestor de tareas académicas. Permite agregar tareas, asignarles una prioridad, marcarlas como completadas, reabrirlas o eliminarlas. Aunque la funcionalidad es simple, cada parte de la demo está diseñada para representar una característica técnica importante de Svelte.

El objetivo principal no es construir una aplicación empresarial completa, sino aislar y demostrar de manera controlada los elementos clave del framework: reactividad, componentes, eventos, renderizado condicional y actualización automática de la interfaz.

---

## 🎯 Objetivo de la demo

Esta demo fue creada para una presentación técnica en vivo sobre **Svelte**, mostrando cómo este framework permite construir interfaces dinámicas con menos código repetitivo y una experiencia de desarrollo más directa.

La demostración busca responder tres preguntas principales:

- ¿Cómo maneja Svelte el estado reactivo?
- ¿Cómo se actualiza la interfaz cuando cambian los datos?
- ¿Cómo se separa una interfaz en componentes reutilizables?

---

## ✨ Funcionalidades principales

- Agregar nuevas tareas.
- Asignar prioridad: **Alta**, **Media** o **Baja**.
- Marcar tareas como completadas.
- Reabrir tareas completadas.
- Eliminar tareas.
- Validar que no se agreguen tareas vacías.
- Mostrar estadísticas reactivas:
  - Total de tareas.
  - Tareas completadas.
  - Tareas pendientes.
- Separar la interfaz en componentes reutilizables.
- Permitir modificaciones pequeñas durante la demo en vivo.

---

## 🧠 Conceptos de Svelte demostrados

| Concepto                | Implementación en la demo                          |
| ----------------------- | -------------------------------------------------- |
| `$state`                | Manejo del estado principal de la aplicación       |
| `$derived`              | Cálculo automático de estadísticas                 |
| Componentes             | Separación entre `App.svelte` y `TaskItem.svelte`  |
| Props                   | Envío de datos del componente padre al hijo        |
| Eventos                 | Acciones para agregar, completar y eliminar tareas |
| Renderizado condicional | Mensaje cuando no existen tareas                   |
| Listas dinámicas        | Renderizado de tareas con `{#each}`                |
| Clases dinámicas        | Cambio visual cuando una tarea está completada     |
| Validación              | Prevención de tareas vacías                        |

---

## 🧩 Estructura del proyecto

```txt
SVELTE_TECHNICAL_DEMO/
├─ index.html
├─ package.json
├─ vite.config.js
├─ src/
│  ├─ app.css
│  ├─ App.svelte
│  ├─ main.js
│  └─ TaskItem.svelte
└─ README.md
```
````

---

## 🚀 Instalación y ejecución

### 1. Clonar el repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

### 2. Entrar a la carpeta del proyecto

```bash
cd SVELTE_TECHNICAL_DEMO
```

### 3. Instalar dependencias

```bash
npm install
```

### 4. Ejecutar el servidor de desarrollo

```bash
npm run dev
```

### 5. Abrir en el navegador

```txt
http://localhost:5173/
```

---

## 🛠️ Scripts disponibles

| Comando           | Descripción                                  |
| ----------------- | -------------------------------------------- |
| `npm run dev`     | Ejecuta la aplicación en modo desarrollo     |
| `npm run build`   | Genera la versión optimizada para producción |
| `npm run preview` | Previsualiza la versión de producción        |

---

## 🔥 ¿Por qué esta demo representa Svelte?

Esta demo representa Svelte porque muestra su forma principal de trabajar: construir interfaces reactivas mediante componentes declarativos que luego son compilados a JavaScript optimizado.

En lugar de manipular manualmente el DOM, la aplicación actualiza la interfaz automáticamente cuando cambia el estado. Por ejemplo, al agregar, completar o eliminar una tarea, los contadores de tareas se recalculan sin escribir lógica adicional para actualizar la vista.

Esto demuestra una de las ventajas principales de Svelte: permite escribir código más directo, legible y enfocado en la lógica de la aplicación.

---

## 🧪 Modificaciones posibles durante la demo en vivo

La demo está preparada para aceptar cambios pequeños en tiempo real, por ejemplo:

### Agregar una nueva prioridad

```svelte
<option>Urgente</option>
```

### Cambiar el mensaje cuando no hay tareas

```svelte
<p>No hay tareas pendientes. Todo bajo control.</p>
```

### Limitar la cantidad máxima de tareas

```js
if (tasks.length >= 5) {
  error = "Solo se permiten 5 tareas en esta demo.";
  return;
}
```

Estas modificaciones permiten demostrar que el código es propio, entendible y adaptable durante la presentación.

---

## ⚖️ Comparativa breve: Svelte vs React

| Aspecto           | Svelte                                     | React                                      |
| ----------------- | ------------------------------------------ | ------------------------------------------ |
| Enfoque           | Compilador                                 | Librería basada en runtime                 |
| Reactividad       | Directa mediante `$state` y `$derived`     | Basada en hooks como `useState`            |
| Código repetitivo | Menor                                      | Mayor                                      |
| Curva inicial     | Más simple                                 | Más amplia                                 |
| Ecosistema        | Más pequeño, pero en crecimiento           | Muy grande y consolidado                   |
| Ideal para        | Interfaces rápidas, ligeras e interactivas | Aplicaciones grandes con ecosistema amplio |

---

## 📚 Tecnologías utilizadas

- **Svelte 5**
- **Vite**
- **JavaScript**
- **HTML**
- **CSS**

---

## 👥 Integrantes

| Nombre                  | Rol                                       |
| ----------------------- | ----------------------------------------- |
| Nombre del integrante 1 | Investigación, explicación técnica y demo |
| Nombre del integrante 2 | Desarrollo, ejecución y defensa técnica   |

---

## ✅ Estado del proyecto

```txt
✔ Proyecto funcional
✔ Código propio
✔ Demo ejecutable en vivo
✔ Componentes separados
✔ Reactividad implementada
✔ Preparado para modificaciones durante la presentación
```

---

## 📸 Vista general de la demo

```txt
┌──────────────────────────────────────┐
│          Svelte Lab Manager          │
├──────────────────────────────────────┤
│ Nueva tarea                          │
│ [ Practicar preguntas del docente ]  │
│ [ Prioridad: Media ] [ Agregar ]     │
├──────────────────────────────────────┤
│ Total: 2 | Completadas: 1 | Pend: 1  │
├──────────────────────────────────────┤
│ ✓ Probar demo en vivo                │
│ ○ Preparar explicación de Svelte     │
└──────────────────────────────────────┘
```

---

## 🧾 Conclusión

**Svelte Lab Manager** demuestra de forma breve pero completa cómo Svelte permite crear interfaces modernas, reactivas y organizadas con una sintaxis clara y poco boilerplate.

La demo no busca ser una aplicación compleja, sino una muestra técnica precisa de los elementos más importantes del framework. Esto permite explicar el funcionamiento interno de Svelte, defender el código durante el Q&A y realizar cambios en vivo sin depender de ejemplos pregrabados o código externo.

---

<div align="center">

### ⚡ Built with Svelte 5

**Código simple. Reactividad clara. Demo lista para producción académica.**

</div>
```
