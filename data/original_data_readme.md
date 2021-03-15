# About

Conjunto de datos con los incidentes viales reportados por el Centro de Comando, Control, Cómputo, Comunicaciones y Contacto Ciudadano de la Ciudad de México (C5) desde 2014 y actualizado mensualmente.

Recomendamos consultar el descriptor de archivo (diccionario de datos) publicado aquí para realizar un análisis más preciso de los datos.

En este conjunto se reporta: folio, fecha de creación del reporte, hora de creación del reporte, día de la semana de creación del reporte, fecha de cierre de reporte, hora de cierre de reporte, motivo del incidente dependiendo del tipo de emergencia, alcaldía donde sucedió el incidente, latitud y longitud del incidente, código de cierre del incidente reportado, clasificación del incidente, origen del incidente por tipo, alcaldía en que se dio resolución al incidente o emergencia.

Los registros que se reciben en el C5 se clasifican internamente por medio de un código de cierre:

* A = “Afirmativo”: Una unidad de atención a emergencias fue despachada, llegó al lugar de los hechos y confirmó la emergencia reportada

* N = “Negativo”: Una unidad de atención a emergencias fue despachada, llegó al lugar de los hechos, pero en el sitio del evento nadie confirmo la emergencia ni fue solicitado el apoyo de la unidad

* I = “Informativo”: Corresponde a solicitudes de información

* F = “Falso”: El incidente reportado inicialmente fue considerado como falso en el lugar de los hechos.

* D = “Duplicados”: El incidente reportado se registró en dos o más ocasiones procediendo a mantener un solo reporte como el original. Para el uso e interpretación correctos de la información, debe considerarse:

  1. Para contabilizar aquellos incidentes “reales”, es decir, aquellos confirmados por las autoridades en el lugar de los hechos, se debe trabajar con los códigos de cierre “Afirmativo”.
  2. Para contabilizar los registros recibidos en la institución, se debe trabajar con todos los códigos de cierre.
¿Qué es el C5?

Centro de Comando, Control, Cómputo, Comunicaciones y Contacto Ciudadano de la CDMX (C5), es la dependencia del Gobierno de la Ciudad de México encargada de captar información integral para la toma de decisiones en materia de seguridad pública, urgencias médicas, medio ambiente, protección civil, movilidad y servicios a la comunidad en la capital del país a través del video monitoreo, de la captación de llamadas telefónicas y de aplicaciones informáticas de inteligencia, enfocadas a mejorar la calidad de vida de las y los capitalinos. Cada incidente registrado genera un folio único identificador, excepto las llamadas no procedentes o “falsas” (bromas, niños jugando, etc.) que se reciben por distintos medios. Mientras un folio está abierto; es decir, mientras el registro está siendo atendido, éste no se carga en la base de datos interna, una vez que el folio ha sido cerrado éste se refleja en el sistema y es posible visibilizarlo internamente con un día de vencimiento, pues se realiza una recarga diaria (por esta razón las fechas de inicio y cierre de folio no necesariamente coinciden).

Content
The data set has the following columns:

folio: a unique ID for each register
fecha_creacion: creation date
hora_creacion: creation time
dia_semana: day of the week when incident happens
codigo_cierre: internal classification. The column could contain the following codes.
A: Affirmative, if the incident is confirmed by emergencies team.
N: Negative, if the emergencies team doesn't confirm the incident at the location point.
I: Informative, in case attention teams want to add extra information.
F: False, if initial report doesn't match with the real events
D: Duplicated, records with closing code affirmative, negative or false but operators identify them
fecha_cierre: close date, the date when the incident was resolved
año_cierre: close year
mes_cierre: close month
hora_cierre: close time
delegacion_inicio: entity inside Mexico City where the incident was registered
incidente_c4: a brief explanation about the incident.
latitud: accident latitude
longitud: accident longitude
clasconf_alarma: code identifying the situation's severity
tipo_entrada: how the incident was reported
delegacion_cierre: entity inside Mexico City where the incident was closed
geopoint: latitude and longitude columns combined
mes: month when the incident was reported
