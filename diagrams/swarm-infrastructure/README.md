# Arquitectura de Docker Swarm

Este directorio contiene diagramas de arquitectura para un despliegue de Docker Swarm a nivel de infraestructura.

## Diagrama de Arquitectura

![Arquitectura de Docker Swarm](DockerSwarm.drawio.svg)

## Visión General
Este diagrama ilustra el diseño fundamental de un clúster de Docker Swarm. Muestra cómo se organizan los nodos y los servicios para garantizar alta disponibilidad y escalabilidad.

## Componentes Clave
- **Manager Nodes**: Gestionan el estado del clúster, la programación de tareas y las API de Docker.
- **Worker Nodes**: Ejecutan las tareas (contenedores) asignadas por los nodos gestores.
- **Servicios/Stacks**: Definiciones de alto nivel que describen los contenedores a ejecutar en el clúster.

## Layout de la Infraestructura
El diseño refleja:
- **Alta Disponibilidad**: Distribución de gestores para tolerancia a fallos.
- **Escalabilidad**: Capacidad para añadir o quitar trabajadores de forma dinámica.
- **Redes (Networking)**: Configuración de redes overlay para la comunicación entre servicios.

## Archivos
- `DockerSwarm.drawio`: El archivo fuente de Draw.io.
- `DockerSwarm.drawio.svg`: Versión exportada en SVG para visualización rápida.
