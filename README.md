# Pro-ASIXc1D-G5
Projecte Transversal ASIXc 2024-2025

Bienvenido al manual de Documentación del Grupo 5
---
## Indice
1. [Proposta CPD](#ejercicio-1)
2. [Implantación de los servicios de Audio y Video](#ejercicio-2)
3. [Diseño e implementación de una Base de Datos](#ejercicio-3)
4. [Sostenibilidad](#ejercicio-4)

---
<!-- Ejercicio 1 -->
# Ejercicio 1
## Propuesta de CPD
 - Para iniciar, hemos organizado las posibles propuestas para montar nuestro CPD para que cumpla con los requisitos que se piden en el proyecto.


---
<!-- Ejercicio 2 -->
# Ejercicio 2
## Implantación de los servicios de Audio y Video

**- Implantación de un servidor de Audio:** Hemos instalado un servidor de audio que nos permite gestionar transmisiones en tiempo real para nuestros clientes y usuarios. La infraestructura debe ser capaz de soportar el volumen de tráfico generado por este tipo de servicio, sin comprometer la calidad del contenido. Además, hemos realizado diversas comprobaciones para asegurarnos de que nuestra red pueda gestionar de manera eficiente este tráfico.


**- Implantación de un servidor de Streaming Video:** Otro de los servicios es el streaming de video. Hemos solicitado la implementación de un servidor que permita una distribución fluida y de calidad de nuestro contenido audiovisual. Al mismo tiempo, hemos hecho diversas pruebas para evitar saturaciones en la red y garantizar una experiencia de usuario óptima, maximizando el uso responsable de los recursos disponibles.


**- Comprobaciones de Ancho de banda:** Las comprobaciones de ancho de banda serán una prioridad para asegurarnos de que el sistema diseñado pueda gestionar adecuadamente los flujos simultáneos de audio y video sin pérdidas de calidad ni colapsos en la red. Queremos una solución que optimice el uso de la infraestructura existente y minimice el impacto ambiental de los servicios que ofrecemos.



---
<!-- Ejercicio 3 -->
# Ejercicio 3
## Diseño e implementación de una Base de Datos

En esta parte del proyecto hemos tenido que idear y crear una base de datos para la gestión de los clientes cumpliendo los requisitos que se indican.

Primeramente, hemos hecho el diseño Entidad-Relación con los datos que se muestran: (Empleados, Niveles de Grupo y Departamentos), indicando en cada uno de ellos su *clave primaria*, los diferentes atributos que tienen y relacionando las entidades entre sí.

![Entidad-Relación](bd/Entidad-Relación.png) 


Seguidamente, hemos realizado la transformación relacional del diseño Entidad-Relación anterior como primer paso antes de empezar la implementación de los datos reales dentro del gestor de bases de datos.

Una vez ya teniendo los datos de los convenios correspondientes y ya hecha la transformación relacional del diseño previo, ya podíamos comenzar con la implementación al gestor de bases de datos. (MySQL)

Hemos creado las tablas de cada una de las Entidades, añadiendo los atributos necesarios con un límite de caracteres e indicando si son la clave primaria, clave foránea, números decimales, números enteros...



---
<!-- Ejercicio 4 -->
# Ejercicio 4
## Sostenibilidad

Hemos seguido con los Objetivos de Desarrollo Sostenible (ODS) y los valores del Institut Tecnològic de Barcelona para desarrollar un proyecto con enfoque sostenible y eficiente.

Con ello en mente, hemos ideado las siguientes medidas:

### Acciones sostenibles implementadas
- Uso de proveedores cloud con energía renovable.
- Virtualización y consolidación de servicios para reducir el número de máquinas.
- Monitorización del rendimiento para evitar consumos innecesarios.
- Elección de regiones cloud con menor huella de carbono.

### Estimación de impacto ambiental
- Consumo energético anual estimado: ~2.400 kWh
- Emisiones estimadas de CO₂: ~960 kg CO₂/año  
  (Reducible usando regiones cloud con energía 100% renovable)

### Medidas adicionales
- Apagado automático de servicios fuera del horario laboral.
- Uso de instancias cloud con eficiencia energética certificada.
- Implementación de autoscaling para optimizar recursos.
- Promoción de buenas prácticas TIC sostenibles entre los usuarios.


