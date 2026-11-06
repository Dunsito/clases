> **Traducción no oficial al español.** Original: https://github.com/kousen/codex-training (licencia MIT, autor Kenneth Kousen). Traducido el 2026-11-06. Los comandos, rutas, nombres de archivo, opciones y nombres de herramientas se mantienen en inglés.

# Entrenamiento de OpenAI Codex

Curso práctico para usar OpenAI Codex en la CLI, la aplicación, las extensiones de IDE y los flujos en la nube.

## Visión general del curso

Este taller práctico de 5 horas cubre la instalación, la autenticación, flujos de agente seguros, la configuración, los servidores MCP, las skills, las tareas en la nube y laboratorios de desarrollo práctico.

### Qué aprenderás

- 🚀 **Instalación y configuración**: CLI, aplicación, IDE, inicio de sesión con ChatGPT y autenticación con clave de API
- 🛡️ **Seguridad**: modos de sandbox, políticas de aprobación, proyectos de confianza y revisiones
- 🎯 **Funciones principales**: guía con AGENTS.md, prompts personalizados, perfiles y reanudación de sesiones
- ⚡ **Skills de agente**: paquetes reutilizables de flujos de trabajo con scripts, referencias y recursos
- 🔧 **Capacidades avanzadas**: integración con MCP, Codex Cloud, modelos OSS locales y flujos de CI/CD
- 💻 **Práctica**: ejercicios reales en Java, Python y TypeScript

## Requisitos previos

- Experiencia con la línea de comandos
- Conocimientos básicos de programación en al menos un lenguaje
- Familiaridad con Git
- Docker (para los ejercicios avanzados)

## Estructura del repositorio

```
codex-training/
├── slides.md                     # Presentación Slidev (más de 160 diapositivas)
├── exercises/                    # Laboratorios prácticos con código inicial
│   ├── plan-mode-warmup/        # Lab 0: modo plan y calentamiento
│   ├── java-spring-boot/        # Lab 1: API REST con Spring Boot
│   ├── python-refactoring/      # Lab 2: refactorización de código heredado
│   ├── react-forms/             # Lab 3: formularios en React TypeScript
│   ├── microservices/           # Lab 4: microservicios en varios lenguajes
│   ├── skills-creation/         # Lab 5: crear skills personalizadas de Codex
│   └── mcp-context7/            # Lab 6: conectar documentación actual vía MCP
├── config-examples/              # Configuraciones de ejemplo
│   ├── basic-config.toml        # Configuración mínima para principiantes
│   └── advanced-config.toml     # Todas las funciones con MCP y perfiles
├── prompts/                      # Plantillas de prompts personalizados
│   └── *.md                     # security-audit, test-gen, etc.
├── docs/                         # Documentación de referencia
│   ├── TROUBLESHOOTING.md       # Problemas comunes y soluciones
│   └── MODEL-SELECTION.md       # Guía de coste y rendimiento
├── .github/workflows/            # Ejemplos de CI/CD
│   └── codex-review.yml         # Revisión automática de PR con Codex
└── exports/                      # Exportaciones de las diapositivas (PDF)
```

## Inicio rápido

### 1. Instalar Codex

```bash
# Script oficial de instalación (macOS/Linux)
curl -fsSL https://chatgpt.com/codex/install.sh | sh

# Con npm
npm install -g @openai/codex

# Con Homebrew (macOS/Linux)
brew install --cask codex

# Verificar la instalación
codex --version
```

### 2. Autenticarse

```bash
# Cuenta de ChatGPT (recomendado)
codex login

# O guardar una clave de API en Codex
printenv OPENAI_API_KEY | codex login --with-api-key
```

### 3. Ejecutar el primer comando

```bash
codex "Create a hello world function in Python"
```

### 4. Empezar el curso

```bash
# Clonar este repositorio
git clone https://github.com/kousen/codex-training
cd codex-training

# Instalar las dependencias de las diapositivas
npm install

# Iniciar la presentación
npm run dev

# Abrir en el navegador http://localhost:3030
```

## Diapositivas en línea

Cada push a `main` que modifique `slides.md` reconstruye la presentación dos veces, mediante los flujos de [`.github/workflows/`](.github/workflows/):

- **Versión web** (GitHub Pages): **<https://kousen.github.io/codex-training/>**
- **PDF**: [`codex-training-slides.pdf`](https://github.com/kousen/codex-training/releases/latest/download/codex-training-slides.pdf) desde la versión continua `slides-latest`

## Ejercicios

### Lab 0: calentamiento de planificación y dirección
Aprende el modelo de interacción actual de Codex antes de los laboratorios grandes:
- Pedir a Codex un plan antes de editar
- Dirigir una tarea en curso con mensajes de seguimiento
- Revisar permisos, elección de modelo y diferencias con comandos de barra

**Tiempo**: 15–20 minutos

### Lab 1: API REST con Spring Boot
Construye una API completa de gestión de tareas con Spring Boot, que incluye:
- Operaciones CRUD con validación
- Integración con la base de datos H2
- Documentación OpenAPI
- Suite de pruebas completa

**Tiempo**: 60–90 minutos

### Lab 2: refactorización de código Python
Transforma código Python heredado con buenas prácticas modernas:
- Añadir anotaciones de tipo y documentación
- Implementar patrones de diseño
- Crear una suite de pruebas con pytest
- Configurar herramientas de calidad de código

**Tiempo**: 45–60 minutos

### Lab 3: formularios en React TypeScript
Crea un formulario de registro listo para producción con:
- React Hook Form + Zod para validación
- Cumplimiento de accesibilidad
- Flujo de varios pasos
- Cobertura completa de pruebas

**Tiempo**: 45–60 minutos

### Lab 4: arquitectura de microservicios
Construye un sistema de microservicios orientado a eventos con:
- Varios lenguajes (Node.js, Python, Go, Java)
- Cola de mensajes RabbitMQ
- Orquestación con Docker
- Gateway de API

**Tiempo**: 90–120 minutos

### Lab 5: creación de skills
Crea una skill personalizada de Codex con `$skill-creator`:
- Formato SKILL.md con frontmatter en YAML
- Generador de mensajes de commit convencionales
- Compartir con el equipo a través del repositorio

**Tiempo**: 30 minutos

### Lab 6: servidores MCP con Context7
Conecta Codex a la documentación actual de bibliotecas:
- Añadir Context7 como servidor MCP
- Inspeccionar las herramientas MCP configuradas
- Usar la documentación actual de React Hook Form, Zod, pytest y Spring en los prompts

**Tiempo**: 15–20 minutos

## Funciones clave de Codex cubiertas

### Funciones principales
- ✅ Navegación por la interfaz de terminal
- ✅ Modos de sandbox y políticas de aprobación
- ✅ Memoria de proyecto con AGENTS.md
- ✅ Prompts personalizados y perfiles
- ✅ Gestión y reanudación de sesiones

### Skills de agente
- ✅ Crear paquetes de skills reutilizables
- ✅ Formato y estructura de SKILL.md
- ✅ Invocación explícita (`$skill-name`) e implícita
- ✅ Skills integradas: `$skill-creator`, `$skill-installer`
- ✅ Comparación entre skills y prompts

### Funciones avanzadas
- ✅ Model Context Protocol (MCP)
- ✅ Modelos de OpenAI y proveedores OSS locales mediante Ollama o LM Studio
- ✅ Ejecución como servidor MCP
- ✅ Aplicación Codex, extensiones de IDE y flujos de Codex Cloud
- ✅ Integración con CI/CD
- ✅ Ejecución no interactiva

### Configuración
- ✅ Archivos de configuración TOML
- ✅ Configuración local del proyecto (`.codex/config.toml`)
- ✅ Variables de entorno
- ✅ Políticas de entorno de shell
- ✅ Sistemas de notificación

## Consejos para tener éxito

1. **Empieza con cautela**: usa `workspace-write` con `on-request`, o `read-only` para tareas solo de revisión
2. **Usa AGENTS.md**: aporta contexto para mejores resultados
3. **Crea perfiles**: separa las configuraciones de desarrollo y producción
4. **Revisa el código generado**: nunca aceptes sugerencias de IA a ciegas
5. **Aprovecha MCP**: incorpora documentación actual y datos del proyecto a los prompts
6. **Prueba a fondo**: verifica siempre que el código generado funciona

## Referencia de comandos útiles

```bash
# Uso básico
codex                          # Modo interactivo
codex "prompt"                 # Iniciar con un prompt inicial
codex exec "prompt"            # Ejecutar y salir
codex resume                   # Selector de sesiones para reanudar
codex resume --last            # Reanudar la sesión más reciente
codex update                   # Actualizar la CLI

# Configuración
codex --profile development    # Usar un perfil específico
codex --sandbox read-only      # Definir el modo de sandbox
codex --model gpt-6.1-sol      # Fijar un modelo (/model o codex debug models muestra tu catálogo)
codex --strict-config          # Fallar pronto ante claves de configuración obsoletas o desconocidas
codex --search "latest docs"   # Activar búsqueda web en vivo para esa ejecución

# Avanzado
codex mcp list                 # Listar servidores MCP configurados
codex mcp login server-name    # Inicio de sesión OAuth para servidores MCP compatibles
codex doctor                   # Diagnosticar instalación, configuración, autenticación y estado del entorno
codex cloud exec "prompt"      # Lanzar una tarea en la nube
codex cloud diff               # Inspeccionar los cambios de una tarea en la nube
codex cloud apply              # Aplicar localmente los cambios de una tarea en la nube
codex login --device-auth      # Flujo de autenticación por dispositivo para entornos remotos o sin interfaz
codex review --uncommitted     # Revisar cambios locales
codex review --base main       # Revisar tu rama frente a main
```

Dentro de una sesión interactiva de Codex también puedes invocar skills directamente:

```text
$skill-creator
$skill-installer linear
$create-plan
```

## Recursos

### Materiales del curso
- [Diapositivas del curso](./slides.md): presentación completa en Slidev
- [Ejercicios](./exercises/): laboratorios prácticos con código inicial
- [Guía de solución de problemas](./docs/TROUBLESHOOTING.md): problemas comunes y soluciones
- [Guía de selección de modelos](./docs/MODEL-SELECTION.md): optimización de coste y rendimiento

### Documentación oficial
- [Documentación de la CLI de Codex](https://learn.chatgpt.com/docs/codex/cli)
- [Documentación de la aplicación Codex](https://learn.chatgpt.com/docs/app)
- [Documentación de MCP en Codex](https://learn.chatgpt.com/docs/extend/mcp)
- [Repositorio de GitHub de Codex](https://github.com/openai/codex)
- [Documentación de Agent Skills](https://learn.chatgpt.com/docs/build-skills)
- [Catálogo de skills](https://github.com/openai/skills)
- [Model Context Protocol](https://modelcontextprotocol.io)
- [Especificación agentskills.io](https://agentskills.io)

## Instructor

**Kenneth Kousen**
- Presidente de Kousen IT, Inc.
- Autor y formador técnico
- ken.kousen@kousenit.com
- https://www.kousenit.com

## Contribuir

¿Encontraste un problema o quieres contribuir? Por favor:
1. Abre un issue en GitHub
2. Envía un pull request
3. Comparte tu experiencia

## Licencia

Este material de formación tiene licencia MIT. Consulta el archivo [LICENSE](./LICENSE) para más detalles.

## Agradecimientos

- OpenAI, por Codex
- La comunidad de código abierto, por las herramientas MCP

---

**¿Listo para empezar?** Ve al directorio de [ejercicios](./exercises/) y comienza con el Lab 1.
