<- [[Inicio]]
## Introducción

El enfoque tradicional de desarrollo de software que sigue las fases de Planificación, Análisis de Requisitos, Diseño, Implementación, Pruebas y Mantenimiento, conocido como el modelo en cascada, tiende a separar claramente las responsabilidades entre el equipo de desarrollo y el equipo de operaciones (sysadmin).

![[desarrollo-de-software-tradicional-o-cascada.png|600]]

## Inconvenientes/desventajas del enfoque

 En un contexto de desarrollo de software moderno, donde se busca agilidad, colaboración y entrega continua, este enfoque puede ocasionar varios inconvenientes. Algunos de ellos a resaltar son:

1. **Silencios y falta de comunicación**
    
	- Los equipos de desarrollo y operaciones suelen trabajar en "silos", lo que genera barreras de comunicación y colaboración. Esto puede llevar a malentendidos y retrasos en la entrega de funcionalidades, ya que cada equipo puede tener sus propias prioridades y metodologías de trabajo.

2. **Lentitud en la entrega de software**:    
    
	- La estricta separación de tareas y responsabilidades entre desarrollo y operaciones ralentiza la entrega de software. Los desarrolladores crean el software y lo pasan a operaciones, lo que puede generar cuellos de botella, especialmente si hay problemas de compatibilidad o configuraciones que no se tuvieron en cuenta durante el desarrollo.

3. **Problemas en la gestión de cambios**:

  - La integración de cambios se vuelve compleja y riesgosa, ya que las modificaciones hechas por los desarrolladores deben ser validadas y adaptadas por el equipo de operaciones, lo cual puede no estar alineado con la frecuencia de entregas que requieren los entornos modernos.

3. **Menor capacidad de respuesta ante fallos o incidentes**:
    
    - En caso de problemas en producción, la resolución puede tardar más tiempo, ya que los desarrolladores y el equipo de operaciones podrían no compartir el mismo contexto o conocimiento del problema, lo que complica la identificación y solución de los errores.
1. **Infraestructura como un obstáculo, no como una ventaja**:
    
    - El equipo de operaciones puede no estar involucrado lo suficiente en las primeras etapas del ciclo de desarrollo, lo que lleva a que la infraestructura se vea como un obstáculo en lugar de una ventaja estratégica. Esto puede resultar en problemas de escalabilidad y rendimiento no anticipados.
1. **Falta de automatización**:
    
    - La separación de roles puede llevar a la falta de automatización en el proceso de entrega de software, lo cual es fundamental en enfoques modernos como DevOps. La falta de integración continua y entrega continua (CI/CD) puede resultar en procesos manuales que son lentos y propensos a errores.
1. **Entornos inconsistentes**:
    
    - Los desarrolladores suelen trabajar en entornos de desarrollo que no reflejan con precisión los entornos de producción gestionados por el equipo de operaciones. Esto puede llevar a la frase común de "funciona en mi máquina", pero falla en producción debido a configuraciones y dependencias diferentes.
1. **Baja moral y sentido de propiedad compartida**:
    
    - La separación de funciones y responsabilidades puede resultar en una baja moral entre los equipos debido a la falta de sentido de propiedad compartida. Los desarrolladores pueden sentir que su trabajo se termina cuando entregan el código, y el equipo de operaciones puede sentirse abrumado con la responsabilidad de mantener el sistema sin una comprensión completa del código base.
1. **Costos operativos más altos**:
    
    - La falta de colaboración puede llevar a costos operativos más altos debido a la ineficiencia en la implementación y mantenimiento del software. Además, los procesos manuales y la duplicación de esfuerzos son comunes en este tipo de dinámicas.
1. **Menor alineación con las necesidades del negocio**:
    
    - En los modelos tradicionales, puede haber una desconexión entre lo que se está desarrollando y las necesidades reales del negocio o del usuario final, ya que los equipos de operaciones y desarrollo no están sincronizados en objetivos y métricas de éxito.
<- [[Inicio]]
