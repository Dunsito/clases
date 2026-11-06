# Cursos en GitHub — catálogo verificado (2026-11-06, con acceso a la API)
Método: GitHub API `search/repositories` (metadatos y licencia de la API) + lectura del README con `raw.githubusercontent.com`. No se ha leído el árbol completo de cada repo (las páginas de árbol y la API de contenidos están bloqueadas para repos externos sin `add_repo`). Por eso el estado distingue "README leído" de "contenido completo verificado" (este último no se alcanzó en ningún caso).
Licencia: la indicada por la API de GitHub (spdx). "none" = el repo no tiene LICENSE → todos los derechos reservados, solo lectura.

## Cursos gratuitos / open source (README leído)
| ID | Repositorio | Tema | Licencia | Estrellas | Qué dice el README | Estado |
|---|---|---|---|---|---|---|
| GC001 | huggingface/mcp-course | MCP | Apache-2.0 | 925 | Curso de Model Context Protocol. El enlace de registro aparece como "Coming Soon". | [VERIFICADO_OPEN_SOURCE]; unidades no abiertas |
| GC002 | decodingai-magazine/building-a-coding-agent-from-scratch-course | Harness de agentes / Claude Code desde cero | Apache-2.0 | 1.127 | Curso open source con esquema de contenidos. Coste $0 con tiers gratuitos (Gemini, OpenRouter :free, $30 de créditos en Modal como opción recomendada). | [VERIFICADO_CURSO_GRATUITO] |
| GC003 | kousen/codex-training | Codex CLI | MIT | 37 | Taller práctico de 5 horas: instalación, autenticación, flujos seguros, configuración, MCP, skills, tareas en la nube y laboratorios. Incluye slides y ejercicios. | [VERIFICADO_CURSO_GRATUITO] |
| GC004 | zorost/AI-Engineering-Lab | Ingeniería de IA, 24 semanas | MIT | 315 | Programa gratuito de 24 semanas, sin registro. Semanas 1–13 sin API de pago; 18–24 con tiers gratuitos. Tiene notebooks. | [VERIFICADO_CURSO_GRATUITO] |
| GC005 | justxor/claude-code-pro-course | Claude Code (ruso) | MIT | 344 | Curso práctico de Claude Code: CLAUDE.md, settings, skills, subagents, hooks, MCP, plugins, headless y CI, con laboratorios. | [VERIFICADO_CURSO_GRATUITO] (idioma ruso) |
| GC006 | neural-maze/realtime-phone-agents-course | Agentes de voz / agente telefónico | MIT | 1.117 | Curso "Phone Calling Agents": FastRTC, Superlinked, Twilio, Opik, RunPod. Lecciones 0–n con pasos. | [VERIFICADO_CURSO_GRATUITO] — útil para voz; requiere cuentas de Twilio y RunPod (coste) |
| GC007 | decodingai-magazine/enterprise-mcp-course | MCP en empresa | MIT | 278 | Serie open source "Designing Enterprise MCP Systems" con esquema y prerrequisitos. | [VERIFICADO_OPEN_SOURCE] |
| GC009 | ai-builders-group/build-production-ai-agents | Agentes en producción con LangGraph, Pydantic, Docker | MIT | 67 | Código de laboratorio open source del libro "Production-Ready AI Agents" (de pago). El curso escrito no es gratuito. | [VERIFICADO_OPEN_SOURCE]; el libro no |
| GC010 | microsoft/ai-agents-for-beginners | Agentes de IA para principiantes | MIT | 79.100 | 18 lecciones (verificado en sesión anterior). | [VERIFICADO_CURSO_GRATUITO] |
| GC011 | rohitg00/ai-engineering-from-scratch | Ingeniería de IA desde cero | MIT | 77.100 | Currículo y skills (nº de lecciones según snippet). | [VERIFICADO_OPEN_SOURCE] |
| GC012 | dannyblaker/rag-tutorial | RAG | Apache-2.0 | 20 | 6 lecciones y 3 ejemplos (verificado en sesión anterior). | [VERIFICADO_CURSO_GRATUITO] |
| GC013 | NirDiamant/RAG_Techniques | RAG avanzado | ver nota | 30.300 | Un notebook por técnica. | [VERIFICADO_OPEN_SOURCE]; licencia [PENDIENTE] |
| GC014 | minicoohei/ai-agent-camp | Agentes para no ingenieros | ver nota | 347 | Lecciones, skills y hooks para Claude Code, Cursor y Codex. | [VERIFICADO_OPEN_SOURCE]; licencia [PENDIENTE] |

## Solo lectura: sin licencia (no reutilizar)
| ID | Repositorio | Tema | Estrellas | Nota | Estado |
|---|---|---|---|---|---|
| GC015 | MohElshamy1994/n8n-course-Projetcs | n8n: agentes de IA (2025) | 863 | Proyectos del curso de YouTube del autor. README leído. Sin licencia. | [VERIFICADO_TERCEROS] |
| GC016 | tylerprogramming/n8n-full-beginner-course | n8n desde cero | 65 | Colección de workflows JSON por nivel y plantillas CSV. README leído. Sin licencia. | [VERIFICADO_TERCEROS] |
| GC017 | datawhalechina/easy-vibe | Vibe coding 101 | 20.372 | Guía práctica de vibe coding. README leído. Sin licencia (la API no detecta licencia). | [VERIFICADO_TERCEROS] |

## Restringidos (companion de cursos de pago)
| ID | Repositorio | Motivo | Estado |
|---|---|---|---|
| GC018 | tobiaszwingmann/n8n-ai-bootcamp | Repositorio oficial de un evento en directo de O'Reilly (de pago). README leído. | [ACCESO_RESTRINGIDO] |
| GC019 | LinkedInLearning/build_AI_agents_with-n8n-4103420 (y otros 3 repos LinkedIn Learning de n8n y Codex) | Código de ejercicios de cursos de pago de LinkedIn Learning. Licencia "NOASSERTION". | [ACCESO_RESTRINGIDO] |

## Leads sin abrir (solo metadatos de la API)
- carlvellotti/free-ai-courses (2.202 ★, licencia NOASSERTION) — curso interactivo para product managers con Claude Code. [PENDIENTE]
- carlvellotti/claude-code-everyone-course (576 ★, sin licencia) — "Claude Code for Everyone" dentro de Claude Code. [PENDIENTE]
- carlvellotti/codex-pm-course (14 ★, sin licencia) — curso de Codex para PM. [PENDIENTE]
- artem-istranin/codex-course (3 ★, sin licencia). [PENDIENTE]
- cemergin/openclaw-course (0 ★, sin licencia) — desplegar OpenClaw en VPS. [PENDIENTE]
- M-F-Tushar/AI-Builder-with-n8n-Create-Agents-Voice-Agents (9 ★) — n8n con agentes de voz. [PENDIENTE]
- bhanuchaddha/CrewAI-Crash-Course (2 ★, sin licencia) — 7 módulos de CrewAI. [PENDIENTE]
- DanielPuentee/autogen-groq-multiagent-analyser (3 ★, MIT). [PENDIENTE]
- TemaBlag/RAG (2 ★, MIT) — notebooks de "RAG from Scratch" de LangSmith. [PENDIENTE]
- ChidambaraRaju/RAG-from-scratch-with-langchain-and-langgraph (2 ★, MIT). [PENDIENTE]
- MateoProjects/RAG-Agents-for-LLM-course (35 ★, 2024). [PENDIENTE]
- MarkShawn2020/DeepLearning.ai-Courses-ClaudeCode (339 ★, sin licencia) — notas de un curso de DeepLearning.AI, en chino. [PENDIENTE]
- fufankeji/VibeCodingCourse_v1 (126 ★, sin licencia). [PENDIENTE]
- Koomook/fastcampus-ai-agent-vibecoding (135 ★, sin licencia) — materiales de un curso de pago. [PENDIENTE]
- sysdr/AI-Agent-Mastery (32 ★, sin licencia) — "3 lecciones gratuitas" con curso de pago. [PENDIENTE]
- brivenai-oss/automation-course (0 ★) y muyinzad/ai-automation-mastery (0 ★) — cursos de n8n/Make/Zapier. Baja calidad aparente. [PENDIENTE]
