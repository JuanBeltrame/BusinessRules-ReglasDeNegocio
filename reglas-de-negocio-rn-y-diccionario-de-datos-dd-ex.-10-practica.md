---
description: Dialogo en la Fotocopiadora | Dialog at the Photocopier
cover: >-
  https://images.unsplash.com/photo-1666101041092-468eb2818c87?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxQaG90b2NvcGllcnxlbnwwfHx8fDE3NDUxNTQ5OTF8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 10 - Practica

<mark style="color:orange;">**Ejercicio 10 - Exercise 10**</mark>

Spanish:

Se viene otro diálogo y es el último.\
–Hola Elisa, ¿Cómo estás? - saluda Tomás\
–¡Hola Tomy! Bien, ¿Ya sacaste las fotocopias de todos los apuntes de teoría de ADESI? - pregunta\
Elisa.\
–Lo íbamos a realizar en la mañana, estoy esperando a Julian, ya que parece que el centro de\
estudiantes habilitó una página web y el tiene la url para acceder - comenta Tomy.\
-¡Hola chicos! ¿Encargamos las fotocopias?--pregunta Julián.\
–Si, dale! Te estábamos esperando para hacerlo - dice Elisa.\
–Voy a encargar todo a nombre mío, ¿Qué tipo de hoja prefieren: ecológica o común? - pregunta Julián\
–La ecológica es mucho más cara me parece, y cada apunte tiene como 90 hojas!--dice Elisa\
–¿En serio? ¿Cómo vamos a hacer para leer todo eso?--dice Tomy\
–Pienso que la única manera sería... leyendo–dice en chiste Julián\
–Que gracioso está Julian –dice Elisa\
–Hay que leer los apuntes para poder hacer los crucigramas de ciclo de vida y eso —dice serio Julián\
–Dicen por ahí que el profe de ADESI va a sacar los crucigramas de JULIO—sigue haciendo chistes\
Julián\
–Ahora hablo en serio, todos quieren copias de los apuntes, ¿no?, me ayudan diciéndome el nombre\
de cada uno de los apuntes- nuevamente Julián\
–Poné la dirección de tu casa y que te lo envíen ahí o les parece que los retiremos por la fotocopiadora\
¿Qué opinan? –pregunta Tomy\
–Acordate de descargar las constancia del pedido, que te dan cuando terminas de realizar el encargo-\
indica Elisa - Porque ahí te informan la fecha estimada en que estarán listas las fotocopias.

a) Define el diccionario de datos de flujos para la actividad Encargar Fotocopias.

English:



***

<mark style="color:green;">**Solution:**</mark>

**Reglas de Negocio & Diccionario de Datos:**



**Reglas de Negocio:**

* \
  \


**Diccionario de Datos:**

e: encargoDeFotocopias = nombre + tipoDePapel(d) + 1{cantidadDeCopias}3 + 1{nombreApuntes}n + tipoDeRetiro(d) \
\
tipoDePapel(d) = \[ecologico + comun]\
tipoDeRetiro(d) = \[domicilio + fotocpiadora]\
\
s: constanciaDePedido = fechaRetiro + precio&#x20;

**Tipo de Evento:** Evento Externo
