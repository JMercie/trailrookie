---
title: "No/Low code tools Vs Coding en Salesforce. ¡Hablemos al respecto!"
draft: false
date: "2020-12-10"
tags: ["post", "Automations", "Flows", "Apex"]
type: "post"
image: "cover.jpg"
comment: true
categories: ["Developer", "Admin"]
---

**Leyeron el título y algunos** seguramente ya tenían al ganador en su mente, eso seguro. Pero realmente, hablemos sobre este duelo y porque, en nuestra opinión (spoiler alert) no tiene ganador.
En Salesforce, como ya sabemos los que trabajamos en la plataforma y también nuestros lectores más nuevos, tenemos diversas herramientas Point-and-Click que no requieren el mínimo conocimiento de desarrollo para lograr realizar automatizaciones en tu entorno de trabajo que logren satisfacer desde simples hasta complicados requerimientos de negocio. Claro tiene sus limitaciones, pero cada día son menores, ya que hay un gran equipo del lado de Salesforce que cada release nos trae mejoras y nuevas formas de sacar provecho a las mismas.

**En esta contienda, desde la esquina roja, ¡tenemos a… Cloudy!** y representando, las dos herramientas de automatización más conocidas y las que seguramente habrás usado alguna vez; ya sea en trailhead para completar un módulo o en tu trabajo: **Lightning Flow y Process Builder**. Ambas son bastante poderosas, con ellas puedes realizar acciones cuando se crea, actualiza, elimina o se restablece un registro. Podes llamar otros procesos similares como hijos, invocar clases apex, iniciar procesos de aprobación, realizar una acción basada en el tiempo… Vaya, que lo que puedes hacer es un montón para ser unas herramientas que no requieren escribir una línea de código.

**Y en la esquina azul, ¡tenemos a… Codey!** y representado, encontraremos al lenguaje de programación Apex. Nuestro first class citizen en Salesforce y el utilizado para realizar toda operación desde el lado del backend en la plataforma, con el podemos realizar casi cualquier requerimiento de negocio que se presente desde automatizaciones, integraciones con 3rd party apps, API’s, actualizar, crear, eliminar y buscar registros. Más allá de los governor limits, las limitaciones son pocas y al igual que las herramientas de Point-and-Click, hay un equipo interesado y trabajando constantemente en la mejora de la experiencia del desarrollador al emplearlo, lo cual aprovechamos de agradecer.

### ¿Por qué hablamos de que esto es una contienda?

**Salesforce recomienda siempre mantener una relación 80-20** entre lo que es Point-and-Click y código (en ese orden). Más desde la realidad, normalmente es difícil, sino imposible en diversos casos, mantener esta relación y ya donde se avoca el mayor esfuerzo y desarrollo termina siendo una decisión de los arquitectos a cargo de la implementación del proyecto.  
De lado y lado pueden pasar cosas muy malas si no se mantiene un balance entre ambos. Cuando te abocas 100% al código o al menos, en su mayoría para configuración, terminas con un entorno muy difícil y costoso de mantener actualizado y libre de errores. Por otro lado, si pasa lo contrario, y nos abocamos al 100% a las herramientas Point-and-Click, terminamos realizando automatizaciones por demás complejas (innecesariamente) que dañan el performance de la organización, tenes poco y nada reutilizable y poco escalable con grandes volúmenes de datos.
Codey y Cloudy, Point-and-Click y Apex, no son enemigos, sino **compañeros**. Están ahí para cubrir la espalda del otro cuando uno no puede realizar la tarea. De esta forma se pensó y es la mejor práctica complementar siempre el uno con el otro, si bien aprovechar el gran poder de herramientas como Flow y process builder debe ser tu primera opción, recuerda también pensar en lo que ya está en la org, si es lo mejor ahora, ¿lo será en un futuro? Luego de estas preguntas, creemos que es seguro proceder con lo que convenga, dependiendo de tus respuestas a las mismas.

¡Suenan las campanas, y el referee declara un empate!

> P.D No uses un Flow para procesar gran cantidad de registros o una SOQL query en un loop, te observamos. 🧐
