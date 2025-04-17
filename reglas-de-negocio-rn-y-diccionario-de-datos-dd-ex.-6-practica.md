---
description: Eventos Rosario | Rosario Events
cover: >-
  https://images.unsplash.com/photo-1516450360452-9312f5e86fc7?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxMHx8cGFydHl8ZW58MHx8fHwxNzQ0OTE1NDUxfDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 6 - Practica

<mark style="color:orange;">**Ejercicio 6 - Exercise 6**</mark>

Spanish:

Lo que más me gusta de Rosario es la cantidad de fiestas que hay. Todos las semanas además de\
estudiar, que por supuesto es lo más importante en mi vida, reservo unas horas para ir a alguna fiesta. Hoy&#x20;voy a consultar en la plataforma de Eventos Rosario cuáles son las próximas fechas de fiestas, precios y&#x20;espero que en alguna se convoque a alguna DJ super copada. Micaela ( Argentina)\
\
a) ¿Qué actividad va a realizar Micaela esta semana, además de estudiar?.\
b) Realiza el diccionario de datos para los flujos de entrada y salida asociados a la misma.

English:

What I love most about Rosario is the number of parties there are. Every week, in addition to studying – which of course is the most important thing in my life – I set aside a few hours to go to a party. Today I’m going to check the _Eventos Rosario_ platform to see the upcoming party dates, prices, and hopefully one of them will feature a really cool DJ. Micaela (Argentina)\
\
**a)** What activity is Micaela going to do this week, besides studying?\
**b)** Create the data dictionary for the input and output flows associated with that activity.

***

<mark style="color:green;">**Solution:**</mark>

**Reglas de Negocio & Diccionario de Datos:**

A) La actividad que va a realizar Micaela es "Buscar a que fiesta/evento puede asistir el fin de semana"&#x20;

**Reglas de Negocio:**

* **Inferencias (Inferences):** Las consultas se realizan de manera online a traves de la pagina web.&#x20;
* **Hechos (Facts):** Los tickets se adquieren a traves del sitio EventosRosario
* **Restricciones (Constraints)**:  Hay que ser mayor de 18 años para asistir a la fiesta.&#x20;

**Diccionario de Datos:**

e: consultarEvento = fecha(e) + precio + (artistaInvitado(d)) + tipoEvento(d)\
fecha(e) = dia + hora\
artistaInvidtado(d) = \[dj | musicoSolista | banda]\
tipoEvento (d) = \[fiesta | cenaShow | boliche | concierto]\
\
s: datosEvento = fecha(e) + precio + (artistaInvitado(d) + tipoEvento(d) + nombreEvento + direccion(e)\
fecha(e) = dia + hora\
artistaInvitado(d) = \[dj + musicoSolista | banda]\
tipoEvento (d) = \[fiesta | cenaShow | boliche | concierto ]

**Tipo de Evento:** Evento externo
