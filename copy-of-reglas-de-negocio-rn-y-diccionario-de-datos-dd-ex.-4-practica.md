---
description: Recordatorio turno dentista | Dentist appointment reminder
cover: >-
  https://images.unsplash.com/photo-1616391182219-e080b4d1043a?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwzfHxkZW50aXN0JTIwYXBwb2ludG1lbnR8ZW58MHx8fHwxNzQ0MzgyMDQ1fDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 5 - Practica

<mark style="color:orange;">**Ejercicio 5 - Exercise 5**</mark>

Spanish:

Tomás tiene pendiente un tratamiento odontológico, ya sacó un turno en la clínica más prestigiosa de la\
ciudad. La misma tiene varios dentistas. No recuerda cuando era el turno, sin embargo no se preocupa,\
sabe que 24 horas antes del mismo recibirá un recordatorio al mail con todos los datos de la visita al\
odontólogo.\
\
a) Realiza una investigación preguntando a familiares o amigos si recibieron recordatorios de turnos\
en el último tiempo. En lo posible pídeles que te envíen una foto o captura de pantalla del\
recordatorio , utiliza este recordatorio como base para armar un diccionario de datos.

English:

Tomás has an upcoming dental treatment; he has already booked an appointment at the most prestigious clinic in the city. The clinic has several dentists. He doesn’t remember when the appointment is, but he isn’t worried – he knows that 24 hours beforehand, he will receive a reminder email with all the details of his visit to the dentist.

**a)** Conduct some research by asking family members or friends if they have received any appointment reminders recently. If possible, ask them to send you a photo or screenshot of the reminder. Use this reminder as a basis to create a data dictionary.

***

<mark style="color:green;">**Solution:**</mark>

<figure><img src=".gitbook/assets/Captura de pantalla 2025-04-11 141924.jpg" alt=""><figcaption><p>Captura de pantalla de un recordatorio del turno</p></figcaption></figure>

**Reglas de Negocio & Diccionario de Datos:**

**Reglas de Negocio:**

* **Inferencias (Inferences):** \
  Para ser atendido por un odontologo se necesita un turno previo.\
  Es necesario presentarse en el establecimiento un tiempo antes previo a ser atendido. \
  Es una buena practica asistir con buen higiene bucal al turno con el dentista.
* **Hechos (Facts):** \
  Previo al turno se debe dar aviso si la consulta sera por obra social o particular.\
  Todas las tareas administrativas, compo por ejemplo dar los turnos, se hacen a traves del personal administrativo.&#x20;
* **Restricciones (Constraints)**: \
  La consulta se realiza de manera presencial\
  Se necesita un turno previo para ser atendido, a menos que sea una emergencia.&#x20;
* **Calculos (Computations):** Cada tipo de practica poseen diferentes costos.&#x20;
* **Acciones disparadoras (action enablers):** Al final la consulta, el profesional evaluara si es necesario realizar una o varias positivas posteriores a la misma.

**Diccionario de Datos:**

e: turnoDentista = fecha(e) + direccion + nombreOftalmologo + consulta(d) + precioConsulta

fecha(e) = fecha + hora\
consulta(d) = \[particular | obra social]

s: facturaPrestacion = 1{tipoDePractica}n + precioConsulta &#x20;

**Tipo de Evento:** Evento externo
