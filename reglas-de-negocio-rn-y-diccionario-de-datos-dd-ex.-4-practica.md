---
description: Compra de Tickets para el Cine | Cinema Tickets Purchase
cover: >-
  https://images.unsplash.com/photo-1587135325273-adef4e88bc25?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHxtb3ZpZSUyMHRpY2tldHN8ZW58MHx8fHwxNzQ0MzAwNTU2fDA&ixlib=rb-4.0.3&q=85
coverY: -235
---

# Reglas de Negocio (RN) y Diccionario de Datos (DD) - Ex. 4 - Practica

<mark style="color:orange;">**Ejercicio 4 - Exercise 4**</mark>

Spanish:

Juan, Brian y Nicolás van a rendir Análisis Matemático I, luego de varias semanas de estudio ha llegado el&#x20;momento del Examen Final. Para poder rendir deberán realizar la inscripción .\
\
a) Investiga en la Facultad Regional Rosario y en la carrera de Ingeniería en sistemas de Información\
cuáles son las reglas de negocio relacionadas con la actividad de Inscribirse a un Examen Final .&#x20;Enuncialas.\
\
b) Realiza el diccionario de datos para el flujo de entrada y salida para la actividad de Inscribirse a un\
Examen Final.

Juan, Brian y Nicolás van a rendir Análisis Matemático I, luego de varias semanas de estudio ha llegado el&#x20;momento del Examen Final. Para poder rendir deberán realizar la inscripción.\
\
a) Investiga en la Facultad Regional Rosario y en la carrera de Ingeniería en sistemas de Información\
cuáles son las reglas de negocio relacionadas con la actividad de Inscribirse a un Examen Final .\
Enuncialas.\
\
b) Realiza el diccionario de datos para el flujo de entrada y salida para la actividad de Inscribirse a un\
Examen Final.

English:

Juan, Brian, and Nicolás are about to sit for _Mathematical Analysis I_. After several weeks of studying, the time has come for the Final Exam. In order to sit the exam, they must complete the registration process.

**a)** Investigate, within the Rosario Regional Faculty and the degree course in Information Systems Engineering, what business rules are related to the activity of registering for a Final Exam. List them.

**b)** Create the data dictionary for the input and output flow of the activity _Registering for a Final Exam_.

Juan, Brian, and Nicolás are about to sit for _Mathematical Analysis I_. After several weeks of studying, the time has come for the Final Exam. In order to sit the exam, they must complete the registration process.

**a)** Investigate, within the Rosario Regional Faculty and the degree course in Information Systems Engineering, what business rules are related to the activity of registering for a Final Exam. List them.

**b)** Create the data dictionary for the input and output flow of the activity _Registering for a Final Exam_.

***

<mark style="color:green;">**Solution:**</mark>

**Reglas de Negocio & Diccionario de Datos:**

**Reglas de Negocio:**

* **Restricciones (Constraints)**: \
  Para rendir un final se necesita estar como regular en la materia\
  La inscripcion al examen se puede generar unicamente durante en el periodo de inscripcion al mismo.
* **Inferencias (Inferences):** El examen se rinde de manera presencial en la facultad.&#x20;
* **Hechos (Facts):** \
  Los finales se rinden en las mesas de examen.\
  La inscripcion se realiza a traves del Sysacad
* **Acciones disparadoras (action enablers):**  Cuando se genera la inscripcion satisfactoriamente, se genera un comprobante con los datos de la mesa de examen.&#x20;

**Diccionario de Datos:**

e: inscripcionExamen = login(e) + nombreMateria + profesorExaminador\
\
login(e) = numLegajo + contraseña&#x20;

s: comprobanteInscripcion = fechaExamen(e) + lugarDeExamen + numAula + numComision + profesorExaminador

fechaExamen(e) = hora + dia&#x20;

**Tipo de Evento:** Evento Externo&#x20;
