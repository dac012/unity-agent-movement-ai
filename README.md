# C# Agent Movement & AI

Este repositorio implementa y prueba un sistema de **movimiento de personajes** e **inteligencia artificial (IA)** en C#, usando Unity como motor gráfico. Está orientado al desarrollo y experimentación con agentes autónomos capaces de desplazarse y tomar decisiones en su entorno.

## Características principales

- **Lógica de movimiento** programable para personajes y agentes.
- **Sistemas de inteligencia artificial** para controlar el comportamiento de los personajes (por ejemplo: búsqueda, patrullaje, evasión, etc.).
- **Modularidad** para separar la lógica de movimiento de la de IA, permitiendo experimentar y mezclar distintos algoritmos.
- **Enfoque educativo y experimental**: fácil de modificar y ampliar.

## Estructura del repositorio

- `Assets/`: Carpeta estándar de Unity que contiene todos los recursos, scripts y escenas del proyecto, incluyendo la lógica de movimiento y la IA de los agentes.
- `Packages/`: Configuración de paquetes utilizada por el proyecto de Unity.
- `ProjectSettings/`: Configuración del proyecto de Unity (inputs, layers, build settings, etc.).
- `.gitignore`, `.collabignore`: Archivos para excluir ficheros y carpetas del control de versiones.
- `README.md`: Este archivo.

## Ejemplo de comportamiento de IA

```csharp
if (agent.CanSee(target))
{
    agent.MoveTowards(target.Position);
}
else
{
    agent.Patrol();
}
```

## ¿Para qué usar este proyecto?

- Como base para prácticas de inteligencia artificial, agentes autónomos o videojuegos en C#.
- Para experimentar con lógicas de movimiento y decisión en personajes no jugadores (NPCs).
- Como punto de partida para sistemas más complejos de simulación o juegos.
