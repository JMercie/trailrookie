---
title: "¿Salesforce y tecnologías Open Source? Entrevista a Julián Duque, Lead Developer Advocate de Heroku"
draft: false
date: 2020-11-24T11:43:52-03:00
tags: ["post", "general", "Heroku", "Javascript"]
type: "post"
image: "cover.jpg
"
comment: true
categories: ["Developer"]
---

La semana pasada pudimos entrevistar a [Julián Duque](https://www.linkedin.com/in/juliandavidduque), colombiano viviendo en Estados Unidos hace unos años y que actualmente trabaja como lead developer advocate en Salesforce, más precisamente en el equipo de **HEROKU**, hace poco más de un año.
La principal función de su trabajo es la de “crear un puente entre los desarrolladores que utilizan el producto y el producto como tal” generando contenido multimedia y desarrollando a la comunidad.

**¿Qué es heroku?**

Heroku es una **PLATAFORMA COMO SERVICIO (PaaS)** para poder desplegar aplicaciones desarrolladas con **LENGUAJE DE PROGRAMACIÓN OPEN SOURCE** (Por ejemplo: php, NodeJS, Python, Ruby, etc.) que nos permitan tener experiencia de usuarios bastante personalizadas.
Además, no solo te permite desplegar la aplicación, si no que existen servicios de datos en los cuales podrías crear una base de datos para tu aplicación con tecnologías open source de BD como PostgreSQL, Redis, Apache Kafka.
Además, tiene una capa de integración con SALESFORCE mediante Heroku Connect que permite hacer una sincronización bidireccional con la base de datos que tengamos en heroku.
Todo esto permite que desarrolladores que no conocen la forma de desarrollar aplicaciones en Salesforce (por ejemplo, que no conozcan SOQL o SFDX) puedan acceder a los datos de Salesforce manejando lenguajes o tecnologías que efectivamente conocen.

La idea de heroku es simplificar todo el trabajo de infraestructura y mantenimiento de operaciones de una aplicación permitiendo que los desarrolladores solo se concentren en el desarrollo de la aplicación y el negocio.

Heroku es parte de la oferta Pro Code para poder extender aplicaciones de Salesforce para poder ofrecer experiencias de usuario personalizadas.

**Están saliendo muchas cosas open source relacionadas a Salesforce, lo cual ayuda mucho para hacer crecer a la comunidad. Aparte de heroku, ¿notas que hay una tendencia de lanzar herramientas para atraer a cada vez más desarrolladores externos hacia Salesforce?**

En Salesforce se empieza a poner a JavaScript como un protagonista o nativo para desarrollar aplicaciones en la plataforma. empezando por Lightning Web Components, la librería de componentes web de Salesforce, muy utilizado para desarrollar layouts en Salesforce, pero también podrían usarlo para desarrollar aplicaciones externas a SF.
Uno de los casos de uso donde se podrían desplegar aplicaciones LWC open source es en heroku.
Hace poco lanzamos una aplicación llamada [Ecars](https://github.com/trailheadapps/ecars) en la [sample gallery de trailhead](https://trailhead.salesforce.com/sample-gallery), donde mantenemos los diferentes ejemplos de aplicaciones con buenas prácticas desarrolladas para la plataforma. Ecars es una de las pocas aplicaciones que utiliza toda la plataforma, especialmente la mezcla de cómo hacer una aplicación de SF que utilice Heroku. Los LWC se reutilizan tanto fuera como dentro de Salesforce, además tiene diferentes microservicios escritos en Nodejs, con JavaScript y TypeScript, base de datos en PostgreSQL, técnicas de maneja de información orientadas a IOT, etc. Lo cual es muy llamativo para desarrolladores que tienen skills en frontend o backend y quieren sacar provecho de todo lo que Salesforce ofrece.

Ya para hablar del futuro, en Dreamforce 2019, se anunció una tecnología llamada en ese entonces SALESFORCE EVERGREEN y este año se renombró a SALESFORCE FUNCTIONS. Un nuevo producto (ya lanzado como piloto abierto), es una solución serverless para Salesforce. En la misma yo tengo una infraestructura para correr funciones donde yo no me tengo que preocupar por la escalabilidad, recursos o límites, simplemente yo voy a utilizar este entorno de ejecución para delegar ciertas funciones que sería muy costoso a nivel de recursos (no económicos sino de CPU, memorias, recursos físicos) en plataforma Salesforce, de esta manera delegamos a un entorno de ejecución elástico y que permite crecer a medida que se le demande más trabajo.
Lo interesante de este entorno de Salesforce functions es que se van a poder utilizar lenguajes open source (en este caso NodeJS, pero hay planes para soportar JAVA) pero más que el lenguaje de programación en sí, lo interesante es todo ese ecosistema que hay alrededor de ese lenguaje de programación.
Un ejemplo: Quiero crear una aplicación para vender tickets de un concierto. Creo en Salesforce toda la estructura para manejar los contactos, los tickets, etc., pero quiero generar los tickets que vengan en un pdf con código QR para enviar por email a los usuarios. Entonces ahora hay 3 problemas que tengo que ver cómo resolver en Salesforce, como generar el pdf, como generar el QR y cómo enviar el correcto. Debo averiguar qué productos del AppExchange me sirven para esto, como comunicarse entre sí, como género algo personalizado, me debo preocupar por la escalabilidad. Termino necesitando un servicio externo para esto, y algo externo implica un montón de preguntas acerca de seguridad, comunicación, etc.
Con Salesforce Functions, van a poder realizar funciones que se encarguen de hacer esas operaciones, integrables 100% con Salesforce sin autenticación ni configuración adicional. Las funciones corren dentro de la plataforma, pero en este entorno de ejecución elástico del que hablaba antes y, adicionalmente, van a poder utilizar todas las librerías y plugin que otros desarrolladores creado para realizar estas operaciones que necesitan (por ejemplo
las librerías de NPM de JavaScript). Las funciones no van a estar regidas por los government limits entonces no se van a tener que preocupar por la escalabilidad y también va a permitir acercar desarrolladores externos a Salesforce “sin tanta fricción”.
Eso no significa que APEX va a desaparecer, sigue siendo el lenguaje nativo de SF, pero se ofrece esta alternativa para poder extender las posibilidades de Salesforce.

**En cuanto a la cultura Salesforce, Ohana y demás, vos desde adentro, fuera de lo que es la tecnología, ¿cómo ves todo esto?**

Yo vengo trabajando durante más de 15 años en la industria del software y tuve la suerte de trabajar en muy buenas compañías y equipos y cuando apliqué a Salesforce tenía un poco de recelo hacia afiliarse a una mega compañía gigante como Salesforce. Y habiendo trabajado para empresas más pequeñas se me manifestaron un montón de dudas acerca de si iba a ser uno más entre los más de 50 mil empleados o si mi trabajo iba a hacerse notar e impactar.
En mi primer mes me sentía completamente perdido, ya que entre a una empresa totalmente distinta a lo que estaba acostumbrado. Pero la sorpresa fue diferente, la calidad humana de las personas que trabajan ahí pero también la calidad humana de la empresa. Uno puede trabajar en una compañía donde interesa el resultado, tienes un proyecto y solo interesa que se termine el mismo en el tiempo definido, eres un recurso más que vale tantos dólares la hora. En cambio, en Salesforce importa más uno como ser humano, si uno está bien el resultado de lo que uno haga va a estar bien, y si uno está mal el resultado no va a ser óptimo, entonces la PRIORIDAD ES QUE UNO ESTÉ BIEN.
por ejemplo, durante la pandemia, con todas las consecuencias que tuvo para el trabajo y las personas, Salesforce nos ha invitado mucho a velar y cuidarnos a nosotros mismos. Nos dieron algunos viernes libres para dedicarlo a lo personal y a desestresarnos. Nos permite elegir un día donde no se programan reuniones para poder concentrarse en el trabajo sin distracciones. programas semanales para hacer break, con clases temáticas como por ejemplo kickboxing o meditación o alimentación sana. Hay un montón de espacios, para los que lo quieran utilizar, para trabajar en esa paz mental y evitar preocupaciones personales.
Como compañía han hecho una labor muy fuerte en mantenernos tranquilos y enfocados, se nota mucho que le importamos como humanos. OHANA puede sonar muy de marketing para mucha gente, pero desde adentro se nota que si de verdad hay mucho interés por el bienestar de los empleados.
Veo un lugar donde puedo hacer una carrera y donde puedo planificar trabajar durante más de 5 años. Algo muy difícil en el mercado actual de sistemas donde uno cambia de trabajo como cambia de ropa.

Para mí ha sido algo totalmente diferente y la compañía me ha demostrado que hay muchas formas de impactar a la comunidad todavía.
Es una compañía que entiende lo valiosa que es la comunidad y que hay que potenciar. Los miembros de la comunidad Salesforce tienen mucha pasión por el producto atravesados por el cambio que Salesforce le ha permitido en su vida. Las personas que estaban apasionadas por el producto empiezan a estar apasionadas por lo que hay detrás del producto y ayudan a potenciar la comunidad.

**Última pregunta, ¿qué consejos le puedes dar a las personas que recién empiezan en IT, no solo desarrolladores si no en general?**

Primero que hay muchos recursos online para aprender, por ejemplo, trailhead para lo que es Salesforce.

Segundo, van a tener dificultades, errores, momentos de frustración, dudas sobre si todo esto vale la pena. Sepan que eso es normal, todos pasamos por eso, pero lo importante es tener un objetivo claro y continuar en base a eso.

Tercero, no transiten este camino solos, frustrarse estando solo hace más fácil abandonar el proceso. Únanse a comunidades, participen en lugares donde estén interesados. La pandemia hizo esto mucho más fácil ya que las reuniones son en línea y en todo el mundo.
