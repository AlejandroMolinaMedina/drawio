# Diagrama de Docker Swarm

Este directorio contiene un diagrama que ilustra la arquitectura de Docker Swarm enfocada en un flujo de CI/CD.

## Diagrama

![Arquitectura Docker Swarm](DockerSwarm.drawio.svg)

## Visión General
Este diagrama detalla cómo se automatiza la integración y despliegue continuo (CI/CD) dentro de un entorno orquestado por Docker Swarm. El objetivo principal es asegurar entregas rápidas y consistentes de aplicaciones.

## Componentes Clave
- **Clúster de Docker Swarm**: Entorno de ejecución compuesto por nodos gestores (Managers) y trabajadores (Workers).
- **Herramienta de Automatización (N8N)**: Orquestador encargado de ejecutar la lógica de despliegue tras detectar cambios.
- **Webhook**: Mecanismo que dispara el proceso de CI/CD al recibir notificaciones de eventos (e.g., nuevos commits).

## Flujo de Trabajo
El diagrama ilustra el siguiente flujo:
1. **Desarrollo**: Los cambios se envían al repositorio.
2. **Revisión**: Se gestionan las actualizaciones mediante Pull Requests.
3. **Automatización**: N8N detecta el cambio mediante un Webhook.
4. **Despliegue**: N8N coordina con el Manager Node para actualizar los servicios en los Worker Nodes.

## Archivos
- `DockerSwarm.drawio`: El archivo fuente de Draw.io.
- `DockerSwarm.drawio.svg`: Versión exportada en SVG.
