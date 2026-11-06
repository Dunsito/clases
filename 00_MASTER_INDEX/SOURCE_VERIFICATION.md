# Verificación de fuentes — 2026-11-06 (UTC ~21:55–21:56)
Método: apify/web-fetch (HTTP 200 comprobado). Un recurso solo se marca VERIFICADO si su página se leyó. Mencionar un recurso en un buscador no basta.

| URL | Estado | Qué se comprobó |
|---|---|---|
| https://www.skool.com/imperio/about | [ACCESO_RESTRINGIDO] | Página pública leída: comunidad de pago $59/mes, 4,2k miembros, temas anunciados. Contenido de clases no accesible. |
| https://bencorde.com/cursos/ | [VERIFICADO_OFICIAL] | Índice de 4 cursos gratuitos. Autor: Benjamín Cordero. |
| https://bencorde.com/cursos/claude-code/ | [VERIFICADO_OFICIAL] | Temario 00–16 + bonus, 7 proyectos, requisitos. |
| https://bencorde.com/cursos/codex/ | [VERIFICADO_OFICIAL] | Temario 00–16, 10 proyectos. |
| https://bencorde.com/cursos/hermes/ | [VERIFICADO_OFICIAL] | 8 etapas, enlace a YouTube. |
| https://bencorde.com/cursos/meta-ads-con-claude/ | [VERIFICADO_OFICIAL] | Temario 01–11 + bonus. |
| https://bencorde.com/biblioteca/ | [VERIFICADO_OFICIAL] | 4 rutas. |
| https://bencorde.com/recursos/ | [VERIFICADO_OFICIAL] | Enlaces a cursos + 1 descarga TXT (no descargada). |
| https://bencorde.com/temas/claude-code/ | [VERIFICADO_OFICIAL] | Ruta + 23 guías listadas. |
| https://bencorde.com/temas/codex/ | [VERIFICADO_OFICIAL] | Ruta + 10 guías listadas. |
| https://bencorde.com/temas/agentes-ia/ | [VERIFICADO_OFICIAL] | Ruta + 23 guías listadas. |
| https://bencorde.com/temas/automatizacion-con-ia/ | [VERIFICADO_OFICIAL] | Ruta + 19 guías listadas. |
| https://claudecode.imperioagentico.com/ | [VERIFICADO_CURSO_GRATUITO] | Landing de registro: "100% gratis", 17 módulos, 52 temas, 7 proyectos. Texto de estreno "31 de julio" (fecha antigua en la página). |
| https://codex.imperioagentico.com/ | [VERIFICADO_CURSO_GRATUITO] | Landing: curso y guía PDF gratis, 10 proyectos, 17 módulos. |
| https://anuncios.imperioagentico.com/ | [VERIFICADO_CURSO_GRATUITO] | Landing: gratis, 3:09:02, 11 módulos + bonus. |
| https://www.youtube.com/@bencord | [PENDIENTE_VERIFICACION] | No accesible desde el sandbox (CONNECT 403 / sin conexión). |
| https://www.youtube.com/watch?v=FQZGoSwdS_0 | [PENDIENTE_VERIFICACION] | Enlace del curso de Hermes; no abierto. |
| https://bencorde.com/blog/* (69 guías) | [PENDIENTE_VERIFICACION] | Listadas en índices oficiales, contenido no leído. |
| https://github.com/* (leads) | [PENDIENTE_VERIFICACION] | Solo snippets de búsqueda. Ver 22_GITHUB_PROJECTS. |
| https://www.youtube.com/watch?v=xgNykmTdM-w | [PENDIENTE_VERIFICACION] | Solo snippet de búsqueda. |
| https://learn.chatgpt.com/docs/projects | [PENDIENTE_VERIFICACION] | Enlace de la guía Codex; no abierto. |
| https://claudecode.imperioagentico.com/guia | [PENDIENTE_VERIFICACION] | Guía/cheat sheet del curso de Claude Code: requiere registro con correo. |
| https://bencorde.com/blog/videos-infantiles-ia-n8n/recursos/brief-direccion-creativa.txt | [PENDIENTE_VERIFICACION] | Descarga TXT, no descargada. |

Dominios inaccesibles desde el sandbox (proxy): youtube.com (vídeo), arxiv.org, docs.n8n.io, learn.microsoft.com, deeplearning.ai, freecodecamp.org, huggingface.co, docs.anthropic.com. Solo se alcanzan vía Apify web-fetch/web-search; GitHub responde parcialmente (api.github.com/search → 403).
