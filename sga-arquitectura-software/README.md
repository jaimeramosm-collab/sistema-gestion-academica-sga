# Diseño de la arquitectura de software de un Sistema de Gestión Académica (SGA)

Trabajo de la asignatura **Arquitectura de Software** – Corporación Unificada Nacional de Educación Superior (CUN).

- **Integrantes:** [nombres del equipo]
- **Docente:** [nombre del docente]
- **Video de sustentación (YouTube):** [enlace]

## ¿Qué es este repositorio?

Contiene la **documentación de diseño** del SGA: informe, modelos del sistema y evidencias del
uso de Google AI Studio.

> **Alcance honesto:** este trabajo es de **diseño**. No se implementó el sistema.
> Las verificaciones descritas en el informe (pruebas de carga, de concurrencia, de
> restauración, etc.) son un **plan de pruebas propuesto**, no resultados obtenidos.
> [Si el equipo implementó algo, indicarlo aquí.]

## Arquitectura en una línea

Monolito modular con capas internas, API REST (OpenAPI), PostgreSQL con réplica,
dos instancias de aplicación detrás de un balanceador y auditoría en la misma transacción.
Tecnología propuesta: Java 21 + Spring Boot 3 (backend), React + TypeScript (frontend), PostgreSQL 16.

## Estructura

| Carpeta | Contenido |
|---|---|
| `docs/` | Informe final (Word; el PDF de entrega se exporta desde este archivo) |
| `diagramas/imagenes/` | Casos de uso, componentes, despliegue, datos y secuencia (PNG) |
| `diagramas/fuente/` | Archivos fuente de los diagramas (Mermaid y Graphviz) |
| `ia/` | Prompts usados y capturas de Google AI Studio |

## Modelos incluidos

1. Casos de uso (`uc`)
2. Componentes / vista lógica (`comp`)
3. Despliegue (`dep`)
4. Datos conceptual (`er`)
5. Secuencia: matrícula de un estudiante (`seq`)

## Datos sensibles

No se incluyen datos personales reales ni credenciales en prompts, capturas o archivos.
