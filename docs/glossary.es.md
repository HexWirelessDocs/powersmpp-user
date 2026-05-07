---
tags:
  - Reference
  - SMPP
  - Getting Started
---

# Glosario

Una guía de referencia rápida a términos comunes utilizados en toda la documentación Power SMPP.

---

## Términos de mensajería

| Mandato | Forma completa | Descripción |
|------|-----------|-------------|
| **SMS** | Servicio de mensajes cortos | Protocolo de mensajería de texto estándar para dispositivos móviles |
| **MT** | Móvil Terminado | Un mensaje enviado **a** un teléfono móvil (outbound) |
| **MO** | Origen móvil | Un mensaje enviado **desde** un teléfono móvil (de entrada) |
| **DLR** | Informe de entrega | Confirmación del estado confirmando si se entregó un mensaje MT |
| **A2P** | Aplicación a persona | Mensajes automatizados enviados desde una aplicación a usuarios finales |
| **P2P** | Persona a persona | Mensajes intercambiados entre usuarios individuales |

---

## SMPP Protocol

| Mandato | Forma completa | Descripción |
|------|-----------|-------------|
| **SMPP** | Mensaje corto Peer-to-Peer | Protocolo estándar para el intercambio de SMS entre sistemas |
| **SMSC** | Short Message Service Centre | Sistema central que almacena, recorre y entrega mensajes SMS |
| **ESME** | Entidad externa de mensajería corta | Una aplicación externa que se conecta al SMSC vía SMPP |
| **PDU** | Dependencia de Datos sobre el Protocolo | Un único paquete de datos SMPP intercambiado entre ESME y SMSC |
| **Bind** | — | The process of establishing an SMPP session between ESME and SMSC |
| **Tx** | Transmisor | Una sesión SMPP que sólo puede **Enviar** mensajes |
| **Rx** | Receptor | Una sesión SMPP que sólo puede **recibir** mensajes |
| **TRx** | Transceptor | Una sesión SMPP que puede ambos **enviar y recibir** mensajes |
| **TPS** | Transacciones por segundo | Capacidad de rendimiento de una conexión SMPP |

---

## Addressing

| Mandato | Forma completa | Descripción |
|------|-----------|-------------|
| **TON** | Tipo de número | Define el formato de la dirección (por ejemplo, International, Alphanumeric) |
| **NPI** | Indicador del Plan de Número | Identifica el estándar de numeración (por ejemplo, E.164, ISDN) |
| **OA** | Dirección de origen | Dirección del remitente (fuente) de un mensaje |
| **DA** | Dirección | La dirección receptora (destinación) de un mensaje |
| **MCC** | Código del país móvil | Un código de 3 dígitos identificando un país de suscriptor móvil |
| **MNC** | Código de red móvil | Un código de 2-3 dígitos identificando un operador de red móvil |
| **MSISDN** | Mobile Station International Suscriptor Directorio Número | El número completo de teléfono internacional de un suscriptor móvil |

---

## Características de la plataforma

| Mandato | Descripción |
|------|-------------|
| **Plan de tarifas** | Una plantilla de precios que define los costos por mensajería para diferentes destinos |
| **Regla de rotación** | Una regla que determina qué gateway maneja un mensaje basado en criterios como destino, remitente o contenido |
| **Gateway** | Una conexión externa SMSC o aggregator configurada en iTextPRO |
| **Interfaz** | Un conector SMPP o HTTP que permite a los socios conectarse a iTextPRO |
| **Blind Routing** | Permite enviar mensajes a destinos sin precios predefinidos |
| **Stop Loss** | Un umbral máximo de costo de la puerta de entrada para evitar pérdidas en mensajes desviados |
| **HLR Lookup** | Inicio Ubicación Registro consulta para validar un número móvil antes de enviar |
| **DLT** | Tecnología Ledger distribuida — Marco regulatorio de la India para SMS A2P que requiere pre-registración de remitentes y plantillas |

---

## Facturación " Negocios

| Mandato | Descripción |
|------|-------------|
| **Prepago** | Modo de facturación donde los usuarios deben tener suficiente saldo de crédito antes de enviar |
| **Puestos pagados** | Modo de facturación donde los usuarios son facturados después del consumo |
| **Moneda básica** | La moneda primaria utilizada para todos los cálculos de facturación interna |
| **Factura recurrente** | Factura automatizada generada a intervalos regulares (semana, mensual, etc.) |

---

## Sistema de vigilancia

| Mandato | Descripción |
|------|-------------|
| **Event Viewer** | Un visor de registros para monitorear eventos del sistema, errores y advertencias |
| **Audit Log** | Un registro cronológico de todas las acciones de usuario y sistema para el cumplimiento |
| **PDU Logger** | Una herramienta para capturar e inspeccionar paquetes de datos de protocolo SMPP crudos |
| **Preguntar Enlace** | Un paquete de mantenimiento continuo SMPP enviado periódicamente para mantener sesiones activas |
| **QoS** | Calidad del servicio - métricas utilizadas para evaluar el rendimiento de la entrega de la puerta de entrada |
