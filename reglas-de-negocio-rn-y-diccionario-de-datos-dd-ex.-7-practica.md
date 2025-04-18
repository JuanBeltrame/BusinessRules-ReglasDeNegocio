---
description: Francisco y el Cajero | Francisco and the ATM
cover: >-
  https://images.unsplash.com/photo-1551260627-fd1b6daa6224?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwyfHxBVE18ZW58MHx8fHwxNzQ0OTE2MDU5fDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 7 - Practica

<mark style="color:orange;">**Ejercicio 7 - Exercise 7**</mark>

Spanish:

Francisco es el protagonista formal.\
Alguna que otra vez, Francisco saca una parte de los fondos de una cuenta bancaria a manera de billetes&#x20;físicos. Si te estás preguntando ¿Por qué Francisco hace esto? La respuesta que obtuvimos es la\
siguiente: “realizo esta actividad en un cajero automático para contar con una parte de mi capital líquido,&#x20;para pagar diferentes bienes y servicios que requieran un método en efectivo”.\
\
Además nos comentó que: se puede retirar dinero en más de una operación en un mismo día para la\
misma tarjeta de débito, sin embargo nos alerta sobre que existe un tope de $250.000 pesos por día para la&#x20;misma tarjeta. Algo para destacar es que se puede elegir si el retiro viene en billetes de menor\
denominación ($100 a $500), o en los de mayor denominación ($1.000/$2.000).\
\
a) Enunciar la actividad que realiza Francisco en el cajero automático. Escribir los flujos de entrada y\
de salida para la misma.\
b) Enunciar las reglas de negocio.

English:

Francisco is the formal protagonist.

From time to time, Francisco withdraws part of the funds from a bank account in the form of physical banknotes. If you're wondering _"Why does Francisco do this?"_, the answer we received was:

> “I carry out this activity at a cash machine in order to have some of my liquid capital on hand, to pay for different goods and services that require cash.”

He also mentioned that it’s possible to withdraw money in more than one transaction on the same day using the same debit card. However, he warns us that there is a daily withdrawal limit of $250,000 pesos per card.

An interesting feature is that one can choose whether the money comes in lower denomination notes ($100 to $500 pesos), or higher denominations ($1,000/$2,000 pesos).

**a)** State the activity Francisco carries out at the cash machine. Write the input and output flows for this activity.

**b)** State the business rules.

***

<mark style="color:green;">**Solution:**</mark>

**Reglas de Negocio & Diccionario de Datos:**

a) La actividad que realiza Francisco es la de extraer dinero

**Reglas de Negocio:**

* **Inferencias (Inferences):** \
  El monto de $250.000 se reinicia al comenzar un nuevo dia.&#x20;
* **Hechos (Facts):** \
  El cajero puedo entregar billetes de denominacion baja, o billetes de denominacion alta. \
  Se pueden realizar varias operaciones de retiro de dinero en un mismo día.&#x20;
* **Restricciones (Constraints)**: \
  Se puede retirar hasta $250.000 por dia.&#x20;
* **Calculos (Computations):** \
  El sistema tiene registro de cuanto dinero se lleva extraido hasta el momento en un mismo dia.&#x20;
* **Acciones disparadoras (action enablers):** \
  Luego que el cajero entrega el dinero en efectivo genera e imprime un ticket con los datos de la operacion.

**Diccionario de Datos:**

e:extraerDinero = tipoDeRetiro(d) + 1{cantidadDeOperaciones}n + 1{montoRetiro}250.000\
tipoDeRetiro(d) =  \[denominacionBaja | denominacinAlta] \
\
s: recibirDinero = 1{montoRetiro}250.000 + ticketExtraccion(e)\
ticketExtraccion(e) = 1{montoRetiro}250.000 + fecha(e) + nombreDelBanco&#x20;

**Tipo de Evento:** Evento Externo
