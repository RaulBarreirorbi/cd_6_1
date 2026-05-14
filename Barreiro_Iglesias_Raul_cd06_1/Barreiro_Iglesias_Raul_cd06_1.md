# TaskMaster - Aplicación de Gestión de Tareas

## Descripción

TaskMaster es una aplicación diseñada para mejorar la productividad, permitiendo gestionar tareas de manera eficiente. Con esta herramienta, los usuarios pueden organizar sus actividades diarias de manera sencilla y eficaz.

## Características

- Creación y edición de tareas.
- Asignación de fechas límites y prioridades.
  - Prioridad baja, media, alta.
  - Fechas límite personalizadas con control de calendario.
- Organización en categorías y etiquetas.
- Marcar tareas como completadas.
- Notificaciones y recordatorios automáticos.
- Visualización en lista y tablero Kanban.
  
## Instalación

Para instalar y ejecutar la aplicación, sigue los siguientes pasos:

```Bash
\# Clonar el repositorio
git clone https://github.com/usuario/taskmaster.git
cd taskmaster

\# Instalar dependencias
npm install

\# Ejecutar la aplicación
npm start
```

## Uso de la api

Taskmaster proporciona una API REST para gestionar tareas. A continuación, un ejemplo de cómo crear una tarea usando **JavaScript**:

```JavaScript
fetch("https://api.taskmaster.com/tareas", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ titulo: "Nueva tarea", prioridad: "Alta" })
})
.then(response => response.json())
.then(data => console.log("Tarea creada:", data));
```

## Fórmula de productividad

La eficiencia del usuario se calcula con la siguiente fórmula:
$$ E = \frac {TAREAS \ COMPLETADAS}{TAREAS \ TOTALES} X 100 $$

Donde:
- $E$ es la eficiencia en porcentaje.
- $Tareas Completadas$ es el número de tareas finalizadas por el usuario.
- $Tareas Totales$ es el número total de tareas asignadas.

## Diagrama de clases

La siguiente representación en UML muestra la estructura del sistema:

```Mermaid
classDiagram
    class Usuario{
    - nombre: String
    - email: String
    +agregarTarea(tarea: Tarea): void
    +eliminarTarea(tarea : Tarea) : void
    }
    class Tarea{
    - titulo: String
    - prioridad: String
    - completada: Boolean
    + marcarComoCompletada() : void
    }
    Usuario "1"--> "*" Tarea : asigna
```

## Capturas de pantalla

A continuación, una vista previa de la interfaz de usuario:

![Captura](image.png)