# Arquitectura de Infraestructura Docker Swarm

Este repositorio contiene la documentación técnica y los diagramas de arquitectura para la implementación de un clúster de **Docker Swarm**. El proyecto se enfoca en la orquestación de contenedores, la gestión de alta disponibilidad mediante Application Load Balancers (ALB) y la integración de flujos de CI/CD para despliegues automatizados.

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Swarm](https://img.shields.io/badge/Docker_Swarm-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## Características Principales

*   **Alta Disponibilidad**: Configuración de nodos de orquestación para asegurar la continuidad del servicio.
*   **Balanceo de Carga**: Implementación de Application Load Balancers (ALB) para la distribución eficiente del tráfico.
*   **Automatización de CI/CD**: Flujos definidos para la integración y despliegue continuo en entornos de clúster.
*   **Documentación Visual**: Diagramas de arquitectura detallados para la infraestructura y los pipelines de despliegue.

## Estructura del Proyecto

La estructura del repositorio está organizada para separar la documentación técnica y los diagramas por componentes críticos:

```text
.
├── diagrams/
│   ├── ALB/                      # Diagramas de Application Load Balancer
│   ├── swarm-cicd/               # Diagramas de pipelines CI/CD
│   └── swarm-infrastructure/     # Diagramas de la topología de Docker Swarm
```

### Detalle de Directorios
*   `/diagrams/ALB`: Contiene archivos `.drawio` y sus exportaciones en SVG que describen la topología de entrada de tráfico.
*   `/diagrams/swarm-cicd`: Visualización del ciclo de vida de los despliegues automatizados.
*   `/diagrams/swarm-infrastructure`: Esquema detallado de la comunicación entre nodos manager y worker en el clúster.

## Guía de Inicio Rápido

Para visualizar los diagramas presentes en este repositorio, se recomienda utilizar [Draw.io](https://app.diagrams.net/) o cualquier visor de archivos SVG.

### Requisitos Previos
1.  **Docker Engine**: Instalado en cada nodo participante.
2.  **Acceso SSH**: Configurado para la gestión de los nodos del clúster.
3.  **Draw.io Integration**: Recomendado para editar los archivos `.drawio`.

### Inicialización de Swarm
Para desplegar el clúster basándose en los diagramas de infraestructura:

```bash
# Iniciar el nodo manager
docker swarm init --advertise-addr <IP-DEL-NODO>

# Unir nodos workers (ejecutar en cada worker)
docker swarm join --token <TOKEN> <IP-MANAGER>:2377
```

## Soporte y Documentación

*   **Reporte de errores**: Utiliza la sección de *Issues* del repositorio para reportar discrepancias en los diagramas o problemas de infraestructura.
*   **Documentación adicional**: Consulta los archivos `README.md` ubicados dentro de cada subdirectorio en la carpeta `/diagrams` para obtener detalles técnicos específicos de cada componente.

## Mantenimiento y Contribución

Este proyecto es mantenido por el equipo de DevOps. Las contribuciones son bienvenidas mediante *Pull Requests*. Por favor, asegúrese de:

1.  Actualizar los archivos `.drawio` correspondientes si se realizan cambios en la arquitectura.
2.  Generar una nueva exportación SVG tras cada modificación en los diagramas.
3.  Seguir las convenciones de nomenclatura establecidas en la estructura de archivos.

---
*Este proyecto se distribuye bajo los términos definidos en el archivo `LICENSE`.*