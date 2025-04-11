# 📱🎮 Questify

> **Convierte tus objetivos diarios en una aventura épica**  
> Una aplicación móvil que te motiva a lograr tus metas diarias a través de mecánicas gamificadas inspiradas en RPG.


[![Licencia MIT](https://img.shields.io/badge/licencia-MIT-blue)](LICENSE)
[![Unity](https://img.shields.io/badge/Unity-2021.3.0f1-blueviolet)](https://unity.com/)
[![C#](https://img.shields.io/badge/C%23-language-orange)](https://docs.microsoft.com/dotnet/csharp/)
[![SQL](https://img.shields.io/badge/SQL-database-yellow)](https://www.mysql.com/)

---

## Índice 🗂️
- [Descripción general](#descripción-general)
- [Características](#características)
- [Tecnologías](#tecnologías)
- [Arquitectura y Diseño](#arquitectura-y-diseño)
- [Plan de Desarrollo](#plan-de-desarrollo)
- [Instalación y Ejecución](#instalación-y-ejecución)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)
- [Contacto](#contacto)

---

## Descripción general 📖

Esta aplicación es una herramienta motivacional diseñada para gestionar tus objetivos diarios y transformarlos en una experiencia divertida. A medida que alcanzas tus metas, acumulas experiencia, desbloqueas logros y haces avanzar a un personaje virtual con características de RPG.

---

## Características ✨

- **Gestión de Objetivos Diarios** 📝  
  Crea, edita y sigue tus metas diarias de forma intuitiva.

- **Progreso y Experiencia** 🚀  
  Gana experiencia por cada objetivo cumplido y sube de nivel.

- **Sistema de Logros y Recompensas** 🏆  
  Desbloquea hitos y consigue recompensas a medida que avanzas.

- **Interfaz Gamificada** 🎨  
  Disfruta de una experiencia visual inspirada en juegos RPG.

- **Alertas y Recordatorios** ⏰  
  Recibe notificaciones para mantenerte enfocado en tus objetivos.

---
## Funcionalidades y Mecánicas de Questify 🎯🎮

En esta aplicación, la experiencia del usuario se enriquece mediante un sistema de gamificación que involucra la creación de metas personales, la participación en una misión mensual y la medición del progreso a través de una barra de XP, que se traduce en niveles y recompensas.

### ¿Los usuarios crearán sus propias metas? ✍️
Sí, los usuarios serán los responsables de crear y personalizar sus propias metas diarias. Cada meta puede ser adaptada a sus necesidades y se le asignará una duración estimada que puede ser de 1 a 5 horas. Esto les permitirá planificar y gestionar sus actividades de forma flexible.

### ¿Habrá misiones prediseñadas? 🗓️
Además de las metas personales, la aplicación ofrecerá una **misión mensual** prediseñada enfocada en fomentar hábitos saludables y mantener un estilo de vida equilibrado. Por ejemplo, algunas de estas misiones podrían incluir:
- Recordatorios para quedar con nuestro mejor amigo/a.
- Desafío de correr 1 km.
- Llamar a nuestros padres y tener una charla con ellos.

Esta misión mensual busca impulsar acciones que mejoren el bienestar personal y social, actuando como complemento a las metas individuales.

### ¿Cómo se mide el progreso? 📈
El progreso del usuario se visualizará a través de una **barra de XP** que se irá completando conforme se realicen las tareas asignadas:
- Cada tarea cuenta con un tiempo establecido (1 a 5 horas).
- Por cada hora planificada y completada, se añade **1 punto de XP**.
- Al acumular **20 puntos de XP**, el usuario sube de nivel.

### ¿Qué tipo de recompensas o retroalimentación se da? 🏆
La aplicación recompensa la constancia y la fidelidad del usuario mediante:
- **Niveles:** Cada 20 puntos de XP equivale a un nivel alcanzado.
- **Medallitas de Recompensa:** Por cada 10 niveles alcanzados, el usuario recibirá una medallita. Esta medalla simboliza el compromiso y la constancia en el cumplimiento de las metas, además de servir como incentivo para continuar progresando.

---

## Tecnologías 🛠️

El proyecto se desarrollará utilizando las siguientes tecnologías:

- **C#**  
  Lenguaje principal para el desarrollo y la lógica de la aplicación.

- **Unity**  
  Motor de desarrollo que facilita la creación de interfaces interactivas y la implementación de elementos gamificados.

- **SQL**  
  Base de datos para la gestión y almacenamiento de usuarios, objetivos y logros.

---

## Arquitectura y Diseño (MVC) 🏗️

El proyecto seguirá el patrón **Modelo-Vista-Controlador (MVC)**, un enfoque de diseño que facilita la separación de responsabilidades en el desarrollo de software. Gracias a MVC, podremos mantener la lógica de negocio, la presentación y el manejo de datos de forma independiente, lo que simplifica el mantenimiento, las pruebas y la escalabilidad de la aplicación.

### ¿Qué es el patrón MVC?

El patrón MVC divide la aplicación en tres componentes principales:

- **Modelo (Model) 📊:**  
  Es la capa encargada de la gestión de datos y de la lógica de negocio. Aquí se definen las estructuras de datos, las reglas y las funciones que manipulan la información, como la creación, actualización y eliminación de registros en la base de datos SQL.

- **Vista (View) 👀:**  
  Es la interfaz de usuario y la parte visual de la aplicación. Se encarga de mostrar la información que proviene del Modelo de forma interactiva y atractiva. En nuestro caso, Unity se utilizará para diseñar esta capa, presentando el progreso del usuario, los logros y la evolución del personaje con elementos gráficos y animaciones.

- **Controlador (Controller) 🎮:**  
  Actúa como intermediario entre el Modelo y la Vista. El Controlador interpreta las acciones del usuario (por ejemplo, cuando se marca un objetivo como completado), actualiza el Modelo y solicita a la Vista que se refresque para reflejar los cambios. Esta capa coordina la interacción entre la lógica de negocio y la presentación.

### Aplicación del MVC en el Proyecto

- **Modelo (Model) 📊**
  - **Responsabilidades:**  
    - Gestionar y validar los datos (objetivos diarios, experiencia, logros, perfiles de usuario, etc.).
    - Realizar operaciones CRUD (crear, leer, actualizar, borrar) en la base de datos SQL.
  - **Ejemplo en la app:**  
    - Al completar un objetivo, el modelo actualiza la experiencia acumulada y registra el logro en la base de datos.

- **Vista (View) 👀**
  - **Responsabilidades:**  
    - Mostrar de manera atractiva la interfaz de usuario utilizando Unity.
    - Presentar de forma clara los objetivos diarios, las notificaciones, el progreso del personaje y los logros desbloqueados.
  - **Ejemplo en la app:**  
    - Pantallas y animaciones que reflejan el avance, como el incremento de niveles o la aparición de nuevos logros.

- **Controlador (Controller) 🎮**
  - **Responsabilidades:**  
    - Recibir y procesar las interacciones del usuario (por ejemplo, hacer clic en "objetivo completado").
    - Invocar las funciones del Modelo para actualizar los datos.
    - Coordinar con la Vista para actualizar la interfaz según los cambios en los datos.
  - **Ejemplo en la app:**  
    - Un controlador que, al detectar la finalización de un objetivo, solicita al Modelo que incremente la experiencia y, a continuación, manda una señal a la Vista para que muestre una animación de avance.

---

## Plan de Desarrollo 📅

El desarrollo se llevará a cabo en las siguientes fases:

1. **Investigación y Análisis** 🔍  
   Estudio de aplicaciones similares y metodologías de gamificación.

2. **Diseño de la Aplicación** 🎨  
   Creación de wireframes, mockups y diagramas de arquitectura.

3. **Desarrollo del MVP** 🚧  
   - Configuración del entorno en Unity y desarrollo en C#.  
   - Implementación de la gestión de objetivos y conexión a la base de datos SQL.

4. **Integración de Gamificación** 🏅  
   Implementación del sistema de experiencia, logros y progreso del personaje.

5. **Pruebas y Optimización** 🛠️  
   Sesiones de testing y ajustes para optimizar la experiencia de usuario.

6. **Documentación y Lanzamiento** 🚀  
   Elaboración de la documentación técnica y preparación para la presentación final.

---

## Instalación y Ejecución 📥

> **Nota:** Las instrucciones pueden ajustarse conforme avance el desarrollo.

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/N4thaniel446/TFG.git
   cd TFG
