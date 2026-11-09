# Prompts usados en Google AI Studio

Modelo: Gemini 3.8 Flash (búsqueda web desactivada).

## Prompt 1 – Arquitectura base

```
Actúa como arquitecto de software. Diseña la arquitectura de un Sistema de
Gestión Académica (SGA) web para una institución de educación superior que
gestiona estudiantes, docentes, programas, asignaturas, grupos, matrículas,
calificaciones y horarios. Roles: administrador, coordinador académico,
docente y estudiante.

Requisitos clave: HTTPS y contraseñas con hash; 95 % de consultas en menos de
3 s con 300 usuarios concurrentes; disponibilidad 99,5 %; escalabilidad;
bajo acoplamiento; API REST documentada; consistencia en matrículas y
calificaciones; auditoría; respaldo y recuperación; privacidad por rol.

Entrega: (1) estilo arquitectónico recomendado comparando capas, monolito
modular y microservicios, con justificación según el tamaño del sistema;
(2) módulos con responsabilidades e interfaces; (3) tecnologías sugeridas
justificadas; (4) riesgos y puntos únicos de falla.
```

## Prompt 2 – Correcciones y diagramas

```
Gracias. Detecté estos problemas en tu propuesta, corrígelos:
1) Falta un módulo de Reportes (reportes de matriculados, grupos, asignaturas
y resultados, con filtros por periodo y programa) y un módulo de Gestión de
Personas (estudiantes y docentes).
2) La auditoría debe escribirse en la misma transacción que la operación,
no por eventos asíncronos en memoria.
3) Elimina tenant_id (es una sola institución) y deja la infraestructura
neutral, sin depender de AWS.
4) La disponibilidad del 99,5 % es mensual (aprox. 3,6 h/mes).
5) Añade la restricción única contra matrículas duplicadas.
Luego genera en Mermaid: (a) diagrama de casos de uso, (b) diagrama de
componentes, (c) diagrama de despliegue, (d) modelo entidad-relación con
Usuario, Rol, Estudiante, Docente, Programa, Asignatura, PeriodoAcadémico,
Grupo, Matrícula y Calificación con cardinalidades, y (e) secuencia de la
matrícula de un estudiante.
```

Las capturas del prompt y de las respuestas van en la carpeta `capturas/`.
Los diagramas del informe son una versión **corregida por el equipo** de lo
que propuso la IA (ver la tabla de aceptado, modificado y descartado en el informe).
