# Catálogo de cursos — Imperio Agéntico / Benjamín Cordero
Fecha de verificación: 2026-11-06 (UTC ~21:55–21:56)
Método: lectura de cada página con apify/web-fetch (HTTP 200). Las fichas se leyeron; los vídeos de YouTube NO (ver MISSING_MATERIAL.md).

| ID | Curso | Duración / formato | Módulos | Coste | Acceso | Estado de verificación |
|---|---|---|---|---|---|---|
| C001 | Curso de Claude Code en español | "Más de 6 horas" (ficha); landing dice "52 temas" | 17 módulos (00–16) + bonus; 7 proyectos | Gratis (ficha: `isAccessibleForFree: true`, price 0) | Registro con correo en claudecode.imperioagentico.com; guía/cheat sheet incluida | [VERIFICADO_CURSO_GRATUITO] ficha y landing leídas. Clases/vídeo no verificados. |
| C002 | Curso de Codex | 4 h 54 min | 17 módulos + 10 proyectos | Gratis | Registro en codex.imperioagentico.com; guía PDF gratuita | [VERIFICADO_CURSO_GRATUITO] ficha y landing leídas. |
| C003 | Curso de Hermes Agent | "Más de 4 horas"; sin número de módulos (agrupado en 8 etapas) | 8 etapas: fundamentos, instalación, Telegram, skills/MCP, memoria, correo, publicidad/video, cierre | Gratis | Sin formulario: se abre directamente en YouTube (enlace de ficha: youtube.com/watch?v=FQZGoSwdS_0) | [VERIFICADO_CURSO_GRATUITO] ficha leída. Enlace YouTube PENDIENTE (YouTube no accesible). |
| C004 | Curso de Meta Ads con Claude | 3 h 09 min (landing: 3:09:02) | 11 módulos + bonus | Gratis | Registro en anuncios.imperioagentico.com | [VERIFICADO_CURSO_GRATUITO] ficha y landing leídas. |
| C005 | Imperio Agéntico (comunidad Skool) | Comunidad, 6 sesiones en vivo/semana (según página) | Ver 01_ORIGINAL_CURRICULUM | **$59/mes** (la página indica subida a $77 al llegar a 4.300 miembros). 4,2k miembros. | Privada; requiere pago | [ACCESO_RESTRINGIDO] Solo se registra el temario anunciado. No se accedió al contenido. |

## Detalle por curso

### C001 Claude Code (bencorde.com/cursos/claude-code/)
Módulos según la ficha pública: 00 Bienvenida · 01 El ecosistema Claude · 02 Instalación · 03 La interfaz · 04 Tu primer proyecto (landing + Vercel) · 05 Tokens, límites y contexto · 06 Control y permisos · 07 CLAUDE.md y memoria · 08 Skills · 09 MCP y conectores · 10 Subagentes y Ultracode · 11 Loops y goals · 12 Automatización (Routines y n8n) · 13 Agente investigador (navegador) · 14 Segundo cerebro (Obsidian) · 15 Proyecto final: Matías (media buyer) · 16 Próximos pasos · Bonus: otros modelos.
Proyectos: 1 Web publicada · 2 Sherlock (subagentes) · 3 Scout de tendencias (loops/goals, framework DAME) · 4 Cotizador 24/7 · 5 Investigación en navegador · 6 Segundo cerebro · 7 Matías.
Requisitos: Mac o Windows y cuenta de Claude (la landing indica que el plan Pro permite seguir el curso).
Nota: la landing menciona un curso anterior "el de MCP", no localizado todavía.

### C002 Codex (bencorde.com/cursos/codex/)
Módulos: 00 Bienvenida y mapa · 01 Ecosistema OpenAI · 02 Instalación · 03 Interfaz y voz · 04 Tu primera landing · 05 Tokens, modelos y contexto · 06 Permisos y planificación · 07 Estructura de un proyecto · 08 MCP y conectores · 09 Corto de animación 3D · 10 Navegador, computador y teléfono · 11 Skills y anuncios · 12 Impresión 3D y oficina (Blender) · 13 Subagentes y orquestación · 14 Automatización local y nube · 15 Segundo cerebro · 16 Próximos pasos.
Proyectos: 10 (landing, app existente, corto 3D, investigador de ideas, generador de anuncios, pieza de impresión 3D, oficina en Blender, publicación de vídeo, newsletter y "Buenos días", segundo cerebro).
Requisitos: computador y cuenta con acceso a Codex.

### C003 Hermes Agent (bencorde.com/cursos/hermes/)
Etapas: 01 Fundamentos de un agente · 02 Instalación y diagnóstico (local, VPS, Docker, Hermes Doctor) · 03 Telegram y gateway · 04 Skills, MCP y primera web · 05 Memoria y tareas programadas · 06 Correo y newsletter · 07 Publicidad y video (Meta, Higgsfield, HyperFrames) · 08 Respaldo, CRM y cierre (GitHub, GoHighLevel).
Guía de apoyo en el blog: bencorde.com/blog/curso-hermes-agente-ia-espanol/ (PENDIENTE de leer).

### C004 Meta Ads con Claude (bencorde.com/cursos/meta-ads-con-claude/)
Módulos: 01 Marketing Machine · 02 El 80/20 · 03 Meta y los creativos · 04 Contexto y conexión con Claude · 05 Las tres campañas (laboratorio, remarketing, escala) · 06 Videos modulares · 07 Anuncios y resultados · 08 Gráficos con Higgsfield · 09 Ángulos, copy y títulos · 10 El juez de anuncios · 11 La rutina automática · Bonus: leads.
Advertencia del propio autor: la ficha indica que el sistema no garantiza anuncios rentables. Algunas piezas dependen de herramientas de pago (Higgsfield, Meta Ads, Claude).

## Costes que el curso NO incluye (según las propias fichas)
Suscripción de Claude (Pro) o de Codex, Higgsfield, alojamiento (Vercel, VPS), inversión publicitaria en Meta, GoHighLevel. Los cursos son gratuitos; las herramientas no.

## Cursos externos localizados (no verificados todavía)
Ver 22_GITHUB_PROJECTS/GITHUB_PROJECTS.md (leads de búsqueda, estado PENDIENTE).

## Clases propias en construcción
- CLASE 01 — Agente de WhatsApp que atiende y vende: 09_WHATSAPP_AGENTS/CLASE_01_AGENTE_WHATSAPP_VENTAS.md. Basada en recursos MIT/Apache y documentación oficial de Meta y n8n. Sin ejecutar código de terceros.
