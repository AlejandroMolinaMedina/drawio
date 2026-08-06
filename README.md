# Arquitectura de Infraestructura Docker Swarm

Este repositorio contiene la documentación técnica y los diagramas de arquitectura para la implementación de un cluster de **Docker Swarm** de alta disponibilidad, incluyendo configuraciones de balanceo de carga y pipelines de despliegue continuo.

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-Cloud-blue?style=for-the-badge)

---

## Características Principales

- **Diseño de Alta Disponibilidad:** Documentación detallada sobre la topología de red y despliegue de nodos en Docker Swarm.
- **Balanceo de Carga:** Configuración de Application Load Balancers (ALB) para la distribución eficiente del tráfico hacia los servicios del cluster.
- **CI/CD Automatizado:** Esquemas de referencia para la integración y despliegue continuo en entornos de contenedores.
- **Documentación Visual:** Diagramas técnicos exportables y editables en formato `.drawio` para facilitar la comprensión del diseño de red y sistemas.

---

## Estructura del Proyecto

```text
.
├── diagrams/
│   ├── ALB/                      # Documentación del Balanceador de Carga
│   ├── swarm-cicd/               # Flujos de trabajo de integración continua
│   └── swarm-infrastructure/     # Topología de nodos Docker Swarm
├── changes.txt                   # Registro de cambios del proyecto
└── structure.txt                 # Definición de la estructura del repositorio
```

---

## Guía de Uso

Los diagramas están disponibles en formato `.svg` para visualización directa y en formato `.drawio` para ediciones personalizadas mediante [draw.io](https://app.diagrams.net/).

1. **Exploración:** Navega por los subdirectorios dentro de `./diagrams/` para encontrar la documentación específica de cada componente.
2. **Visualización:** Haz clic en los archivos `.svg` para visualizar los esquemas de arquitectura.
3. **Edición:** Importa los archivos `.drawio` en tu herramienta de diagramación preferida para realizar ajustes en la infraestructura.

---

## Soporte y Documentación

Para dudas técnicas sobre la implementación o reporte de inconsistencias en los diagramas:

- **Issues:** Utiliza la sección de [Issues](../../issues) del repositorio para reportar errores o solicitar mejoras.
- **Documentación Adicional:** Consulta los archivos `README.md` ubicados dentro de cada carpeta en `./diagrams/` para detalles específicos de diseño.

---

## Mantenimiento y Contribución

Este repositorio está abierto a mejoras en la documentación y esquemas de infraestructura.

- **Contribuciones:** Si deseas sugerir cambios, realiza un *Fork* del repositorio y envía un *Pull Request*.
- **Código de Conducta:** Se espera que todos los colaboradores mantengan un entorno profesional y respetuoso.
- **Mantenedores:** Este proyecto es mantenido por el equipo de DevOps/Infraestructura.