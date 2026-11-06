# Código para un agente de WhatsApp que vende y atiende (2026-11-06)
Objetivo: una IA que converse con clientes por WhatsApp, responda dudas, califique leads y cierre ventas.
Criterio: licencia libre (MIT/Apache), API oficial de Meta (WhatsApp Cloud API) y README leído. No he ejecutado ningún código; eso requiere revisarlo antes con tus propias claves.

## Recomendados (API oficial de Meta, licencia libre)
| Proyecto | Licencia | ★ | Qué hace | Para ventas | Notas |
|---|---|---|---|---|---|
| mnk-nasir/whatsapp-ai-agent | MIT | 2 | Asistente en n8n + OpenAI + WhatsApp Cloud API + Pinecone. Texto, voz e imágenes, memoria de 20 mensajes, búsqueda web y base de conocimiento. | Alta: es la base más completa para vender y atender | Muy nuevo y con pocas estrellas: revisa el código. [VERIFICADO_OPEN_SOURCE] (README leído) |
| atelon7/WhatsApp-AI-Agent | MIT | 8 | Servidor Flask con Meta Cloud API y un Assistant de OpenAI con memoria de conversación y conocimiento propio. | Media-alta: buen ejemplo en Python | [VERIFICADO_OPEN_SOURCE] (README leído) |
| KhazarHaydarli/whatsapp-rag-chatbot | MIT | 0 | Bot de atención con RAG híbrido: responde solo con tu base de conocimiento (tarifas, precios, políticas) y, si no está seguro, dice que no lo sabe en lugar de inventar. Datos de ejemplo sintéticos. | Alta para responder preguntas de precios sin inventar | [VERIFICADO_OPEN_SOURCE] (README leído) |
| Marwan513/multilingual-ai-sales-agent-n8n | MIT | 5 | Flujo de n8n: detecta idioma, pide email, servicio y presupuesto, crea contacto y oportunidad en HubSpot y confirma por WhatsApp con Twilio. | Alta: es un flujo de venta completo (calificar + registrar) | README corto (MVP). [VERIFICADO_OPEN_SOURCE] |
| blitzlabeg/whatsapp-chatbot | MIT | 0 | Atención multilingüe con Cloud API y un modelo local en Ollama (sin coste por uso). Consulta pedidos y catálogo. | Media: bueno si quieres evitar pagar la IA | [VERIFICADO_OPEN_SOURCE] (README leído) |
| TomasS-R/chatbotWhatsAppApiBusiness | MIT | 13 | Chatbot de WhatsApp Business en Node.js con la API en la nube. | Básica | Enlace consultado: el README dio 404 en la rama principal; no leído. [PENDIENTE] |
| chattermate/chattermate.chat | Apache-2.0 | 156 | Plataforma completa de atención con IA, traspaso a humano y soporte de WhatsApp. Es un producto, pero el código es libre. | Alta si quieres un panel de conversaciones y traspaso a persona | Producto grande: úsalo como referencia. [VERIFICADO_OPEN_SOURCE] |

## No recomendado para un negocio
- Haroon966/Wavo (licencia NOASSERTION, 2 ★): usa whatsapp-web.js, es decir, WhatsApp Web sin la API oficial. El propio README dice que es "no afiliado a WhatsApp o Meta, usar bajo tu propio riesgo". Meta puede bloquear el número. Descartado.

## Otros (sin licencia o no revisados)
- Nazuuu-Ali/n8n-whatsapp-Ai-Agent, hassanraza1/arik-whatsapp-bot, igorhsouza/smart-retail-whatsapp-bot, santifer/jacobo-workflows: sin licencia o no revisados. Solo referencia, no copiar. [PENDIENTE]

## Ruta sugerida (solo con código libre y API oficial)
1. Aprender la API oficial: 09_WHATSAPP_AGENTS/WHATSAPP_CLASSES.md (W1, Meta Cloud API).
2. Partir de mnk-nasir (n8n + OpenAI + Cloud API) y añadir la base de conocimiento de KhazarHaydarli para no inventar precios.
3. Añadir el flujo de calificación y registro de Marwan513 (email, servicio, presupuesto, CRM).
4. Pasar a una persona cuando el cliente lo pida o cuando la IA no esté segura.

## Antes de usarlo con clientes reales
- Solo escribir a quien dio su número o aceptó recibir mensajes.
- Verificación del negocio en Meta y número de WhatsApp Business dedicado.
- Plantillas aprobadas por Meta para mensajes fuera de la ventana de 24 horas.
- Probar con tu propio número y datos ficticios antes de conectarlo a ventas reales.
