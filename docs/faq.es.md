---
tags:
  - FAQ
  - Help
---

# Preguntas frecuentes

Encuentre respuestas rápidas a preguntas comunes sobre Power SMPP.

---

## Comienzo

??? question "¿Cómo puedo acceder al panel de usuarios?"
 Navegue a su URL de instancia de Power SMPP proporcionada por su administrador. Entra en tu **Nombre de usuario** y **Contraseña** para acceder al panel de usuario iText Hub.

 Si ha olvidado sus credenciales, comuníquese con su administrador del sistema para restablecer la contraseña. Para seguridad, se recomienda cambiar su contraseña después de su primer login a través de **Ajustes Cambiar contraseña**.

??? question "¿Qué muestra el tablero?"
 El dashboard (iText Hub) ofrece una visión general en tiempo real de su actividad de mensajería con cuatro métricas clave:

    - **SMS enviado hoy** — Mensajes SMS totales enviados desde todas las interfaces en el día actual
    - **Hoy en día** — Mensajes SMS totales entregados con éxito en el día actual
    - **SMS enviado ayer** — Mensajes enviados el día anterior
    - **Entregado ayer** — Mensajes enviados el día anterior

 También muestra gráficos interactivos de monitoreo de tráfico para ambos **MT (Mobile Terminated / outgoing)** y **MO (Mobile Originated / entrando)** mensajes. Desde el panel de control, puede acceder rápidamente a la creación de campañas, gestión de contactos, visualización de tráfico, descargas de informes y ajustes de perfil. Véase [Dashboard](user/dashboard/dashboard.md) para más detalles.

??? question "¿Cómo cambio mi contraseña?"
    1. Ve. **Ajustes Cambiar contraseña**
    2. Entra en tu **contraseña actual** para la verificación
    3. Entra en tu **nueva contraseña** (Debe cumplir con los requisitos de seguridad establecidos por su administrador)
    4. **Confirmación** la nueva contraseña
    5. Haga clic **Guardar**

 Se recomienda actualizar periódicamente las contraseñas para mantener la seguridad de la cuenta y ajustarse a las mejores prácticas. Su administrador también puede hacer cumplir una política de cambio de contraseña que requiere actualizaciones periódicas. Véase [Cambiar contraseña](user/settings/changepassword.md).

??? question "¿Cómo actualizo mi información de perfil?"
 Ve. **Ajustes Mi perfil** donde puede actualizar los siguientes campos:

    - **Nombre** — Referencia de su cuenta de padre para facturar
    - **Número de móvil** - Utilizado para comunicaciones y verificación de cuentas
    - **Código del país** — Se puede aplicar automáticamente a los números de campaña a través de la opción "Código de país autoadd"
    - **ID de correo** - Utilizado para comunicaciones, alertas, OTP y entrega de notificación
    - **País / Estado** - Para fines de facturación y referencia
    - **Zona horaria** - Afecta todas las pantallas de fecha/hora en toda la plataforma, incluyendo la programación de campañas e informes

 Haga clic **Guardar** después de hacer cambios. Ver [Mi perfil](user/settings/myprofile.md).

??? question "¿Qué zona horaria utiliza la plataforma?"
 La plataforma utiliza la zona horaria configurada en su **Mi perfil** Ajustes. Esta zona de tiempo afecta:

    - Pantalla de métricas de panel
    - Programación de campañas
    - Fecha de presentación/hora sellos
    - Informes de cuenta del mensaje

 Siempre verifique que su zona horaria es correcta antes de programar campañas para asegurar que se envían en el momento indicado para sus receptores.

??? question "¿Cuál es la diferencia entre los mensajes MT y MO?"
    - **MT (Mobile Terminated)** — Mensajes enviados **a** un teléfono móvil. Estos son sus mensajes de salida / salida (por ejemplo, campañas, notificaciones, OTPs).
    - **MO (Mobile Originated)** — Mensajes enviados **desde** un teléfono móvil. Estos son mensajes entrantes o entrantes recibidos de sus destinatarios (por ejemplo, respuestas, solicitudes de exclusión).

 Tanto el tráfico MT como el MO se muestran en sus gráficos de panel.

---

## Envío de SMS

??? question "¿Cómo puedo componer y enviar una campaña de SMS?"
 Siga estos pasos para crear y enviar una campaña SMS:

    1. Haga clic **SMS MT** para abrir la página de SMS de Composición
    2. Ingrese a **Nombre de la campaña** (autogenerado con prefijo "Camp " y fecha-tiempo, o introducir un nombre personalizado)
    3. Seleccione una **ID del remitente** de la lista aprobada (o introducir una dinámica si "Open Sender ID" está habilitado por su administración)
    4. **Añadir destinatarios** usando uno de cuatro métodos:
        - **Grupos almacenados** — Seleccione de grupos de contacto precreados
        - **Archivo local** — Cargue un archivo Excel/CSV con números de teléfono
        - **Entrada manual** — Números de tipo directamente (separados con código de país, no + símbolo)
        - **Copiado** — Números de desechos de otra fuente
    5. **Componga su mensaje** en el cuadro de texto (o seleccione de borradores/templatos)
    6. Opcionalmente habilitado **Flash SMS** para pantalla instantánea
    7. El sistema **auto-detectos Unicode** si se utilizan caracteres especiales
    8. Elige **Envía ahora.** o **Cuadro** para más tarde
    9. Haga clic **Enviar SMS** — una vista previa del costo se muestra antes de la confirmación final

    !!! tip
 Pruebe siempre su contenido de mensaje en algunos números antes de ejecutar campañas a gran escala, ya que los contadores de caracteres son aproximados debido a variaciones de navegador / codificación.

 Ver [Comprar SMS](user/smsmt/compose.md) para la guía completa.

??? question "¿Cómo envío SMS personalizado desde un archivo Excel?"
 La función SMS From Excel le permite enviar mensajes personalizados utilizando datos de su hoja de cálculo:

    1. Abrir el **SMS From Excel** pestaña
    2. Descargar el **muestra de archivo** a través de la pestaña "Ver Muestra" para ver el formato requerido
    3. Prepare su archivo Excel con números móviles en una columna y datos de personalización (nombres, cantidades, fechas, etc.) en otras columnas
    4. **Subir** el archivo Excel — las 5 filas superiores se muestran para la verificación
    5. **Seleccione la columna** con números móviles
    6. Ingrese a **ID del remitente**
    7. Componga su mensaje y haga clic **"Insert Placeholder"** añadir variables dinámicas de sus columnas de hoja de cálculo (por ejemplo, <span data-ph="0"></span>, <span data-ph="1"></span>)
    8. Haga clic **Vista previa** para ver los 5 mejores mensajes personalizados con conteos de caracteres
    9. Elige **Cuadro** o **Envía ahora.**
    10. Review the **pantalla de vista previa final** muestra de la desintegración de los costos por países
    11. Haga clic **Enviar**

 Esto es ideal para contenidos personalizados como recordatorios de citas, confirmaciones de pedidos o notificaciones de pago. Véase [SMS From Excel](user/smsmt/smsfromexcel.md).

??? question "¿Qué formatos de archivo son compatibles para subidas de contacto?"
 Power SMPP admite los siguientes formatos de archivo para subidas de contacto:

    | Formato | Extensión | Caso de uso |
    |--------|-----------|----------|
    | Excel | .xls, .xlsx | Más común, soporta múltiples columnas |
    | CSV | .csv | Compatibilidad ligera y universal |
    | Texto | .txt | Listas de números simples |

 **Requisitos:**

    - Los números de teléfono deben incluir **código de país** (por ejemplo, 919909945175, no +919909945175)
    - Do **no** utilizar el <span data-ph="0"></span> símbolo antes del código del país
    - Las columnas adicionales pueden contener datos de personalización (nombres, cantidades, etc.)
    - Las columnas de auto-detectos del sistema después de subir

??? question "¿Qué es el SMS Flash y cuándo debería utilizarlo?"
 Flash SMS es un tipo de mensaje especial que **aparece directamente en la pantalla del destinatario inmediatamente** sin ser almacenado en su buzón de entrada. El mensaje se muestra como una superposición popup en el teléfono.

 **Cuándo utilizar SMS Flash:**

    - Alertas urgentes y notificaciones de emergencia
    - Información que requiere atención inmediata
    - Códigos OTP que no necesitan ser guardados
    - Notificaciones del sistema crítico

 **Cómo habilitar:** Revisar el **Flash SMS** checkbox mientras que compone su mensaje en la página Compose SMS. Tenga en cuenta que el comportamiento de SMS Flash puede variar dependiendo del teléfono y el transportista del destinatario.

??? question "¿Cómo funciona la detección de caracteres especiales y Unicode?"
 Power SMPP **detecta automáticamente** cuando su mensaje contiene caracteres Unicode. Así es como funciona:

    - **GSM 7-bit encoding** (default): Admite letras, números y símbolos básicos en inglés. Límite: **160 caracteres** por segmento SMS.
    - **Codificación Unicode** (auto-detectado): Activado cuando se detectan scripts no latinos (árabe, hindi, chino, etc.), emojis o caracteres especiales. Límite: **70 caracteres** por segmento SMS.

 **Importante:** Cuando se detecta Unicode, el contador de caracteres actualiza automáticamente. Un único emoji o un personaje especial cambiará todo el mensaje a la codificación Unicode, reduciendo los caracteres disponibles por segmento.

    !!! warning
 Los contadores de mensajes y caracteres mostrados son **indicativa únicamente** debido a las variaciones de navegador y codificación. Siempre prueba en un lote pequeño antes de campañas grandes.

??? question "¿Cuál es el límite de caracteres por SMS y cómo funciona la concatenación?"
 **Limitaciones de caracteres por segmento SMS:**

    | Codificación | SMS único | SMS (por segmento) |
    |----------|-----------|-------------------------------|
    | GSM 7-bit (standard) | 160 caracteres | 153 caracteres |
    | Unicode | 70 caracteres | 67 caracteres |

 Cuando un mensaje excede el único límite SMS, se divide automáticamente en **concatenado (multi-part) SMS**. Cada segmento adicional utiliza ligeramente menos caracteres (153 o 67) porque algunos bytes están reservados para el encabezado de concatenación que le dice al teléfono cómo volver a montar las partes.

 **Ejemplo:** Un mensaje GSM de 320 caracteres = 3 segmentos de SMS (153 + 153 + 14 caracteres). Usted está facturado por segmento.

??? question "¿Cómo programaré una campaña para más tarde?"
    1. Al componer su SMS (Comprar SMS o SMS desde Excel), seleccione el **Cuadro** Opción
    2. Elija su deseado **fecha y hora**
    3. Seleccione el correcto **zona horaria** (defaults to your profile timezone)
    4. Complete el resto de la configuración de la campaña y haga clic **Enviar**
    5. La campaña será solicitada y enviada automáticamente en el momento programado

 **Gestión de campañas programadas:**

    - Ve. **Informe " Mis horarios** para ver todas las campañas programadas
    - Puedes **reprogramación** una campaña pendiente haciendo clic en **Editar** botón en la pestaña Acción
    - Siempre verifique la zona horaria seleccionada coincide con el tiempo de entrega previsto

 Véase [Mis Horarios](user/report/schedule.md).

??? question "¿Cuál es la diferencia entre Borradores y Plantillas?"
    | Característica | Proyectos | Plantillas |
    |---------|--------|-----------|
    | **Editabilidad** | Completamente editable — puede modificar todo el contenido | Sólo los titulares de posición pueden ser modificados; el contenido estático está bloqueado |
    | **Aprobación** | No se requiere aprobación | May require admin approval before use |
    | **Caso de uso** | Salvar mensajes de trabajo en progreso | Formatos de mensaje reutilizables y aprobados |
    | **Cumplimiento** | No cumplimiento | DLT-compliant (for India) |

 **Proyectos** son ideales para guardar mensajes en los que sigues trabajando. **Plantillas** son ideales para mensajes estandarizados y preaprobados que deben mantener un formato consistente.

    !!! warning "Usuarios de API"
 Al utilizar plantillas a través de API, asegúrese de que el espaciamiento exacto, las comas y la puntuación coincidan con la plantilla aprobada. Cualquier discrepancia en el formato puede resultar en que la plantilla sea rechazada como inválida.

??? question "¿Puedo agregar un código de país automáticamente a todos los números?"
 Sí. Hay dos maneras:

    1. **Durante la composición de la campaña** - Revisar **"Código de país autoadvertido"** casilla de verificación cuando se agregan los destinatarios. El sistema prependerá el código de país configurado a todos los números.
    2. **En tu perfil** - Ve **Ajustes Mi perfil** y configura tu defecto **Código del país**. Este ajuste se utiliza cuando se activa la opción autoadd.

 Esto es útil cuando su lista de contactos contiene números locales sin el prefijo del país.

---

## Plantillas de identificación del remitente

??? question "¿Cómo solicito un nuevo ID de remitente?"
    1. Ve. **SMS MT > Gestionar ID del remitente**
    2. Haga clic en **"Agregar ID de remitente"** pestaña
    3. Un popup de configuración aparece — ingrese los detalles deseados del ID de remitente siguiendo las directrices de su administrador
    4. Haga clic **Guardar**
    5. El ID del remitente introduce un **pendiente de aprobación** estado
    6. Su administrador revisa y aprueba / rechaza la solicitud
    7. Una vez aprobado, el ID del remitente aparece en su desplegable al componer campañas

 Puedes ver el **Estado de aprobación** de todas tus identificaciones de Sender en la lista de ID de Gestion Sender. Si tu cuenta tiene **"Open Sender ID"** habilitado por el administrador, puede saltar este paso y escribir cualquier ID de remitente directamente al componer. Véase [Manage Sender ID](user/smsmt/managesenderid.md).

??? question "¿Cómo puedo crear y administrar plantillas de mensajes?"
    1. Ve. **Plantilla de administración de SMS MT**
    2. Haga clic en **"Añadir plantilla"** pestaña
    3. Introduzca el nombre de la plantilla y componga el contenido
    4. Haga clic **"Insert Placeholder"** añadir variables dinámicas para la personalización (por ejemplo, <span data-ph="0"></span>, <span data-ph="1"></span>)
    5. Haga clic **Guardar** - la plantilla puede requerir aprobación de administrador

 **Después de la aprobación:**

    - **Contenido estadístico** (todo excepto los propietarios de puestos) está bloqueado y no puede ser cambiado
    - Sólo **Valores de posición** se puede modificar cuando se utiliza la plantilla en las campañas
    - Puede ver el estado de aprobación para todas las plantillas en la vista de lista

    !!! warning "Importante para los usuarios de API"
 Al enviar a través de API utilizando plantillas, asegúrese **exacta** spacing, comas, puntuación y formato coinciden con la plantilla aprobada. Incluso una discrepancia menor puede causar que la plantilla sea tratada como inválida y el mensaje puede ser rechazado.

 Si tu cuenta tiene **"Plantilla abierta"** activado, puede saltar la configuración de plantilla. Ver [Manage Template](user/smsmt/managetemplate.md).

??? question "¿Qué es DLT y por qué se requiere la aprobación de la plantilla/Sender ID?"
 **DLT (Distributed Ledger Technology)** es un marco reglamentario establecido por **TRAI (Telecom Regulatory Authority of India)** para todos los mensajes Application-to-Person (A2P) en India.

 **Requisitos clave:**

    - Todos **ID de remitente** debe registrarse en la plataforma DLT
    - Todos **plantillas de mensajes** debe ser previamente aprobado en DLT antes de usar
    - Los operadores pueden bloquear mensajes que no coincidan con las plantillas aprobadas
    - Esto se aplica a todos los SMS comerciales y transaccionales enviados en India

 **Por qué existe:**

    - Reduce las comunicaciones comerciales no solicitadas (spam)
    - Protege a los consumidores de mensajes fraudulentos
    - Crea un sendero auditable para todos los mensajes A2P
    - Garantiza el cumplimiento reglamentario de los operadores de telecomunicaciones

 Si usted opera fuera de la India, DLT puede no aplicarse, pero su administrador todavía puede hacer cumplir la aprobación de plantilla para el control de calidad.

??? question "¿Qué pasa si mi ID de remitente o plantilla es rechazada?"
 Si su ID de remitente o plantilla es rechazada por su administrador:

    - El estado mostrará como **Rechazado** en la página de gestión respectiva
    - Necesitarás crear un **nueva solicitud** con detalles corregidos
    - Las razones de rechazo comunes incluyen: contenido no compatible, formato incorrecto, entradas duplicadas o violaciones de políticas
    - Póngase en contacto con su administrador por razones y directrices específicas de rechazo

---

## Contactos

??? question "¿Cómo puedo crear y gestionar grupos de contacto?"
 **Crear un grupo:**

    1. Ve. **Contactos Gestion Groups**
    2. Haga clic **Add Group**
    3. Introduzca un nombre de grupo y ahorre

 **Gestión de los grupos existentes: acciones disponibles:**

    | Medida | Descripción |
    |--------|-------------|
    | **Editar nombre del grupo** | Renombrar un grupo existente |
    | **Contactos de importación a granel** | Agregar múltiples contactos a la vez desde un archivo |
    | **Empty Group** | Quitar todos los contactos pero mantener el grupo |
    | **Grupo** | Eliminar permanentemente el grupo y todos los contactos |

 Los grupos facilitan la organización de los destinatarios y los seleccionan rápidamente al componer campañas. Véase [Grupos de gestión](user/contacts/managegroups.md).

??? question "¿Cómo puedo importar contactos?"
 Power SMPP ofrece **tres métodos de importación**:

 **Método 1: Importación de un archivo**

    - Mejor para conjuntos de datos grandes
    - Apoyos **.xls**, **.csv**, y **.txt** formatos
    - Seleccione el grupo de destino, suba el archivo y confirme

 **Método 2: Copia y Prueba**

    - Rápido y flexible
    - Copiar contactos directamente desde una hoja de Excel u otra fuente
    - Pegar en el área de entrada

 **Método 3: Entrada manual**

    - Agregar contactos uno por uno
    - Mejor para pequeños números de contactos

 **Pasos:**

    1. Seleccione **grupo destinatario** de la caída
    2. Elija su método de importación
    3. Añade tus contactos
    4. Haga clic **Hecho** para confirmar la importación

 See [Import Contacts](user/contacts/importcontacts.md).

??? question "¿Cómo exporto contactos?"
    1. Ve. **Contactos Contactos de exportación**
    2. Seleccione **grupo(s)** desea exportar usando casillas de verificación
    3. Haga clic **Exportación**
    4. Elige tu formato preferido:
        - **.xls** — Formato Excel
        - **.csv** - Valores separados por el sistema
        - **.txt** Texto de la traducción
    5. Descargar el archivo exportado

    !!! tip
 Exportar sólo los grupos que necesita para tamaños de archivos manejables. Utilice las exportaciones con fines de respaldo o migrando contactos entre sistemas.

 Ver [Contactos de exportación](user/contacts/exportcontacts.md).

---

## Informes

??? question "¿Cómo puedo ver los informes de campaña?"
 Ve. **Informe " Campaign Report** donde tiene múltiples vistas:

 **Vista de la Campaña:**

    - Lista consolidada de todas las campañas
    - Muestra estado de la campaña, tasas de entrega, fechas de ejecución y estadísticas clave
    - Haga clic en una campaña para profundizar en detalles

 **Vista de la lista:**

    - Informe DLR (Delivery Receipt) con detalle de nivel de mensaje
    - Muestra el estado de entrega de mensajes individuales

 **Situación de la campaña:**

    - Seguimiento de colas de mensajes en tiempo real
    - View completed and pending deliveries

 **Actions Tab:**

    - Cuenta de mensaje entregado
    - Cuenta de mensaje pendiente
    - Número de mensajes fallidos
    - Otras categorías

 Filtro por **rango de fecha** para encontrar campañas específicas. Véase [Informe de Camboya](user/report/campaign.md).

??? question "¿Qué significan los estados DLR?"
 Los estados de DLR (Informe de animación) indican el resultado de la entrega de cada mensaje:

    | Situación | Significado | Medida |
    |--------|---------|--------|
    | **Entrega** | Mensaje entregado con éxito al teléfono del destinatario | No se necesitan medidas |
    | **Failed** | Mensaje no se puede enviar (número inválido, número de red, bloqueado o DND) | Compruebe la validez del número; considerar la eliminación de la lista |
    | **Pendiente** | Mensaje enviado al operador pero la confirmación de entrega aún no recibida | Espera — el estado puede actualizar; algunos operadores retrasan las DLRs |
    | **Queued** | El mensaje está esperando en el sistema para ser procesado y enviado | Espera a procesar |
    | **Rechazado** | El mensaje fue rechazado por el operador o la puerta de entrada | Comprobar el cumplimiento de plantillas, ID de remitente o restricciones de contenido |

    !!! tip
 Usar el **Cuenta del mensaje** reporte para obtener un resumen basado en el estado sobre un rango de fechas, y uso **Descargar Report** para las exportaciones detalladas de Excel.

??? question "¿Cómo puedo ver los informes de cuenta de mensajes?"
    1. Ve. **Informe contable de mensajes**
    2. Seleccione una **rango de fecha** o específicos **mes**
    3. Ver el mensaje cuenta desglosado por estado (Delivered, Pending, Failed, etc.)
    4. Haga clic en **hipervínculo** en un mes para perforar en un **desglose por día**

 El informe muestra cuenta de acuerdo a su zona horaria configurada. Use rango de fechas y filtros de estado juntos para el análisis de tráfico específico. [Conteo de mensajes](user/report/messagecount.md).

??? question "¿Cómo puedo descargar informes en formato Excel?"
    1. Ve. **Informe de descarga**
    2. Ver la lista de **informes solicitados anteriormente** (si hay)
    3. Haga clic **Solicitud de informe** para generar un nuevo informe
    4. El informe entra **Pendiente** estado mientras que el sistema reduce los datos
    5. Una vez completado el procesamiento, el estado cambia **Listo**
    6. Haga clic en el informe para **descarga** en formato Excel (.xls)

 Los informes incluyen datos detallados de nivel de mensajes: número de destinatarios, estado, horarios, costo, identificación del remitente y más. Véase [Informe de descarga](user/report/downloadreport.md).

??? question "¿Puedo reenviar mensajes fallidos de una campaña?"
 Sí, pero con condiciones:

    1. Abrir la campaña **Campaign Report**
    2. Ir a la **Reséndice** pestaña
    3. Seleccione los mensajes fallidos o pendientes para reenviar

 **Reenviar las reglas de elegibilidad:**

    | Escenario | Reenviar Disponible? |
    |----------|-------------------|
    | Campaña ejecutada (completa) | Sí. |
    | Campaign still in queue | No |
    | Los mensajes largos todavía se procesan | No |

    !!! tip
 Descargar el informe **antes de reenviar** para validar su lista de destino y evitar duplicar entregas a números que ya hayan recibido el mensaje.

??? question "¿Cómo detengo una campaña en marcha?"
    1. Ve. **Informe " Campaign Report**
    2. Encuentra la campaña activa
    3. Haga clic en **Para.** botón

 **Importante:**

    - Mensajes **ya enviado** no se puede recordar
    - Sólo **mensajes pendientes** será cancelado
    - Esta acción es inmediata y no se puede deshacer
    - Use esto cuando descubra un error en el contenido de su campaña o necesite detener la entrega urgentemente

??? question "¿Cómo puedo reprogramar una campaña pendiente?"
    1. Ve. **Informe " Mis horarios**
    2. Encuentra la campaña que quieres reprogramar
    3. Haga clic en **Editar** botón en la pestaña Acción
    4. Seleccione el nuevo **zona horaria**
    5. Establecer el nuevo **fecha y hora**
    6. Haga clic **Guardar**

 Siempre verifique la zona horaria seleccionada para asegurar que la campaña envíe a la hora local correcta para sus receptores. Véase [Mis Horarios](user/report/schedule.md).

---

## WhatsApp

??? question "¿Cómo puedo conectar mi cuenta de WhatsApp Business?"
 **Prerrequisitos:**

    - A verified **Facebook Business** cuenta
    - A **WhatsApp Business Profile** vinculado a su cuenta de Facebook

 **Pasos:**

    1. Navegue a la sección WhatsApp
    2. Haga clic **"Conectar usando Facebook"**
    3. Una caja de diálogo aparece: registre su cuenta de Facebook con iTextPro
    4. Crear o vincular su **WhatsApp Business Profile** (esto actúa como el puente entre Meta e iTextPro)
    5. Configurar la configuración de mensajería WhatsApp dentro de iTextPro

 Una vez conectado, puede comenzar a crear plantillas, campañas y utilizar Team Inbox para el soporte al cliente. Ver [Empezar](plugins/whatsapp/whatsappuser/overview.md).

??? question "¿Cómo puedo crear una campaña de WhatsApp?"
    1. Haga clic en **Campaña** botón en la sección WhatsApp
    2. **Seleccione el nombre del remitente** desde el desplegable (predeterminados al nombre del conector)
    3. **Añadir destinatarios** usando uno de tres métodos:
        - **Entrada manual** — Escriba números móviles directamente
        - **Contactos de importación** — Cargue un archivo Excel/CSV
        - **Uso de grupos existentes** — Seleccione grupos de contacto precreados
    4. Haga clic **"Select Template"** y elegir una plantilla preaprobado
    5. **Personalizar el mensaje:**
        - Modificar el encabezado si es necesario
        - Reemplazar variables dinámicas ({{1}} {{2}}, etc.) con valores reales
        - A **vista previa en tiempo real** aparece en el lado derecho
    6. Elige **Cuadro** (ver la caja y establecer fecha/hora) o **Envía ahora.**
    7. Haga clic **Enviar**

 Sólo **Plantillas mejoradas** puede ser utilizado, asegurando el cumplimiento regulatorio. Véase [Campaign](plugins/whatsapp/whatsappuser/campaign.md).

??? question "¿Cuáles son las categorías de plantilla de WhatsApp y cómo puedo crear una?"
 Las plantillas de WhatsApp se clasifican por Meta en tres tipos:

    | Categoría | Propósito | Ejemplos |
    |----------|---------|---------|
    | **Marketing** | Mensajes promocionales para múltiples destinatarios | Ofertas, lanzamientos de productos, boletines informativos |
    | **Utilidad** | Actualizaciones oportunas relacionadas con compras / viaje de clientes | Confirmaciones de pedidos, actualizaciones de envío, recordatorios de nombramientos |
    | **Autenticación** | OTP y mensajes de verificación | Códigos de acceso, verificación de cuentas |

 **Crear una plantilla:**

    1. Ve. **Plantilla WhatsApp**
    2. Seleccione **categoría** (Marketing, Utility, o Authentication)
    3. Seleccione **idioma** (Meta admite varios idiomas)
    4. **Añadir Header** (opcional): Ninguno, texto o medios (imagen, vídeo, documento, ubicación)
    5. **Add Body**: Contenido del mensaje principal con variables a través del botón Variable (formato: {{1}} {{2}} {{3}})
    6. Proporción **ejemplos** para cada variable (ayuda Meta entender y aprobar más rápido)
    7. **Añadir Footer** (opcional): texto de marca o descargo
    8. **Añadir botones** (opcional):
        - **Botón Opt-Out** — Opción de subscripción
        - **CTA Buttons** — Sitio web de visita (hasta 2) o número de teléfono de llamada
    9. Haga clic **Guardar como proyecto** (edit later) or **Save and Submit** para Meta aprobación

 La aprobación generalmente toma un **pocos segundos**. Una vez aprobado, puede previsualizar, editar (requiere re-approval), eliminar, o lanzar directamente una campaña desde la plantilla. Véase [Template](plugins/whatsapp/whatsappuser/template.md).

??? question "¿Cómo uso Team Inbox para atención al cliente?"
 Team Inbox es una plataforma centralizada para gestionar conversaciones WhatsApp:

 **Para los administradores:**

    - Visión completa en **todos los chats** (tanto el agente humano como las conversaciones de chatbot)
    - **Cobertura instantánea** de cualquier conversación en curso para la resolución de edición rápida
    - Búsqueda y filtrar conversaciones

 **Para los agentes:**

    - credenciales de inicio de sesión únicas para cada agente
    - Acceso limitado **chats asignados** sólo
    - Responder a los clientes en tiempo real

 **Características clave:**

    - Monitorización centralizada de todas las interacciones WhatsApp en un solo lugar
    - Capacidad de remoción de minas para las cuestiones más graves
    - Acceso seguro con acceso único garantizando privacidad y protección de datos
    - Buscar y filtrar para buscar una conversación rápida

 Ver [Team Inbox](plugins/whatsapp/whatsappuser/teaminbox.md).

??? question "¿Cómo puedo crear y administrar cuentas de agente?"
 Las cuentas del agente proporcionan acceso individual para los miembros del equipo de soporte:

    1. Ve. **WhatsApp > Equipo con cuentas de agente**
    2. Haga clic **Agregar nuevo agente**
    3. Rellene los detalles necesarios
    4. Haga clic **Guardar** — la cuenta de agente se crea al instante

 **Beneficios de cuentas individuales de agente:**

    - **Mejora de la gestión del equipo** — Crear grupos especializados para diferentes temas o segmentos de clientes
    - **Mejora de la seguridad** - Restrict access to authorized agents only
    - **Mayor rendición de cuentas** — Supervisar el rendimiento y los tiempos de respuesta de cada agente
    - **Plantilla flexible para el cambio** — Cuentas separadas para diferentes turnos o zonas horarias

 See [Team Agent](plugins/whatsapp/whatsappuser/teamagent.md).

??? question "¿Cómo puedo establecer reglas avanzadas para WhatsApp?"
 El enrutamiento avanzado dirige automáticamente mensajes entrantes de WhatsApp al agente adecuado o chatbot:

    1. Ve. **WhatsApp > Reglas avanzadas de rutina**
    2. Haga clic **"Añadir nueva regla"**
    3. Configure la regla con estos parámetros:

    | Parámetro | Descripción |
    |-----------|-------------|
    | **Nombre de la regla** | Nombre claro, descriptivo para fácil identificación |
    | **Alcance - Conector** | Seleccione el conector webchat específico |
    | **Alcance - Marco de tiempo** | Establecer cuando la regla es activa |
    | **Logic - Tipo de carga** | Ruta por tipo de contenido (texto, imagen, etc.) |
    | **Lógica - Texto de carga** | Ruta por palabras clave o frases específicas |
    | **Logic - Captación de carga** | Ruta por imagen/captura de vídeo |
    | **Logic - Información del remitente** | Ruta por los detalles del remitente (nombre, teléfono) |
    | **Operadores lógicos** | Combina las condiciones con la lógica AND/OR |
    | **Fulfillment** | Ruta a un determinado **Agente** o **Bot** |

 See [Advanced Routing](plugins/whatsapp/whatsappuser/advancerouting.md) y [Configuración de reglas](plugins/whatsapp/whatsappuser/ruleconfiguration.md).

??? question "¿Cómo puedo crear flujos de chatbot automatizados?"
    1. Ve. **WhatsApp ► Manage Flow**
    2. Elija: **Use una plantilla preconstruida** (configuración rápida) o **Construido desde Scratch** (totalmente personalizado)
    3. Configurar el **Bot Trigger** — un texto/frase específico que activa el chatbot
    4. Establecer el **Mecanismo de reingreso** por intentos fallidos de disparo
    5. Configuración **Idle Timeout** para el seguimiento automático cuando el usuario deja de responder

 **bloques de construcción de flujo disponibles:**

    | Bloque | Descripción |
    |-------|-------------|
    | **Mensaje** | Enviar un mensaje de texto al usuario |
    | **Coleccion Input** | Mostrar un aviso y capturar la respuesta del usuario en una variable |
    | **Opción** | Presentar hasta 3 opciones (meta limit) con imagen opcional; el flujo continúa basado en la selección |
    | **Subdivisión** | Crear caminos condicionales basados en insumos previamente recogidos |
    | **Enviar adjunto** | Enviar documentos, fotos o videos |

 Combine estos bloques para crear conversaciones automatizadas que manejan FAQs, recopilar información, clasificar pistas y llegar a los agentes humanos cuando sea necesario. Ver [Manage Flow](plugins/whatsapp/whatsappuser/manageflow.md).

??? question "¿Cómo monitorizo los registros de comunicación WhatsApp?"
 Ve. **WhatsApp** to view detailed transactions records:

    - Cada interacción entre su aplicación y Meta (WhatsApp) se ha registrado
    - Ambos **Solicitudes** y **respuestas** se registran
    - Útil para resolver problemas de entrega y diagnosticar problemas técnicos

    !!! warning
 Se mantienen registros de vigilancia para los **pasados 3 días** sólo. Compruebe los registros rápidamente si necesita investigar un problema.

 Véase [Monitoring](plugins/whatsapp/whatsappuser/monitoring.md).

??? question "¿Cómo puedo ver los informes de la campaña WhatsApp?"
 Ve. **Informes de WhatsApp** para múltiples tipos de informes:

 **Reporte de campaña:**

    - **Campaign View** — Resúmenes que muestran nombre de campaña, remitente, contenido, mensajes totales, estado y costo
    - **Lista Ver** — Detalles de nivel de mensajes, incluido el número de destinatarios, plantilla utilizada, fecha de presentación, fecha de entrega, estado y códigos de error

 **Informe de cuenta del mensaje:**

    - Resumen rápido de los mensajes totales enviados dentro de un rango de fecha seleccionado

 **Mi horario:**

    - Ver todas las campañas programadas con cuenta de estado y mensajes de WhatsApp

 **Descargar Report:**

    - Exportar informes detallados de la campaña WhatsApp para el análisis offline
    - Separar los informes de SMS para una mejor organización

 Véase [Informe de Camboya](plugins/whatsapp/whatsappuser/reports/campaignreport.md).

---

## Developer API

??? question "¿Cómo puedo acceder a la documentación de API?"
    1. Ve. **Desarrollador API**
    2. Haga clic **Ver documento API**
    3. El sistema redirige al sistema **Swagger** herramienta API interactiva
    4. Buscar puntos finales, ver formatos de solicitud/respuesta y probar las llamadas API directamente

 La documentación incluye formatos de carga útil, estructuras de respuesta, detalles de autenticación, manejo de errores y mejores prácticas de integración. See [API Document](user/apidocument/document.md).

??? question "¿Cómo puedo generar credenciales de API y empezar?"
 El acceso a la API es proporcionado por su administrador:

    1. Su administración permite **Acceso a la API HTTP** para su cuenta
    2. Usted recibe un **Nombre de usuario** y **API Key** para la autenticación
    3. Ve. **Desarrollador API de desarrolladores** para ver sus credenciales
    4. Haga clic **Ver documento API** para acceder a la herramienta Swagger

 Utilice estas credenciales en el encabezado de autorización de sus solicitudes de API. La herramienta Swagger le permite probar todos los puntos finales de API de forma interactiva antes de integrarse en su aplicación. Ver [Developer API](user/apidocument/developerapi.md).

??? question "¿Qué puntos finales de API están disponibles?"
 Power SMPP ofrece API REST integrales para:

    - **Envío de SMS** — Envío único y masivo de mensajes
    - **Estado de entrega de facturación** — Consultar el estado DLR para mensajes enviados
    - **Gestión de contactos** — Crear, actualizar y eliminar contactos/grupos
    - **Informes de recuperación** — Publicar informes de campaña y mensajes programáticamente

 Todos los puntos finales aceptan estándar **HTTP methods** (GET, POST) y regreso **JSON responses**. La lista completa con parámetros, ejemplos y códigos de respuesta está disponible en el [documento API](user/apidocument/document.md).

??? question "¿Puedo integrar Power SMPP con mi propia aplicación?"
 Sí. Power SMPP apoya la integración de terceros mediante:

    - **REST API** — Full-featured HTTP API para el acceso programático
    - **Webhooks** - Retrocesos en tiempo real para notificaciones DLR y MO
    - **SMPP Protocol** — conectividad directa SMPP v3.4 para integraciones de alto volumen (configurada por admin)

 La documentación de Swagger ofrece ejemplos de solicitud/respuesta y mejores prácticas para la integración perfecta. Contacte con su administrador para detalles de conexión SMPP.

---

## Cuenta facturación

??? question "¿Cómo puedo ver mi plan de tarifas?"
 Ve. **Barra de aplicación Mi plan de tarifas** para ver su precio actual:

    - Los precios se muestran por **país** y **red**
    - Las tarifas son fijadas por su cuenta padre/administrador
    - Estos determinan el **costo por mensaje** para cada destino
    - Utilice esto para estimar los costos de campaña antes de enviar

 La vista previa del costo mostrada durante la composición de la campaña utiliza estas tarifas. Véase [Mi plan de tarifas](user/applicationbar/rateplan.md).

??? question "¿Cuál es la diferencia entre facturación prepagada y postpagada?"
    | Característica | Prepago | Puestos pagados |
    |---------|---------|----------|
    | **Saldo** | Debe tener créditos suficientes antes de enviar | Facturado después del consumo |
    | **Verificación de crédito** | Balance del sistema antes de procesar | No se requiere pre-check |
    | **Gastos** | No es posible — la campaña se detiene cuando los créditos se agotan | Posible - rastreado para invocar |
    | **Caso de uso** | Más común para usuarios finales | Típicamente para cuentas de confianza/empresa |

 Su modo de facturación está configurado por su administrador. Check **Barra de aplicación Mis transacciones** para ver su balance actual y su historial de transacciones.

??? question "¿Cómo comprobé mi historial de transacciones?"
 Ve. **Barra de aplicación Mis transacciones** a la vista:

    - Historial completo de transacción entre su cuenta y su cuenta padre
    - Adiciones de crédito (top-ups)
    - Deducciones crediticias (gastos de campaña)
    - Sendero completo de auditoría para la transparencia

 Esto le ayuda a rastrear el gasto, verificar los top-ups y gestionar su presupuesto de mensajería. [Mis transacciones](user/applicationbar/transaction.md).

??? question "¿Cómo puedo configurar webhooks para notificaciones en tiempo real?"
 Webhooks presiona las notificaciones DLR y MO en tiempo real a su aplicación:

    1. Ve. **Barra de aplicación**
    2. Haga clic **"Añadir nuevo Webhook"**
    3. Configure el webhook:

    | Campo | Descripción |
    |-------|-------------|
    | **Nombre amistoso** | Un nombre descriptivo para el webhook |
    | **Base de punto final URL** | URL de llamada de su servidor |
    | **Método** | Obtener o POST |
    | **Handler** | MO (recibidos mensajes) o DLR (recibimientos de entrega) |

 **Requisitos técnicos:**

    - Tu punto final debe regresar **HTTP 200 OK** dentro del tiempo fuera
    - El tiempo predeterminado es **10 segundos**
    - Si su servidor no responde a tiempo, la notificación puede ser retratada o retirada

 [WebHooks](user/applicationbar/webhook.md).

??? question "¿Cómo puedo configurar los correos electrónicos de notificación?"
 Ve. **Barra de aplicación Emails de notificación** para configurar alertas de correo electrónico:

    - Por defecto, las notificaciones se envían a su **email registrado** dirección
    - Puedes añadir **direcciones adicionales de correo de interesados** para recibir alertas
    - Configurar qué **eventos** dispara notificaciones de correo electrónico

 Las notificaciones por correo electrónico se utilizan para comunicaciones de cuenta, alertas de campaña, entrega de OTP y notificaciones del sistema. Véase [Email de notificación](user/applicationbar/notificationemail.md).

---

## Solución de problemas

??? question "¿Por qué mis mensajes muestran como 'Pendiente' durante mucho tiempo?"
 Varias razones pueden causar estatus prolongado pendiente:

    - **Retrasos del operador** — Algunos operadores móviles tardan más en devolver las confirmaciones de entrega
    - **Teléfono de recepción apagado** — El mensaje se apaga en el operador hasta que el teléfono sea accesible
    - **Congestión de redes** - Los períodos de alto tránsito pueden retrasar el procesamiento DLR
    - **Cuestiones de puerta** — La puerta de entrada puede estar experimentando retrasos

 **Qué hacer:** Esperar un período razonable (varía por país/operador). Si los mensajes permanecen pendientes después de 2448 horas, es poco probable que sean entregados. Comprueba con tu administrador si el problema persiste.

??? question "¿Por qué mi mensaje fue rechazado o fallado?"
 Razones comunes para la falla del mensaje:

    | Razón | Solución |
    |--------|----------|
    | Número de teléfono inválido | Verificar el formato número incluye el código de país correcto |
    | DND/No molestar | El destinatario ha optado por mensajes comerciales |
    | Desigualdad de la plantilla | Asegurar que el mensaje coincida con la plantilla aprobada exactamente |
    | ID de remitente no aprobado | Utilice un ID de remitente aprobado o aprobación de solicitud |
    | Créditos insuficientes | Sube el saldo de su cuenta (prepagado) |
    | Número de lista negra | Compruebe con su administrador |
    | Contenido bloqueado | Contenido del mensaje de revisión para palabras clave restringidas |

??? question "¿Por qué mi campaña cuesta diferente de lo que esperaba?"
 Los costos de las campañas dependen de:

    - **Número de beneficiarios** - Cada número único se carga
    - **segmentos de mensajes** — Los mensajes largos se dividen en múltiples segmentos, cada uno facturado por separado
    - **Unicode vs GSM** — Los mensajes Unicode tienen límites de caracteres inferiores, dando lugar a más segmentos
    - **Tasas de destino** - Diferentes países/redes tienen diferentes costos por mesgo
    - **DLR compensation** — Algunas configuraciones pueden ajustar los costos sobre la base del estado de entrega

 Compruebe siempre el **costo vista** antes de confirmar una campaña, y revisar su [Plan de destino](user/applicationbar/rateplan.md) para precios específicos de destino.

??? question "Olvidé mi contraseña. ¿Cómo lo reajusto?"
 Los reseteos de contraseña son gestionados por su **administrador del sistema**. Contacte con ellos directamente para solicitar un reset. Una vez restaurado, inicie sesión con la contraseña temporal y cambiarla inmediatamente **Ajustes Cambiar contraseña**.

 Su administrador también puede tener una opción de reajuste de contraseñas de autoservicio configurada — compruebe con ellos para el proceso específico.
