---
description: Compra de Tickets para el Cine | Cinema Tickets Purchase
cover: >-
  https://images.unsplash.com/photo-1587135325273-adef4e88bc25?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHxtb3ZpZSUyMHRpY2tldHN8ZW58MHx8fHwxNzQ0MzAwNTU2fDA&ixlib=rb-4.0.3&q=85
coverY: -235
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 3 - Practica

<mark style="color:orange;">**Ejercicio 3 - Exercise 3**</mark>

Spanish:

¡Hola! Soy Agustín, fanático de DC, esta semana hay un super estreno de cine, ya estoy sacando las\
entradas!\
\
Mi mamá no entiende mucho de Comics pero quiere parecer copada y cada vez que le cuento que\
voy al cine a ver DC me hace el mismo chiste:\
\
–¡Agustín! Podes elegir ser Superman o el Superboy de Análisis de Sistemas. Di Si.\
\
Cómo no le contesto, porque no entiendo el chiste, se enoja muchísimo y luego no me habla, por\
unos dos minutos.\
\
Bueno más allá de cómo es mi mamá, ya compré las entradas para la próxima película, voy a ir con\
los chicos del club, justo somos 10 que es el máximo de entradas que te deja comprar a la vez.\
Pude ingresar el código de promoción que me regalaron y así pagar un 35 % menos. El pago lo\
hice con la tarjeta de mi mamá, cuando lo vea en el resumen, ¡se arma!

a) Definir la actividad que hace Agustín (además de soportar los chistes malos de su mamá) .\
b) Definir el diccionario de datos de flujos.\
c) Enunciar las reglas de negocio que hubiere. ¿ Te animás a clasificarlas?\
d) En relación a la actividad definida en el punto a,) ¿ Pensás que hay actividades que pueden ocurrir\
antes o después? De ser así, enunciarlas.\
e) Una vez que Agustín compra las entradas le llega el siguiente mail. Escriba las reglas de negocio\
que encuentra en el mismo. \
\
Contenido del mail:\
\
Estimado/a Agustín:\
\
Usted ha comprado 10 entradas para ver Aquaman el viernes, 2 de febrero de 2024 a\
las 20:00 en el Cine Showcase Rosario, en Sala 7.Su código de confirmación es\
UCNDFX.\
\
Dos pasos para acceder a ver su película:

1. NO ES NECESARIO IMPRIMIR SUS ENTRADAS.
2. Presente el código de confirmación que está más arriba al personal de control de la sala.

Asientos comprados:\
O-7 - Número de serie: 2262472402026E1 0055 - SHMAS2D - Importe: $2,700.00\
O-6 - Número de serie: 2262472402026E1 0056 - SHMAS2D - Importe: $2,700.00\
........\
..........\
O-15 - Número de serie: 2262472402026E1 0058 - SHMAS2D - Importe: $2,700.00\
\
**Política de reembolso:** Showcase no realiza cambios, reintegros ni devoluciones de entradas\
una vez comenzada la función adquirida.\
\
El Cliente tiene derecho a revocar la compra y solicitar la devolución del importe abonado\
de dos maneras, \
\
1\) haciéndose presente en la boletería del cine para el cual compró las\
entradas hasta la hora de inicio de la función. \
\
2\) de manera online hasta tres (3) horas&#x20;antes del comienzo de la función para la cual la entrada fue adquirida utilizando el link:&#x20;DEVOLUCIÓN

English:

Hello! I’m Agustín, a DC fan, and this week there’s a big film premiere – I’m already buying the tickets!\
\
My mum doesn’t know much about comics, but she wants to come across as cool. Every time I tell her I’m going to the cinema to see DC, she makes the same joke:\
\
“Agustín! You can choose to be either Superman or the Systems Analysis Superboy."\
\
Since I don’t reply – because I don’t understand the joke – she gets terribly angry and won’t speak to me for about two minutes.\
\
Anyway, putting aside how my mum is, I’ve already bought the tickets for the next film. I’m going with my club friends – we’re exactly ten, which is the maximum number of tickets you can purchase at one time. I managed to enter the promotional code they gave me and thus paid 35% less. I paid with my mum’s card – when she sees it on the statement, i will be involved in a big trouble. \
\
a) Define the activity that Agustín is doing (besides tolerating his mum’s bad jokes).

b) Define the data dictionary for flows.

c) List any business rules that apply. Can you categorising them?

d) In relation to the activity defined in point a), do you think there are activities that might occur before or after? If so, list them.

e) Once Agustín has purchased the tickets, he receives the following email. Write down the business rules you find in it.\
\
E**mail Content:**

Dear Agustín:

You have purchased 10 tickets to see Aquaman on Friday, 2nd February 2024 at 20:00 at Cine Showcase Rosario, in Hall 7. Your confirmation code is UCNDFX.

**Two steps to access your film:**

IT IS NOT NECESSARY TO PRINT YOUR TICKETS.\
Present the confirmation code shown above to the control staff at the venue.

Purchased seats:\
O-7 – Serial Number: 2262472402026E1 0055 – SHMAS2D – Price: $2,700.00\
O-6 – Serial Number: 2262472402026E1 0056 – SHMAS2D – Price: $2,700.00\
…\
…\
O-15 – Serial Number: 2262472402026E1 0058 – SHMAS2D – Price: $2,700.00\


Refund Policy: Showcase does not offer exchanges, refunds or ticket returns once the purchased screening has began.

The Customer is entitled to cancel the purchase and request a refund of the amount paid in either of the following ways:

1. By presenting themselves at the box office of the cinema for which the tickets were purchased, up until the start time of the screening.
2. Online, up to three (3) hours before the commencement of the screening for which the ticket was purchased, using the following link: REFUND.

***

<mark style="color:green;">**Solution:**</mark>

**Reglas de Negocio & Diccionario de Datos:**

a) La actividad realizada en este enunciado consiste en Comprar entradas para asistir a una funcion en el cine.&#x20;

**Reglas de Negocio:**

* **Restricciones (Constraints)**: Se permite comprar hasta 10 entradas por cliente en una misma compra
* **Calculos (Computations):** Se paga un 35% menos por utilizar un codigo de promocion&#x20;
* **Hechos (Facts):** Al finalizar la compra de las entradas se genera un codigo de confirmacion
* **Inferencias (Inferences):** No se realizan cambios, reintegros ni devoluciones
* **Restricciones (Constraints)**: Se puede solicitar la devolucion del importe abonado hasta tres horas antes de comenzada la funcion.&#x20;

**Diccionario de Datos:**

e: compraEntrada = 1{ticketFuncion(e)}10 + precioTotal + formaDePago(d) + (codigoPromocion)\
\
ticketFuncion(e) = precioUnitario + ubicacion \
formaDePago(d) = \[Efectivo | tDebito | tCredito] \
\
s: informacionTicket = fechaFuncion(e) + 1{datosEntrada(e)}10 + codigoConfirmacion

fechaFuncion(e) = lugar + fecha + hora\
datosEntrada(e) = precioUnitario + numeroDeSerie + numeroAsiento + codigoIdentificacion

**Tipo de Evento:** Evento Externo
