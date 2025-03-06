---
description: Viaje de regreso al pueblo | Journey back to the village
cover: >-
  https://images.unsplash.com/photo-1570125909232-eb263c188f7e?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHx0cmF2ZWwlMjBidXN8ZW58MHx8fHwxNzQwNjg0MjQ5fDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Regla de Negocio (RN) y Diccionario de Datos (DD) - Ex. 1 - Practica

#### <mark style="color:orange;">Ejercicio 1 - Exercise 1</mark>

Spanish:

Hola soy Pedro, estudiante de la carrera de Ingeniería en Sistemas en la ciudad de Rosario. Hace varias semanas que no vuelvo a mi ciudad natal y ya es hora de regresar. Aprovechando el feriado de semana santa voy a averiguar por cuál empresa y en qué horario me conviene viajar el día jueves 28/03. Si bien el precio del pasaje es un factor importante a considerar, para tomar la decisión de en cual compañía comprar, me interesa principalmente encontrar un viaje directo con una duración corta, sinceramente no quiero pensar las 8 horas que demoraría en un “lechero”. \
\
a) Según este relato. ¿Cuál es la primera actividad que deberá realizar Pedro para poder viajar?. Enuncia la misma. \
b) Realiza el diccionario de datos de flujos de entrada y salida. \
c) Mediante un ejemplo realiza una muestra de datos para el Flujo de Salida.

English:

Hi, I'm Pedro, a student of Systems Engineering in the city of Rosario. I haven't been back to my hometown for several weeks and it's time to go back. Taking advantage of the Easter holiday I'm going to find out which company and at what time it's convenient for me to travel on Thursday 28/03. Although the price of the ticket is an important factor to consider when deciding which company to buy from, I am mainly interested in finding a direct journey with a short duration, I honestly don't want to think about the 8 hours it would take on a ‘milkman’.

a) According to this story, what is the first activity that Pedro will have to do in order to travel?  \
b) Make a data dictionary of incoming and outgoing flows. \
c) By means of an example, make a sample of data for the Outflow.



***

<mark style="color:green;">**Solution:**</mark>&#x20;

a) La primera actividad que se debe realizar para poder viajar, es seleccionar la empresa con la cual realizar el viaje

**Reglas de Negocio & Diccionario de Datos:**&#x20;

**Reglas de Negocio:**\
**. Hech﻿os:** El colectivo sale desde la terminal de omnibus \
**. Restricciones:** Ser mayor de 18 años para viajar solo, presentarse con el dni al momento de subir al bus. \
. **Inferencias:** Brindar el numero de dni a la hora de sacar el boleto

**Diccionario de Datos:**\
e: consultaViaje = empresa + fechaViaje(e)\
s: EmisionBoleto = fechaViaje(e) + precioPasaje + tipoDeViaje(d) \
\
fechaViaje(e)  = dia + mes + año + hora\
tipoDeViaje(d) = char(5); \[largo | corto]&#x20;

**Tipo de Evento:** Evento Temporal
