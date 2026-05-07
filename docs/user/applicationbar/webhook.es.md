
## Webhooks: Notificaciones DLR/MO en tiempo real

El **Webhooks** característica en iTextPro permite a los usuarios recibir **notificaciones en tiempo real** de **DLR (Delivery Receipt)** y **MO (Mobile Originated)** mensajes a través de HTTP Web push.

![Webhooks](images/webhook1.png)

---

### Características clave

- **Notificaciones en tiempo real** 
 Recibir instantáneamente copias de los mensajes DLR/MO cuando ocurren.

- **DLR/MO Handling** 
 Elija el tipo de manejador - si el Webhook está destinado para **MO** o **DLR**.

- **Configuración flexible** 
 Establecer un nombre amistoso, definir la URL base de endpoint, seleccionar el método de solicitud (**#** o **POST**), y asignar el manejador apropiado.

- **Timeout Awareness** 
 Las solicitudes de Webhook tienen un **tiempo predeterminado de 10 segundos**. El punto final configurado debe devolver **200** respuesta dentro de este tiempo.

---

### Pasos para configurar Webhooks

1. **Acceso a Webhooks** 
 Navigate a la **Webhooks** sección en iTextPro.

2. **Añadir New Webhook** 
 Haga clic **"Añadir nuevo Webhook"** crear una nueva configuración.

3. **Especificar detalles** 
   - Nombre amistoso 
   - Base de punto final URL 
   - Método (en inglés)**#** o **POST**) 
   - Handler**MO** o **DLR**)

4. **Guardar configuración** 
 Confirme y guarde los detalles del webhook.

---

El **Webhooks** característica asegura **actualizaciones de mensajes instantáneas, fiables y configurables**, ayudando a los usuarios a mantener un flujo de comunicación eficiente con la entrega de datos en tiempo real.
