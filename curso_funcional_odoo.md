# Notas Curso Funcional Odoo
## Crear una base de datos Odoo
1.	En 3 horas, se debe activar una base de datos de Odoo para garantizar la prueba completa de 15 días.
2.	 Cuando se crea un usuario en una base de datos Odoo, un correo electrónico es enviado con un enlace para crear una contraseña segura para la base de datos Odoo.
3.	 Se debe activar  el modo desarrollador para ver la opción "Cargar datos de demostración", que saldra en configuración en el mismo apartado donde se activa el modo desarrolador
4. Solo como administrador se puede instalar aplicaciones
   ## Crear una base de datos Odoo
1. El idioma del usuario se cambia en (Nombre en la parte superior derecha > Mi perfil (Preferencias) > pestaña Preferencias.) y puedes tener varios idiomas
2. La autenticación de dos factores se activa en "Mi perfil" bajo la pestaña "Seguridad de la cuenta".
3. Las diferentes "vistas" que están disponibles para ver los registros son Lista, Kanban, Calendario, Pivote, Gráfico, Actividad.
   ## Calendario de odoo
1. Un nuevo evento de calendario se puede crear desde el módulo Calendario y desde el chat de cualquier registro.
2. Para ver el calendario de otro usuario y todos sus eventos programados, se sigue la siguiente ruta "Calendario > Asistentes > Añadir el usuario."
3. configurar un evento del calendario para que sea un evento recurrente, se sigue la siguiente ruta "Reunión > Editar > Opciones."
   ##  Programar actividades
1.  El campo del formulario de Actividad que se debe editar si desea delegar su actividad a una persona diferente es el campo "Asignado a".
2.  El número que aparece junto al botón Actividades en la parte superior derecha de la barra de navegación significa el número de actividades pendientes que vencen hoy o que ya han vencido.
3.  En la vista Kanban, cuando una ficha tiene un icono verde de Actividades significa que el registro tiene una próxima actividad programada (con una fecha de vencimiento futura).
 ##  Contactos
 1.  Los dos tipos de contactos son Particular y empresa.
 2.  Para archivar un contacto con el que ya no haces negocios debes "Seleccionar/ver contacto > Acción > Archivar."
 3.  Los los botones SMART están localizados en la barra superior del registro en Odoo.
    ## Exportar e importar datos
1. Para especificar registros en Odoo que se desea exportar debe marcar la casilla a la izquierda de la línea de registro mientras está en modo Lista.
2. La configuración para que los datos que estás exportando/importando sean compatibles con Odoo, debes "Marcar la casilla etiquetada: "Quiero actualizar los datos (exportación compatible con la importación)" al exportar. y Descargar la plantilla de la ventana de importación de datos y utilizar los encabezados suministrados."
3. La opción "Importar Registros" en Odoo se encuentra en "Favoritos > Importar registros.", pero en la version 17 se ubica en "acciones" (rueda dentada)
   ## Conceptos básicos de Chatter
1.  En el Chatter de un registro no se puede ver pedidos de venta relacionados.
2.  Se añade un seguidor al registro en "Seguidores > Añadir seguidores > Escribe el nombre o el correo electrónico de la persona > Añadir seguidor."
3.  La diferencia entre "Enviar mensaje" y "Nota de registro" es que "Enviar mensaje" puede enviar un mensaje visible para usuarios externos; "Nota de registro" puede crear una nota NO visible para usuarios externos.
  ## Odoo Discusión (Convesaciones): Mensajes Directos y Llamadas de Voz/Video | Primeros pasos
1. Para ver todas tus conversaciones de Discusión en Odoo, debes hacer clic clic en el icono de Conversaciones en la barra de navegación superior o yendo al módulo Discutir.
2. Los nuevos mensajes no leídos en el módulo discutir (Convesaciones) se pueden ver en  "Bandeja de emtrada"
3.  Para invitar a partes externas a una conversación en Odoo Discuss se debe ir a "Añadir Usuarios > copiar el enlace de invitación > enviar el enlace a la parte externa."
 ## Odoo Discuss: Channels (Convesaciones)
1. Para ver todos los canales públicos en Odoo se sigue la siguiente ruta "Módulo Conversar > Canales > haga clic en el icono de engranaje."
2. Las dos formas de acceder a los canales en Odoo es a través del icono Conversaciones en la esquina superior derecha y a través de la aplicación Discutir (Convesaciones).
3. Se puede suscribir automáticamente en un departamento a un canal en le siguiente ruta "En la pestaña Configuración del canal > Privacidad."
## Flujo de negocio: Tienda de muebles
1. Un producto para el que su inventario muestra una cantidad de 0 se puede vender
2. Para facturar todos sus clientes a la vez, realiza siguiendo estos pasos "Vaya a la aplicación Ventas > A Facturar > Ordenes a Facturar"
## Flujo de negocio: Servicio de consultoria
1. Si desea que se cree un proyecto y tareas cuando se confirma un pedido de cliente, debe crear una tarea en el proyecto del pedido de venta.
2. En las columnas del pedido de cliente se muestran las horas "Entregadas" registradas en las tareas.
3. Las opciones de refacturación disponibles, para configurar los productos de gastos son: "Sin refacturación, A precio de coste, A precio de venta"
4. Para facturar a los clientes por lotes se puede elegir un periodo específico.
   ## Flujo de negocio: Departamento Administrativo
1. La acción dividir "divide un lote de documentos en archivos separados"
2. Cuando uso una dirección de email para recibir documentos, odoo crea un "Alias de email"
3. Odoo permite enviar un documento para que lo firmen mi cliente y mi empleado
   ## Flujo de negocio: Proyecto de construcción
1.  Para que la columna "Analítica" este visible en la Orden de Compra o en la Orden de Venta, debe activar en Contabilidad > Configuración > Ajustes.
2.  Para facturar al cliente el tiempo que los empleados han trabajado en el proyecto, debe  estables el "producto" como un servicio y la política de facturación como hojas de horas por tareas.
3.  Si por ejemplo unos paneles de madera están configurados para facturar las cantidades entregadas y refacturar al "precio de venta" y el coste del producto es de 50 $ y el precio de venta es de 80 $. Se facturaria por 5 paneles 400 euros en total.
## Flujo de negocio: Restaurant
1. En la aplicación de planificación de Odoo, la "marca" roja cuando aparece en un turno significa que exiten conflito de turno para la misma persona.
2.Los módulos necesarios para realizar pedidos en línea son "eCommerce y Website"
3. Para poder editar el diseño de las mesas se debe seleccionar el Icono del lápiz en la esquina superior derecha.
## Flujo de negocio: Eventos y Marketing
1. En las preguntas de registro: si "Preguntar sólo una vez por pedido" no está activado, La pregunta se formula una vez por asistente.
2. Para crear una regla de Generación de clientes potenciales, debo ir a "Events → Configuration → Lead Generation → Create."
3. Si se pueden crear y enviar una publicación a varias plataformas sociales en varior flujos al mismo timepo


