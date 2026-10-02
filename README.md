# Bastián Berrios Alarcón

**Ingeniero Civil Industrial** · Developer de IA aplicada, datos y automatización · Chile.

Construyo sistemas end-to-end en Python y TypeScript: agentes sobre LLM, servidores MCP, pipelines de datos y aplicaciones internas desplegadas en la nube.

📫 [bastianberrios.a@gmail.com](mailto:bastianberrios.a@gmail.com) · 💼 [LinkedIn](https://linkedin.com/in/bberrios) · 🌐 [berriosb.dev](https://github.com/berriosb)

---

## 🔭 ¿Qué hago?

- **Servidores MCP** en Python y TypeScript, publicados en PyPI y npm — integración de herramientas y fuentes de datos para agentes LLM.
- **Agentes de IA** con definición de herramientas, manejo de contexto y memoria, y control de errores.
- **Sistemas anti-alucinación**: trazabilidad de la fuente de cada respuesta, límites explícitos y auditoría.
- **Dashboards y analítica de negocio**: tablas KTP/RFM, riesgo crediticio y logística, con deep-linking de cada vista y cálculo en el cliente.
- **Análisis de datos** sobre datos abiertos del Estado chileno (ChileCompra, Banco Central, SERNAC).

---

## 🚀 Proyectos destacados

### 🔌 [powerbi-orchestrator-mcp](https://github.com/berriosb/powerbi-orchestrator-mcp)
**Servidor MCP orquestador en Python — publicado en PyPI.**

Expone 28 herramientas de alto nivel para Power BI y Microsoft Fabric mediante el Model Context Protocol. Delega a motores especializados vía subprocess y presenta al LLM una superficie coherente en vez de primitivas sueltas.

- **931 tests**, 89% de cobertura, `pytest` + `asyncio`
- Dockerfile, `docker-compose`, documentación MCP
- CI con 3 workflows (`verify`, `publish`, `e2e-nightly`), `SECURITY.md`, `CONTRIBUTING.md`
- Logging estructurado con `structlog`, configuración con `pydantic-settings`, auth con `pyjwt` + `azure-identity`
- Instalable con `pip install powerbi-orchestrator-mcp`

`python` `mcp` `model-context-protocol` `fastapi` `docker` `pytest` `azure`

### 🧩 [stitch-mcp-cli](https://github.com/berriosb/stitch-mcp-cli)
**Servidor MCP + CLI en TypeScript — publicado en npm.**

Exporta diseños de Google Stitch a React, Vue, Svelte, Next.js y más, con scaffolding automático para Cursor, Claude Code, VS Code, Codex y OpenCode.

- 2 transportes MCP: **HTTP y stdio**
- **Rate limiting**, logging estructurado con Pino, **caché offline**
- Secrets encriptados con **AES-256-GCM**, TypeScript strict
- Instalable con `pnpm add -g stitch-mcp-cli`

`mcp` `typescript` `node` `cli` `design-to-code` `security`

### 🤖 [data-analytics-agents](https://github.com/berriosb/data-analytics-agents)
**Toolkit de agentes IA para data analytics — publicado en npm.**

5 personas (`data-explorer`, `sql-analyst`, `reporting-analyst`, `ml-modeler`, `using-data-analytics-agents`) + 20 skills (`csv-profiler`, `pandas-cleaning`, `query-validation`, `feature-engineering`, `model-evaluation`, `schema-mapper`, entre otras).

Instalable con `npx data-analytics-agents install --all`. Funciona en OpenCode, Claude Code, Codex y Antigravity CLI.

`ai-agents` `python` `analytics-engineering` `skills`

### 🇨🇱 [chilecompra-anomalias-sql](https://github.com/berriosb/chilecompra-anomalias-sql)
**Análisis de 918.052 órdenes de compra del Estado chileno (2024).**

Detección de concentración de proveedores (índice **HHI**), top anómalos, estacionalidad y patrones territoriales sobre datos abiertos OCDS.

- ETL reproducible en Python + Parquet columnar
- SQL analítico: CTEs, funciones de ventana, 5.321 organismos compradores
- Dashboard público en Next.js 15 + Recharts

`python` `sql` `duckdb` `parquet` `data-analysis` `chile` `open-data`

### 📊 [dashboards-portfolio](https://github.com/berriosb/dashboards-portfolio)
**Vitrina interactiva de 3 tableros de nivel directivo — [demo en vivo](https://dashboards-portfolio.vercel.app).**

- 🛒 **Retail Omnicanal** — matriz RFM 5×5 algorítmica, embudo de conversión, margen, NPS
- 🏦 **Banca & Riesgo Crediticio** — calidad de cartera, mora CMF (30+ / 90+), aging IFRS 9, ROE
- 🚚 **Logística & SCM** — cumplimiento OTIF, lead time P50/P90, concentración de proveedores

Cálculo íntegro en el cliente (0 ms), deep-linking de cada filtro a la URL, y datasets sintéticos declarados como tales.

`typescript` `nextjs` `recharts` `rfm` `bi`

### 📈 [predictor-precio-cobre](https://github.com/berriosb/predictor-precio-cobre)
**Sistema de ML para predecir el precio diario del cobre — [demo en vivo](https://web-theta-teal-22.vercel.app).**

Ridge Regression α=0.1 sobre 29 features (lags, rolling stats, calendario) y 4.137 cierres diarios.

- Validación **walk-forward**: R² promedio **0.957**, MAPE **1.16%**
- **Publica el benchmark completo contra un baseline naïve**: Ridge gana en 2 de 5 ventanas, la persistencia en 3 de 5
- Un R² alto aquí refleja la persistencia de la serie, no una ventaja predictiva del modelo — el dashboard lo dice explícitamente

`python` `scikit-learn` `time-series` `forecasting` `walk-forward-validation`

### 🔌 [Opencode-Acp-Control](https://github.com/berriosb/Opencode-Acp-Control)
**Skill reutilizable para controlar OpenCode por ACP/JSON-RPC 2.0.**

Resuelve el problema de pérdida del transporte stdio cuando un runtime cierra stdin en background, con un controlador FIFO que mantiene el ownership explícito del PID hijo y el drenaje ordenado de stdout.

`python` `acp` `json-rpc` `mcp` `ai-agents`

### 🛡️ [pre-push-qa](https://github.com/berriosb/pre-push-qa)
**Compuerta de calidad pre-push agnóstica al agente.**

Detecta el stack (uv, pnpm, terraform), corre lint y tests, y escribe un marcador antes de cada `git push`. Sin secrets ni hooks invasivos. Instalable con `npx skills add berriosb/pre-push-qa -g`.

`devops` `ci-cd` `qa` `agent-skills`

---

## 🛠️ Stack técnico

| Categoría | Tecnologías |
|---|---|
| **Lenguajes** | Python, TypeScript, SQL, Bash |
| **IA / Agentes** | MCP, tool calling, agentes de datos, AI SDK (OpenAI / Anthropic / Gemini), n8n |
| **Datos** | DuckDB, PostgreSQL, SQLite, Parquet, Pandas, dbt, SQL analítico (CTEs, window functions) |
| **Backend** | FastAPI, REST APIs, Next.js, React, Node.js |
| **ML** | scikit-learn, NumPy, series temporales, validación walk-forward |
| **Nube / DevOps** | Docker, Docker Compose, GitHub Actions, GCP (Cloud Run, Cloud SQL, Secret Manager), Terraform, uv, pnpm |
| **Seguridad** | OAuth2 / JWT, gestión de secretos, cifrado AES-256-GCM, logging estructurado |

---

## 📚 Otros repos

- [omarchy-cyber-ember-theme](https://github.com/berriosb/omarchy-cyber-ember-theme) — tema custom para Omarchy (WCAG AA).

---

## 📫 Contacto

Abierto a roles de **AI Developer / Applied AI Engineer**, Data y Automatización en Chile (presencial Valparaíso/Santiago, híbrido o remoto).

- Email: [bastianberrios.a@gmail.com](mailto:bastianberrios.a@gmail.com)
- LinkedIn: [linkedin.com/in/bberrios](https://linkedin.com/in/bberrios)
- GitHub: [@berriosb](https://github.com/berriosb)
