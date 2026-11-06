# Automatización de respuestas en WhatsApp: ruta de lectura

Esta carpeta es la guía para aprender solo a automatizar respuestas de WhatsApp con una IA. Sigue el orden. Todo lo que está aquí es gratis y con licencia libre o documentación oficial. Lo que no es gratis está marcado.

## Orden de lectura

### 1. Entender el canal oficial (leer primero)
- **Guía oficial de Meta: WhatsApp Cloud API, Get Started.**
  https://developers.facebook.com/documentation/business-messaging/whatsapp/get-started
  - Lee los pasos 1 a 7. El paso 4 (webhook) y el paso 5 (token permanente) son los que más se olvidan.
  - Qué aprendes: cómo se recibe y envía un mensaje oficial.

### 2. Entender el motor de automatización
- **Academia de n8n, curso N8N102** (webhooks, credenciales, HTTP Request).
  https://learn.n8n.io/courses/course-v1:n8n+N8N102+2026H2/about
  - Si nunca has usado n8n, antes haz N8N101 (mismo sitio).
  - Qué aprendes: cómo recibir un webhook y responder con una llamada HTTP.
  - Precio: la página no lo muestra. n8n se puede autoalojar gratis.

### 3. Hacer tu primer agente (tutorial principal)
- **Clase 1: Agente de WhatsApp que atiende y vende.**
  [../09_WHATSAPP_AGENTS/CLASE_01_AGENTE_WHATSAPP_VENTAS.md](../09_WHATSAPP_AGENTS/CLASE_01_AGENTE_WHATSAPP_VENTAS.md)
  - Es la guía paso a paso. Sigue sus ejercicios 1 a 4 en orden.

### 4. Ver código real (solo para estudiar)
- **Jasper's Market** (ejemplo oficial de Meta): https://github.com/fbsamples/whatsapp-business-jaspers-market
  - Lee el README (configuración de la app, plantillas, ngrok). Licencia por verificar.
- **mnk-nasir/whatsapp-ai-agent** (MIT): flujo completo en n8n con IA, memoria y base de conocimiento.
  https://github.com/mnk-nasir/whatsapp-ai-agent
  - Léelo antes de copiar nada. Tiene pocas estrellas: revisa el código.

### 5. Que la IA no invente
- **KhazarHaydarli/whatsapp-rag-chatbot** (MIT): responde solo con tu base de conocimiento y dice "no lo sé" en lugar de inventar.
  https://github.com/KhazarHaydarli/whatsapp-rag-chatbot
  - Lee primero la sección de "guardarraíles" y la del fallback.

### 6. Calificar y guardar clientes
- **Marwan513/multilingual-ai-sales-agent-n8n** (MIT): pide email, servicio y presupuesto, y guarda el contacto.
  https://github.com/Marwan513/multilingual-ai-sales-agent-n8n
  - Es un MVP corto: úsalo como patrón, no como producto terminado.

## Pendiente (no verificado)
Videos gratis de YouTube sobre WhatsApp con n8n. Los he visto en búsquedas pero no pude abrirlos desde aquí. Si quieres, los añadimos cuando haya acceso. Lista en `../09_WHATSAPP_AGENTS/WHATSAPP_CLASSES.md`.

## No leas ni uses esto
- **Haroon966/Wavo**: usa WhatsApp Web sin la API oficial. Meta puede bloquear el número.
- **Cursos de pago** (Humanspace, Seminarios Top, Ciberaula, la comunidad Imperio): no son gratis.
- Repos sin licencia (por ejemplo, Nazuuu-Ali, hassanraza1, igorhsouza): no copiar.

## Antes de conectar clientes reales
- Escribe solo a quien aceptó recibir mensajes tuyos.
- Verifica tu negocio en Meta y usa un número de WhatsApp Business dedicado.
- Prueba con tu propio número y datos ficticios primero.
