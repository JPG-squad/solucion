# Portal de conversaciones

👋 ¡Bienvenidos a nuestro proyecto! 

## Descripción del proyecto

### 🤔 Problema
La Cruz Roja se enfrenta al problema de que los procesos de acogida y valoración, realizados como primer contacto con un usuario a través de entrevistas y formularios específicos, pueden ser largos y fríos, lo que puede afectar negativamente la experiencia del usuario y reducir su participación en los programas y servicios de la ONG. Para mejorar la eficiencia de este proceso y crear un primer contacto más cálido y acogedor, Cruz Roja busca una solución innovadora que automatice el proceso de acogida y valoración y permita a los entrevistadores obtener los beneficios de una mejor atención sin tener que completar formularios. 


### 💡 Solución

Para abordar el problema de eficiencia en el proceso de valoración, hemos creado una solución innovadora llamada "Portal de conversaciones". Esta plataforma es una herramienta de software basada en la nube, alojada en Amazon Web Services (AWS), que permite a los entrevistadores de Cruz Roja realizar la valoración de los usuarios sin tener que llenar formularios, lo que reduce significativamente el tiempo necesario para completar el proceso.

La plataforma utiliza tecnologías como Transcribe, OpenAI i Deepgram para analizar y procesar los datos de la entrevista y generar un informe detallado del usuario. Además, la plataforma ofrece una interfaz visual intuitiva para que los entrevistadores puedan interactuar con los resultados de la valoración y hacer un seguimiento de los usuarios a lo largo del tiempo.

El "Portal de conversaciones" es una solución innovadora ya que puede procesar en tiempo real una conversación y marcar los puntos clave o preguntas que ya se han hablado en ese momento. Además, gracias a su diseño modular, la plataforma puede adaptarse fácilmente a las necesidades específicas de la Cruz Roja y puede extenderse a otras aplicaciones.

## Table of Contents

- [Portal de conversaciones](#portal-de-conversaciones)
  - [Descripción del proyecto](#descripción-del-proyecto)
    - [🤔 Problema](#-problema)
    - [💡 Solución](#-solución)
  - [Table of Contents](#table-of-contents)
  - [Diagrama de Arquitectura](#diagrama-de-arquitectura)
  - [Descripción técnica](#descripción-técnica)
    - [Software](#software)
      - [Repositorios](#repositorios)
      - [Diagrama relacional](#diagrama-relacional)
      - [🔧 Funcionalidades](#-funcionalidades)
        - [1. Iniciar sesión](#1-iniciar-sesión)
        - [2. Modificar mi perfil](#2-modificar-mi-perfil)
        - [3. Añadir un usuario](#3-añadir-un-usuario)
        - [4. Ordenar usuarios](#4-ordenar-usuarios)
        - [5. Subir conversación](#5-subir-conversación)
        - [6. Ver transcripción](#6-ver-transcripción)
        - [7. Saber más](#7-saber-más)
        - [8. Reproducir conversación](#8-reproducir-conversación)
        - [9. Ficha de usuario](#9-ficha-de-usuario)
        - [10. Grabar conversación](#10-grabar-conversación)
        - [11. Buscador](#11-buscador)
        - [12. Ver notificaciones](#12-ver-notificaciones)
    - [Arquitectura Cloud AWS](#arquitectura-cloud-aws)
      - [Descripción](#descripción)
      - [Repositorios](#repositorios-1)
      - [Recuperación de desastres \& TEST de DRP](#recuperación-de-desastres--test-de-drp)
      - [AWS Pilars](#aws-pilars)
        - [Excelencia operativa](#excelencia-operativa)
        - [Seguridad](#seguridad)
        - [Fiabilidad](#fiabilidad)
        - [Eficiencia del rendimiento](#eficiencia-del-rendimiento)
        - [Optimización de costos](#optimización-de-costos)
        - [Sostenibilidad](#sostenibilidad)
  - [⏭️ Demo](#️-demo)
  - [👥 Team Members](#-team-members)
  - [⏭️ Trabajo futuro](#️-trabajo-futuro)
  - [🎉 Conclusión](#-conclusión)

## Diagrama de Arquitectura

![Arquitectura AWS](img/architecture.svg)

## Descripción técnica

### Software

#### Repositorios

- [Frontend](https://github.com/JPG-squad/front) 

[![React Icon](https://img.shields.io/badge/-React-blue?logo=react&logoColor=white&style=flat)](https://reactjs.org/)
[![JavaScript Icon](https://img.shields.io/badge/-JavaScript-yellow?logo=javascript&logoColor=white&style=flat)](https://www.javascript.com/)


- [Backend](https://github.com/JPG-squad/back)

[![Python Icon](https://img.shields.io/badge/-Python-yellow?logo=python&logoColor=white&style=flat)](https://www.python.org/)
[![Django Icon](https://img.shields.io/badge/-Django-green?logo=django&logoColor=white&style=flat)](https://www.djangoproject.com/)
[![PostgreSQL Icon](https://img.shields.io/badge/-PostgreSQL-blue?logo=postgresql&logoColor=white&style=flat)](https://www.postgresql.org/)
[![OpenSearch Icon](https://img.shields.io/badge/-OpenSearch-blue?logo=amazon-aws&logoColor=white&style=flat)](https://opensearch.org/)
[![Docker Icon](https://img.shields.io/badge/-Docker-blue?logo=docker&logoColor=white&style=flat)](https://www.docker.com/)


- [Research IA ( Not used )](https://github.com/JPG-squad/back)
  
[![Python Icon](https://img.shields.io/badge/-Python-yellow?logo=python&logoColor=white&style=flat)](https://www.python.org/)
[![FastAPI Icon](https://img.shields.io/badge/-FastAPI-blue?logo=fastapi&logoColor=white&style=flat)](https://fastapi.tiangolo.com/)
[![Docker Icon](https://img.shields.io/badge/-Docker-blue?logo=docker&logoColor=white&style=flat)](https://www.docker.com/)


#### Diagrama relacional

A continuación, se muestra el diagrama relacional de los modelos de la base de datos utilizados en la plataforma:

![Ejemplo de imagen](HackatonModel.drawio.png)

#### 🔧 Funcionalidades

A continuación, se enumeran todas las funcionalidades que ofrece el Portal de conversaciones:

- [1. Iniciar sesión](#1-iniciar-sesión)
- [2. Modificar mi perfil](#2-modificar-mi-perfil)
- [3. Añadir un usuario](#3-añadir-un-usuario)
- [4. Ordenar usuarios](#4-ordenar-usuarios)
- [5. Subir conversación](#5-subir-conversación)
- [6. Ver transcripción](#6-ver-transcripción)
- [7. Saber más](#7-saber-más)
- [8. Reproducir conversación](#8-reproducir-conversación)
- [9. Ficha de usuario](#9-ficha-de-usuario)
- [10. Grabar conversación](#10-grabar-conversación)
- [11. Buscador](#11-buscador)
- [12. Ver notificaciones](#12-ver-notificaciones)

##### 1. Iniciar sesión
La funcionalidad de inicio de sesión es la primera en la plataforma, permitiendo a los usuarios acceder a su cuenta a través de su correo electrónico y contraseña registrados previamente. Estos datos deben estar almacenados en nuestra base de datos como un "Empleado".

[link demo login]

##### 2. Modificar mi perfil
Esta funcionalidad te permite actualizar la información de tu cuenta en la plataforma. Para acceder a esta funcionalidad, haz clic en el icono de tu perfil ubicado en la esquina superior derecha de la pantalla. Verás que aparecerá un menú desplegable con varias opciones, entre ellas "Editar mi perfil". Al seleccionar esta opción, podrás editar tus datos personales, por ahora solo tu nombre. También puedes cerrar sesión desde este mismo menú.

La funcionalidad ahora mismo no tiene mucho sentido pero esta pensada por si en un futuro un empleado tiene más campos editables.

[link demo modificar mi perfil y logout]

##### 3. Añadir un usuario
Para empezar una conversación, es necesario añadir un usuario. En la parte izquierda de la plataforma, encontrarás el listado de usuarios y podrás agregar uno nuevo. Solo necesitas introducir su nombre y correo electrónico, y opcionalmente, su número de teléfono. Cuando agregues al usuario, aparecerá en la parte superior de la lista y podrás comenzar una conversación con él o ella desde la parte derecha de la plataforma.

[link demo añadir usuario]

##### 4. Ordenar usuarios
En la sección de listado de usuarios, encontrarás diversas opciones para ordenarlos y facilitar su búsqueda. Podrás ordenarlos alfabéticamente o por el grado de interacción con ellos. Esto te permitirá encontrar rápidamente al usuario con el que quieres conversar y mejorar la eficiencia de tus interacciones en la plataforma.

[link demo filtrar usuarios]

##### 5. Subir conversación

Una vez seleccionado un usuario, verás un botón rojo con un icono de "+" en la parte inferior derecha de la plataforma. Al pulsar este botón, se abrirán dos opciones. 

La primera opción te permitirá subir una conversación en múltiples formatos, como Wav, Mp3 y Webm. Además, podrás seleccionar el modelo de inteligencia artificial que procesará la conversación. 

Por ahora, puedes escoger entre AWS Transcribe y Deepgram. Mientras se procesa la conversación, verás un mensaje de carga en la parte inferior central de la plataforma. Una gran ventaja de nuestra plataforma es que podrás seguir navegando e interactuando con ella mientras se procesa la conversación. 

Una vez se haya procesado con éxito, aparecerá un mensaje y una notificación. La conversación se situará arriba del todo en la lista de conversaciones de ese usuario, ya que por defecto están ordenadas por orden de creación. Se habrá generado automáticamente un título identificativo y una descripción breve para esa conversación. 

Además, habrá tres botones que explicaremos más adelante en otras funcionalidades. 

Si esta es la primera conversación, también se generará automáticamente una ficha de usuario, de la cual hablaremos más adelante.

[link demo subir conversación]

##### 6. Ver transcripción
En la carta de una conversación verás una serie de botones en la parte inferior. El primer botón, te permitirá ver la transcripción generada por el modelo de inteligencia artificial que has seleccionado al subir la conversación. La transcripción se mostrará en un formato de chat, donde podrás ver el diálogo que ha tenido lugar durante la conversación. Este formato hace que la transcripción sea más fácil de leer y comprender, permitiendo al usuario identificar rápidamente lo que se ha dicho en cada momento.

[link demo ver transcripción]

##### 7. Saber más
Al lado del botón para ver la transcripción, verás otro botón con el texto "Saber más". Al hacer clic en él, se abrirá una ventana emergente con un campo de texto en el que puedes escribir cualquier pregunta relacionada con la conversación o cualquier detalle que se te haya pasado durante la entrevista. Una vez hayas escrito alguna pregunta, va a aparecer una respuesta en pocos segundos.

Esta funcionalidad te permite asegurarte de que no se te escapa ningún detalle importante y te permite revivir cualquier pregunta que hayas hecho durante la entrevista para recordar las respuestas del usuario.

Además, esta funcionalidad es muy versátil y te permite hacer cualquier tipo de pregunta en el momento. Todo lo que tienes que hacer es escribir la pregunta en el campo de texto y presionar "Enter". Así de fácil.

[link demo preguntas efímeras]

##### 8. Reproducir conversación
Si bien la transcripción es una herramienta útil, en ocasiones puede haber errores o inexactitudes en el texto generado por los modelos de inteligencia artificial. Para evitar esto, nuestra plataforma ofrece la funcionalidad de reproducir la conversación original con el usuario. Cada conversación cuenta con un botón de reproducción en la parte superior derecha. 

Al hacer clic en él, se desplegará un reproductor de audio en la parte inferior central de la pantalla. Desde allí, podrás avanzar o retroceder en la conversación, pausarla y reanudarla sin ningún problema. La gran ventaja de esta funcionalidad es que puedes tener la conversación reproduciéndose mientras realizas otras tareas en la plataforma, como revisar la transcripción o editar la ficha del usuario. De esta manera, tendrás acceso a la fuente original y podrás asegurarte de que la información que manejas es precisa y completa.

[link demo reproductor]

##### 9. Ficha de usuario

##### 10. Grabar conversación

##### 11. Buscador

##### 12. Ver notificaciones

### Arquitectura Cloud AWS

#### Descripción

#### Repositorios

- [Terraform](https://github.com/JPG-squad/terraform) 

[![Terraform Icon](https://img.shields.io/badge/-Terraform-purple?logo=terraform&logoColor=white&style=flat)](https://www.terraform.io/)
[![aws-vault Icon](https://img.shields.io/badge/-aws--vault-orange?logo=amazon-aws&logoColor=white&style=flat)](https://github.com/99designs/aws-vault)

#### Recuperación de desastres & TEST de DRP

Este es nuestro plan de recuperación de desastres para garantizar la disponibilidad y continuidad de nuestros servicios en caso de cualquier imprevisto. El plan consiste en las siguientes acciones:

1. **Backups de base de datos**: Utilizamos el servicio AWS Backups para realizar copias de seguridad de nuestra base de datos y las replicamos a la región de Irlanda para garantizar la redundancia y disponibilidad de nuestros datos.

2. **Imágenes del backend en ECR**: Subimos las imágenes del backend tanto en el ECR de España como en el de Irlanda para tener una copia de seguridad de nuestras imágenes.

3. **Frontend en buckets de S3**: El frontend (web) está alojado en buckets de S3 en España e Irlanda. Al subir el código se hace en ambos buckets a la vez, y nuestra CDN Cloudfront tiene configurado el bucket de España como principal y el de Irlanda como failover.

4. **Bucket S3 en París**: En el servicio de producción, usamos Transcribe en París y por eso necesitamos un bucket de S3 en esa región. Este bucket lo replicamos usando la funcionalidad de S3 a uno igual en la región de Irlanda para tener una copia de seguridad.

5. **Cluster Fargate en Irlanda**: En Irlanda, configuramos un cluster Fargate con las mismas características que el de España, pero sin EC2. El servicio tiene asociado 0 tareas corriendo. Utilizamos healthchecks de Route53 para comprobar si los servicios de las dos regiones están healthy pasando por los ALB, y dependiendo de cuál esté healthy, hacemos failover a Irlanda.

6. **Ejecución del script de DRP**: Cuando hay un desastre, ejecutamos un script manual que crea una base de datos a partir del backup de la de producción. Una vez que la base de datos está creada, actualizamos el servicio de Irlanda corriendo en Fargate, que `desired_count = 1`.

Este modelo de recuperación de desastres se adapta a nuestras necesidades y presupuesto, al mismo tiempo que nos permite cumplir con los pilares de sustentabilidad y optimización de costos. Además, hemos realizado pruebas para asegurarnos de que el plan es efectivo y ha sido exitoso en nuestras últimas pruebas.

Adjunto encontrarás un video de nuestra última prueba de DRP.
<a href="https://www.youtube.com/watch?v=TUZmK0X9zgk">Demostración del Plan de Recuperación de Desastres</a>


#### AWS Pilars

##### Excelencia operativa

1. Realizar operaciones como código: Utilizamos Terraform para desplegar nuestra infraestructura como código. Esto nos permite tener una infraestructura versionada y repetible. El repositorio se encuentra [aquí] (https://github.com/JPG-squad/terraform)
2. Realizar cambios frecuentes, pequeños y reversibles: Hemos establecido un proceso para desplegar cambios en pequeñas incrementos que se pueden revertir rápidamente si surgen problemas, de esta manera podemos identificar fácilmente la causa raíz de cualquier problema y minimizar el tiempo y los recursos necesarios para solucionarlos.
3. Anticiparse al fallo: Hemos estado haciendo pruebas DRP para asegurarnos de que podemos recuperarnos de cualquier fallo. También hemos implementado alarmas y notificaciones para estar al tanto de cualquier problema que pueda surgir. En el siguiente código de Terraform (https://github.com/JPG-squad/terraform/blob/main/global/monitor/alarms.tf) se puede ver cómo hemos implementado las alarmas y también aquí se puede ver un vídeo con la última prueba DRP que realizamos.

##### Seguridad

1. **Implementar una sólida base de identidad**: Utilizamos AWS IAM para gestionar el acceso a los servicios y recursos de AWS de forma segura.
2. **Mantener una configuración segura**: Utilizamos AWS Config para supervisar nuestra infraestructura y asegurarnos de que cumpla con nuestras políticas de seguridad.
3. **Aplicar seguridad en todas las capas**: Utilizamos AWS WAF para proteger nuestra aplicación de exploits web comunes que podrían afectar la disponibilidad de la aplicación, comprometer la seguridad o consumir recursos excesivos. También usamos grupos de seguridad para controlar el tráfico que se permite llegar a cada servicio, por ejemplo, solo permitimos el tráfico desde el balanceador de carga a los servicios backend.
4. **Proteger los datos en tránsito y en reposo**: Utilizamos AWS KMS para gestionar las claves de cifrado que se utilizan para cifrar nuestros datos. También usamos AWS Secrets Manager para los secretos utilizados por nuestros servicios. Los buckets de S3 se cifran por defecto.
5. Prepararse para eventos de seguridad: POR HACER.

##### Fiabilidad

1. **Recuperación automática ante fallos, escalar horizontalmente para aumentar la disponibilidad de carga de trabajo agregada y dejar de adivinar la capacidad**: Para garantizar una alta disponibilidad y resiliencia, utilizamos AWS Auto Scaling para ajustar la capacidad, AWS Load Balancing para distribuir el tráfico y AWS RDS Aurora para una base de datos altamente disponible. Además, el servicio Opensearch se implementa en dos zonas de disponibilidad para obtener redundancia y tolerancia a fallos adicionales. Nuestros servicios se implementan en dos zonas de disponibilidad para obtener redundancia y tolerancia a fallos adicionales. También contamos con un plan DRP para recuperarnos de cualquier fallo.
2. **Probar los procedimientos de recuperación**: Hemos estado haciendo pruebas DRP para asegurarnos de que podemos recuperarnos de cualquier fallo. [Aquí]() se puede ver un vídeo con la última prueba DRP que realizamos.
3. **Gestionar el cambio en la automatización**: Utilizamos Terraform para desplegar nuestra infraestructura como código. Esto nos permite tener una infraestructura versionada y repetible. El repositorio se encuentra [[aquí](https://github.com/JPG-squad/terraform). Sin embargo, actualmente Terraform no se aplica automáticamente, pero esto se puede hacer en el futuro si el equipo crece.

##### Eficiencia del rendimiento

1. **Democratizar tecnologías avanzadas**: Estamos democratizando tecnologías avanzadas mediante el uso de servicios de AWS como ECS, RDS Aurora, OpenSearch, Transcribe, Route53, CloudWatch, S3, ALB y otros. Este enfoque nos permite aprovechar tecnologías como bases de datos SQL, transcodificación de medios y aprendizaje automático sin requerir experiencia especializada de nuestro equipo de TI. También nos permite centrarnos en el desarrollo de productos en lugar de la aprovisionamiento y gestión de recursos.
2. **Globalizarse en minutos**: Usamos AWS CloudFront para entregar contenido a nuestros usuarios con baja latencia y alta velocidad de transferencia. También usamos AWS Route53 para dirigir el tráfico a la región AWS más cercana. Además, estamos ajustando automáticamente la capacidad de nuestros servicios.
3. **Usar arquitecturas sin servidor**: Solo usamos S3, Transcribe, SNS, Fargate (DRP). Y la razón principal es porque queremos tener una arquitectura sin servidor para evitar la necesidad de gestionar servidores y también reducir costos. Sin embargo, estamos utilizando ECS en EC2 para implementar los servicios backend, pero esto se debe a que queremos optimizar costos, ya que Fargate es más caro que ECS.
4. **Considerar la simpatía mecánica**: Para garantizar un acceso eficiente a los datos y un rendimiento óptimo, hemos elegido utilizar OpenSearch para buscar en un gran volumen de conversaciones y PostgreSQL para la lógica central de la plataforma. Al seleccionar estas tecnologías, podemos lograr escalabilidad, confiabilidad y rentabilidad en nuestra arquitectura.

##### Optimización de costos

Además de los puntos comúnmente explicados en el pilar de Optimización de costos, queremos hacer énfasis en que hemos elegido utilizar AWS EC2 on EC2 como solución para nuestra infraestructura de backend. Esto se debe a que las instancias EC2 son más económicas en comparación con Fargate, y en un futuro el ahorro de costos reservando instancias EC2 puede ser aún mayor. Al seleccionar una solución de infraestructura más económica, podemos optimizar nuestros costos y asignar nuestros recursos a otros aspectos críticos del negocio.


1. **Implementar gestión financiera en la nube**: Utilizamos AWS Cost Explorer para visualizar, entender y gestionar nuestros costos y uso de AWS con el tiempo. También podríamos usar AWS Budgets para establecer presupuestos personalizados que nos alerten cuando nuestros costos o uso excedan (o se pronostiquen que excedan) nuestro monto presupuestado, pero esto aún no está implementado.
2. **Adoptar un modelo de consumo**: En primer lugar, hemos detenido la infraestructura EC2 no utilizada que no era necesaria durante las horas de menor actividad o cuando no se necesitaba realizar pruebas. Además, durante la fase de desarrollo, hemos utilizado solo una instancia en lugar de múltiples instancias en múltiples zonas de disponibilidad. Para el período de evaluación, también hemos utilizado solo una instancia para minimizar los costos. En segundo lugar, hemos utilizado AWS RDS con un nivel gratuito ya que la carga de trabajo era suficiente. De manera similar, hemos utilizado OpenSearch con solo un nodo y un nivel gratuito. Este enfoque nos ha ayudado a evitar el consumo innecesario de recursos y nos ha permitido permanecer dentro de nuestro presupuesto limitado de 50 euros. Al adoptar un modelo de consumo, nos hemos asegurado de que solo pagamos por los recursos informáticos que necesitamos y podemos aumentar o disminuir fácilmente el uso según nuestros requisitos empresariales. Esto nos ha ayudado a lograr ahorros significativos de costos mientras mantenemos un alto nivel de rendimiento y confiabilidad en nuestra infraestructura en la nube.
3. **Medir la eficiencia general**: Usando los paneles de CloudWatch, podemos medir la eficiencia general de nuestra infraestructura. Podemos ver el uso de la CPU, el uso de la memoria, el espacio libre restante, la salud de los servicios, etc. Además, tenemos alarmas de CloudWatch para estar al tanto de cualquier problema que pueda surgir.

##### Sostenibilidad

1. **Maximizar la utilización**: Actualmente, estamos cumpliendo con la regla de maximizar la utilización mediante el uso de una sola instancia y la selección del tamaño de instancia más pequeño para cada servicio debido a limitaciones presupuestarias. Sin embargo, hemos tomado medidas para analizar la utilización utilizando el panel de CloudWatch y alarmas, y estamos preparados para escalar según sea necesario para aumentar la utilización y maximizar la eficiencia energética del hardware subyacente.
2. **Anticipar y adoptar nuevas ofertas de hardware y software más eficientes**: Estamos utilizando los nuevos procesadores AWS Graviton diseñados para ofrecer la mejor relación precio-rendimiento para nuestras cargas de trabajo en la nube que se ejecutan en Amazon EC2 con arm. Esto nos permite aprovechar los últimos avances tecnológicos y mejorar la eficiencia de nuestras cargas de trabajo en la nube. Además, hemos diseñado nuestro sistema con flexibilidad en mente, lo que nos permite adoptar rápidamente nuevas tecnologías eficientes a medida que estén disponibles.
3. **Usar servicios administrados**: El uso de servicios administrados como AWS Fargate y las configuraciones de ciclo de vida de Amazon S3 nos permite compartir recursos en una amplia base de clientes, lo que conduce a una reducción de los requisitos de infraestructura para nuestras cargas de trabajo en la nube.

## ⏭️ Demo

## 👥 Team Members

## ⏭️ Trabajo futuro

## 🎉 Conclusión