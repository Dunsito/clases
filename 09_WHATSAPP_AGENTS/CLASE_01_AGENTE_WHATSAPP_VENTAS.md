# Clase 1: Un agente de WhatsApp que atiende y vende

**Duración estimada:** 3 a 4 horas (sin contar la verificación de Meta, que puede tardar días).
**Nivel:** básico-intermedio. Necesitas saber usar n8n y tener una cuenta de Meta.
**Recursos:** todo lo que se usa aquí tiene licencia libre (MIT o Apache) o es documentación oficial. Ver `WHATSAPP_CLASSES.md` y `WHATSAPP_SALES_AGENT_CODE.md`.

## Objetivos
Al terminar serás capaz de:
1. Conectar un número de WhatsApp Business a n8n con la API oficial de Meta.
2. Recibir un mensaje, pasarlo a una IA y responder por WhatsApp.
3. Hacer que la IA responda solo con tu información (precios, horarios, políticas) y no invente.
4. Calificar un lead (nombre, servicio, presupuesto) y guardarlo.
5. Pasar la conversación a una persona cuando sea necesario.

## Arquitectura
```
Cliente (WhatsApp)
   ↓  mensaje
Meta WhatsApp Cloud API  ──webhook──▶  n8n
                                         │
                       ┌─────────────────┼──────────────────┐
                       ▼                 ▼                  ▼
                 Base de conocimiento   Modelo de IA    Registro de lead
                 (Google Sheets/RAG)    (OpenAI/Gemini   (Sheets/Airtable/
                                         u Ollama local)   HubSpot)
                       └─────────────────┼──────────────────┘
                                         ▼
                              Respuesta por WhatsApp
                              (o traspaso a una persona)
```

## Parte 1. Cuenta y canal (teoría + práctica)
1. Sigue la guía oficial W1 (Meta Cloud API, Get Started): crea la app con el caso de uso "Conectar con clientes por WhatsApp".
2. Genera un token de sistema permanente. El temporal caduca rápido.
3. Envía tu primer mensaje de prueba desde la API a tu propio número.
4. **Ejercicio 1:** dibuja el flujo de un mensaje de cliente, de principio a fin, con tus palabras.

## Parte 2. Recibir y responder en n8n (práctica)
1. Instala n8n (autoalojado, gratis) o usa su prueba en la nube.
2. Crea un nodo Webhook para recibir los mensajes de Meta y responde a la verificación del webhook.
3. Conecta un nodo HTTP Request para enviar la respuesta con la Cloud API.
4. Revisa cómo está estructurado el mensaje entrante (`messages[0].text.body`, `contacts`, `from`).
5. Referencia: N8N102 (webhooks, credenciales y HTTP Request) de learn.n8n.io.
6. **Ejercicio 2:** responde "Hola, ¿en qué te ayudo?" a cualquier mensaje.

## Parte 3. Dar cerebro a la IA (práctica)
Opciones con código libre para estudiar:
- **mnk-nasir/whatsapp-ai-agent** (MIT): flujo completo en n8n con OpenAI, memoria de 20 mensajes y base de conocimiento. Léelo antes de copiarlo.
- **atelon7/WhatsApp-AI-Agent** (MIT): versión en Python con Flask.
- **blitzlabeg/whatsapp-chatbot** (MIT): con un modelo local en Ollama, sin pagar por cada respuesta.

Instrucciones para el prompt del sistema (plantilla):
```
Eres el asistente de [NEGOCIO]. Responde solo con la información de la base de
conocimiento. Si no tienes el dato, di que lo consultarás y ofrece pasar a una
persona. Nunca prometas descuentos o plazos que no estén en la base. Sé breve.
Pide el nombre y el servicio que busca antes de dar un precio.
```

**Ejercicio 3:** escribe tu base de conocimiento en una hoja de cálculo con 10 preguntas frecuentes reales de tus clientes. Conéctala al agente.

## Parte 4. Calificar y registrar el lead (práctica)
- Mira **Marwan513/multilingual-ai-sales-agent-n8n** (MIT): pide email, servicio y presupuesto, y guarda el contacto. Adáptalo a tu CRM o a Google Sheets.
- Pregunta una cosa a la vez. Nunca pidas todo en un solo mensaje.

**Ejercicio 4:** haz que el agente guarde nombre, servicio y presupuesto en una hoja cuando el cliente muestre interés.

## Parte 5. Traspaso a una persona
- Define una palabra clave (por ejemplo "persona" o "asesor") que pase la conversación a un humano.
- Si la IA no tiene el dato, debe ofrecer el traspaso, no inventar.
- Para una plataforma completa con traspaso, revisa **chattermate/chattermate.chat** (Apache-2.0). Es un producto grande; úsalo como referencia.

## Parte 6. Antes de usarlo con clientes reales (obligatorio)
- Escribe solo a quien aceptó recibir mensajes tuyos. Si no, Meta te puede suspender.
- Verifica tu negocio en Meta y usa un número de WhatsApp Business dedicado.
- Los mensajes que inicias tú, fuera de la ventana de 24 horas, deben usar plantillas aprobadas por Meta.
- Prueba con tu propio número y datos ficticios.
- **No** uses WhatsApp Web no oficial (por ejemplo, Wavo): Meta puede bloquear el número.

## Evaluación
Tu agente está listo cuando:
- [ ] Responde en menos de 10 segundos a un mensaje de prueba.
- [ ] No inventa precios ni plazos fuera de la base de conocimiento.
- [ ] Captura nombre, servicio y presupuesto en la hoja.
- [ ] Pasa a una persona con la palabra clave.
- [ ] Tiene una lista de exclusión para quien pida no recibir mensajes.

## Qué sigue
Clase 2 (pendiente): medir conversiones y ajustar el prompt con las conversaciones reales.
