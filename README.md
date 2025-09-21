# C# Agent Movement & AI

Este repositorio implementa y prueba un sistema de **movimiento de personajes** e **inteligencia artificial (IA)** en C#, usando Unity como motor gráfico. Está orientado al desarrollo y experimentación con agentes autónomos capaces de desplazarse y tomar decisiones en su entorno.

## Características principales

- **Lógica de movimiento** programable para personajes y agentes.
- **Sistemas de inteligencia artificial** para controlar el comportamiento de los personajes (por ejemplo: búsqueda, patrullaje, evasión, etc.).
- **Modularidad** para separar la lógica de movimiento de la de IA, permitiendo experimentar y mezclar distintos algoritmos.
- **Enfoque educativo y experimental**: fácil de modificar y ampliar.

## Estructura del repositorio

- `/src`: Código fuente en C# del sistema de movimiento y IA.
- `/agents`: Ejemplos de agentes y personajes programados.
- `/scenarios`: Escenarios y mapas para probar los comportamientos implementados.
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
