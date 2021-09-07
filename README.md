# Api- Feedback_details

GET  https://prod-api.smileweb.net/api/feedback-details

Devuelve información detallada acerca del feedback recibido dentro de un periodo de tiempo, en formato JSON.

## Query Params

### Date Parameters:

- timezone: (TYPE string)

Zona horaria en la que estas. Ejemplo: “-03:00”

Default: UTC-0

- startDate: (TYPE string)

Determina la fecha de inicio a partir de la cual quiero extraer la información con el formato YYYY-MM-DD HH:MM:SS . Ejemplo: “2021-08-01T00:00:00.000”

- endDate: (TYPE string)

Determina la fecha de fin a partir de la cual quiero extraer la información con el formato YYYY-MM-DD HH:MM:SS . Ejemplo: “2021-08-31T00:00:00.000”

En caso de no ingresar los parámetros startDate y endDate, se mostrará información de los últimos 7 días.

### Pagination Parameters:

- per_page: (TYPE int)

Cantidad de registros por página. Ejemplo: 100

- page: (TYPE int)

Número de la página que se quiere consultar. Ejemplo: 1

## Headers:

- Authorization: (Bearer token)

Token válido y sin expirar suministrado por el administrador de la cuenta.

## Success Response:

HTTP Status 200

Contiene toda la información

- votes: (TYPE object)

- current_page: (TYPE int)

Página que se está consultando la data.

- Data: (TYPE array)

Contiene la data de los votos y cada registro muestra la siguiente información.

- campaign_name  (TYPE string)

Nombre de la campana.

- store_name  (TYPE string)

Nombre de la sucursal.

- poll_name  (TYPE string)

Nombre de la encuesta.

- campaign_data  (TYPE string)

Información adicional de la campana.

- form_data  (TYPE string)

Información adicional de datos completados por el usuario.

- created_at (TYPE string)

Fecha de la respuesta.

- contact_data (TYPE object)

Información adicional del usuario.

- user_context (TYPE object)

Información acerca del entorno en el que contestó el usuario

- questions (TYPE array)

Contiene cada pregunta con sus resultados.

- name (TYPE string)

Nombre de la pregunta.

- vote (TYPE string/ int)

Voto.

- motives (TYPE array)

Contiene los motivos de la respuesta.

- motive (TYPE string) 

Nombre del motivo.

- comment (TYPE string)

Comentario del motivo.

- comment (TYPE string)

Comentario de la pregunta.

- total (TYPE int)

Total de registros en el rango de fecha consultado.

- per_page (TYPE int)

Cantidad de registros por página.

- path (TYPE int)

Url con la que se consultó la data.

- last_page (TYPE int)

Número de la última página que posee data.

- first_page_url (TYPE int)

Url para consultar la información de la primera página

- last_page_url (TYPE int)

Url para consultar la información de la última página


