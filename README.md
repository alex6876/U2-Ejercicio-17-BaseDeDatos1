# Base de Datos de Gestión de Clínica Veterinaria

Proyecto enfocado en la modelación Entidad-Relación (DER / MER) e implementación de base de datos relacional para el control operativo de una clínica veterinaria, administrando tutores/dueños de mascotas, datos clínicos de los pacientes animales, profesionales veterinarios, consultas médicas, catálogo de vacunas y el registro de aplicaciones de vacunación.

---

## Descripción

El sistema modela una estructura de datos relacional para la gestión asistencial e historial médico de una clínica veterinaria. Permite registrar a los tutores de los animales, mantener las historias clínicas y datos fisonómicos de las mascotas, registrar la atención profesional dispensada por los veterinarios durante las consultas médicas, y llevar el control del plan de vacunación administrado a los pacientes.

---

## Funcionalidades e Implementación

### Entidades y Atributos

* Tutor:


* id_DNI: Clave primaria identificadora del tutor o responsable del paciente.


* nombre: Nombre del tutor.


* apellido: Apellido del tutor.


* dirección: Domicilio de residencia del tutor.


* teléfono: Número telefónico de contacto.




* Mascota:


* id_Historia clínica: Clave primaria única que identifica la historia clínica de la mascota.


* nombre: Nombre de la mascota.


* especie: Especie del animal (ej. canino, felino).


* raza: Raza específica de la mascota.


* sexo: Sexo del paciente.


* fecha nacimiento: Fecha de nacimiento del animal.


* color de pelaje: Tono o características del pelaje.




* Veterinario:


* id_matricula profesional: Clave primaria identificadora del profesional matriculado.


* nombre: Nombre del veterinario.


* apellido: Apellido del profesional.


* especialidad clínica: Especialidad médica o área de atención.


* teléfono: Teléfono de contacto.




* Consulta Veterinaria:


* id_Consulta: Clave primaria única de la consulta médica.


* fecha: Fecha en la que se efectúa la atención.


* hora: Horario del turno o consulta.


* motivo consulta: Razón de la visita o síntomas presentados.


* peso actual: Lectura del peso del paciente en la consulta.


* temperatura: Registro de temperatura corporal del animal.


* diagnostico: Dictamen clínico o diagnóstico del profesional.




* Vacuna:


* id_Codigo vacuna: Clave primaria identificadora del insumo/vacuna.


* nombre comercial: Denominación comercial o marca del producto.


* laboratorio: Laboratorio farmacéutico fabricante.


* numero de lote: Número identificador del lote de fabricación.


* descripción: Detalle de las propiedades o componentes de la vacuna.




* Aplicación de vacuna:


* Id_aplicación: Clave primaria del evento de inoculación/vacunación.


* fecha de aplicación: Fecha efectiva en que se administró la dosis.


* fecha surgerida: Fecha sugerida/programada para el refuerzo o próxima dosis.


* horario: Hora en que se realizó la administración.





---

## Relaciones del Modelo

1. Tutor ↔ Mascota (Relación 1:N):


* Un tutor puede ser responsable de múltiples mascotas, pero cada mascota está vinculada a un único tutor titular.




2. Mascota ↔ Consulta Veterinaria (Relación 1:N):


* Una mascota puede registrar múltiples consultas veterinarias a lo largo del tiempo, pero cada consulta médica pertenece a una única mascota paciente.




3. Veterinario ↔ Consulta Veterinaria (Relación 1:N):


* Un profesional veterinario puede atender e impartir múltiples consultas clínicas, pero cada consulta es atendida por un único veterinario responsable.




4. Mascota ↔ Aplicación de vacuna (Relación 1:N):


* Una mascota puede recibir la aplicación de múltiples dosis o vacunas a lo largo de su vida, pero cada evento de aplicación se administra a una mascota específica.




5. Vacuna ↔ Aplicación de vacuna (Relación 1:N):


* Un tipo/código de vacuna se aplica en múltiples ocasiones a distintos pacientes, pero cada evento de aplicación corresponde a una vacuna específica.
