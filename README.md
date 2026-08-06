# Biblioteca de Arquitecturas de Infraestructura

Este repositorio centraliza un catálogo estandarizado de patrones de arquitectura, diseñado para documentar y compartir diseños de infraestructura empresarial listos para producción. Proporciona una base técnica para equipos de ingeniería y DevOps enfocada en la escalabilidad, alta disponibilidad y automatización.

![Docker Swarm](https://img.shields.io/badge/Orquestación-Docker%20Swarm-blue)
![Arquitectura](https://img.shields.io/badge/Tipo-Infraestructura%20as%20Code-green)
![Estado](https://img.shields.io/badge/Estado-Activo-success)

## Características Principales

- **Estandarización:** Modelos de referencia reutilizables para topologías de red y orquestación.
- **Alta Disponibilidad (HA):** Diseños validados para nodos de control y tolerancia a fallos.
- **Balanceo de Carga:** Patrones de integración con Application Load Balancers (ALB) para la gestión eficiente del tráfico.
- **Automatización CI/CD:** Definición de flujos para ciclos de entrega continua y despliegues sin tiempo de inactividad.
- **Documentación Visual:** Diagramas esquemáticos vectoriales (.svg) y archivos editables (.drawio) para facilitar la adopción.

## Estructura del Proyecto

La organización sigue una jerarquía modular basada en componentes tecnológicos:

```text
.
├── diagrams/
│   ├── ALB/                      # Configuración de balanceadores de carga
│   ├── swarm-cicd/               # Flujos de integración y despliegue continuo
│   └── swarm-infrastructure/     # Topología de red y quórum del clúster
└── README.md
```

## Patrones Disponibles

### 1. Docker Swarm Infrastructure
Arquitectura base para el despliegue de clústeres. Incluye la configuración de la red overlay, comunicación entre nodos y estrategias de quórum para los nodos manager.
- [Ver documentación y diagramas](./diagrams/swarm-infrastructure/)

### 2. Application Load Balancer (ALB)
Patrón para la gestión de tráfico de entrada, terminación SSL y distribución hacia los nodos trabajadores del clúster.
- [Ver documentación y diagramas](./diagrams/ALB/)

### 3. CI/CD Pipeline para Swarm
Flujos de trabajo automatizados para la integración de registros de contenedores y ejecuciones de *rolling updates*.
- [Ver documentación y diagramas](./diagrams/swarm-cicd/)

## Visualización de Diagramas

Todos los patrones incluyen archivos en formato `.drawio` para edición y archivos `.svg` para visualización directa. Puede editar los archivos de diseño utilizando:
- **[app.diagrams.net](https://app.diagrams.net)**: Cargar el archivo `.drawio` directamente en su navegador.
- **Extensiones de IDE**: Utilizando el plugin de Draw.io en VS Code o IntelliJ.

## Guía de Uso

1. **Exploración**: Navegue por el directorio `diagrams/` para encontrar el patrón de arquitectura necesario para su caso de uso.
2. **Validación**: Revise el `README.md` específico dentro de cada subcarpeta para consultar las decisiones de diseño y configuraciones recomendadas.
3. **Implementación**: Utilice los diagramas como referencia técnica para la configuración de sus entornos de infraestructura.

## Mantenimiento y Contribución

Esta biblioteca es mantenida por el equipo de Arquitectura y DevOps. Para proponer nuevos patrones o mejoras:

1. Realice un **Fork** del repositorio.
2. Cree una rama para su mejora.
3. Asegúrese de incluir el archivo fuente `.drawio` y la versión exportada `.svg`.
4. Envíe un **Pull Request** detallando las decisiones de diseño y ventajas del nuevo patrón.

Para soporte técnico o consultas sobre la arquitectura, abra un *Issue* en este repositorio.