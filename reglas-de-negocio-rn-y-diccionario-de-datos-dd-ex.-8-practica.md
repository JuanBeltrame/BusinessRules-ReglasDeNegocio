---
description: Reserva Cadena Gastronomica | Gastronomic Chain Reservation
cover: >-
  https://images.unsplash.com/photo-1485217988980-11786ced9454?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwyfHxvbmxpbmUlMjByZXNlcnZhdGlvbnxlbnwwfHx8fDE3NDUwNTEyNjF8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 8 - Practica

<mark style="color:orange;">**Ejercicio 8 - Exercise 8**</mark>

Spanish:

Una reconocida cadena gastronómica de la ciudad habilitó en su página web la opción de realizar reservas.&#x20;Cada reserva se identificará con el número de documento de la persona que la realice. \
Una persona puede&#x20;realizar una única reserva por semana. La cantidad máxima de comensales es 10  personas por reserva.\
\
Existen dos turnos en los cuales se puede reservar: almuerzo y cena. Para cada turno debe indicar el\
horario preferido. Para la hora de almuerzo tenemos 12 y 13:30. Para la cena tenemos: 18:30, 20 y 22\
horas. Existe una tolerancia máxima de espera de 15 minutos, en caso de no presentarse al horario de la\
reserva y de que la tolerancia se exceda, la reserva caducará. \
\
Cuando una persona realiza una reserva&#x20;recibe una constancia de reserva, la misma tiene un número de reserva, la fecha y hora seleccionado y&#x20;demás datos necesarios para que se haga efectiva la reserva. (Inspiración: Paulina)\
\
a) Enunciar la actividad principal que se describe. Escribir los flujos de entrada y de salida para la\
misma.\
b) Enunciar las reglas de negocio.

English:

A well-known restaurant chain in the city has enabled an online booking option on its website.\
Each booking will be identified by the national ID number of the person making the reservation.\
A person may make only one booking per week. The maximum number of diners per booking is 10 people.

There are two time slots available for bookings: lunch and dinner. For each time slot, the preferred time must be selected.\
For lunch, the available times are 12:00 and 13:30.\
For dinner, the available times are 18:30, 20:00, and 22:00.

There is a maximum waiting tolerance of 15 minutes. If the guest does not show up at the booked time and the grace period is exceeded, the booking will be cancelled.

When a person makes a reservation, they receive a booking confirmation, which includes a booking number, the selected date and time, and any other necessary details to validate the reservation.\
&#xNAN;_(Inspired by Paulina)_\
\
**a)** State the main activity being described. Write the input and output flows for it.\
**b)** State the business rules.

***

<mark style="color:green;">**Solution:**</mark>

**Reglas de Negocio & Diccionario de Datos:**\
\
**a) La actividad realizada es la de "Realiza reserva online"**

**Reglas de Negocio:**

* **Hechos (Facts):** \
  La reserva se identifica con el numero de documento de la persona que lo haya realizado. \
  Se puede reservar en 2 turnos, almuerzo y cena. \
  Las reservas tienen una tolerancia de 15 minutos pasados el horario de reserva antes que caduque la misma.&#x20;
* **Restricciones (Constraints)**: \
  Una persona puede  &#x20;realizar una única reserva por semana\
  La cantidad máxima de comensales es 10  personas por reserva.
* **Acciones disparadoras (action enablers):** \
  Una vez hecha la reserva, se genera una constancia de reserva.&#x20;

**Diccionario de Datos:**

e: datosReserva = tipoDocumento(d) + 0{cantidadReserva}1 + 1{cantidadComensales}10 + turno(d) + horario(d) + toleranciaEspera\
\
tipoDocumento(d) = \[DNI | L.E | pasaporte]\
turno(d) = \[ almuerzo | cena ]\
horario(d) = \[ 12 | 13:30 | 18:30 | 20 | 22 ]\
\
s: constanciaReserva = numeroReserva + fecha(e) + horario(d) + nompreEmpresa\
fecha(e) = dia + mes + año\
horario(d) = \[ 12 | 13:30 | 18:30 | 20 | 22 ]

**Tipo de Evento:** Evento Externo
