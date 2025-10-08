# 🧠 Prompt Engineering Cheat Sheet for Developers

**Goal:** Empower you to use AI to build, maintain, or scale real-world systems.

---

## 📌 Prompt Anatomy

A well-structured prompt often includes:

1. **Role** — who the AI should be.
2. **Objective** — what you want to accomplish.
3. **Context** — background, requirements, existing code.
4. **Constraints** — format, libraries, performance, style.
5. **Output Type** — code, explanation, architecture diagram, etc.

```txt
You are a [ROLE]. I'm working on [PROJECT CONTEXT].
Objective: [WHAT YOU WANT]
Constraints: [RULES, TECHNICAL PREFERENCES]
Return: [FORMAT OR STYLE]
```

---

## 🚀 General Templates

### 🧱 System Development (Full Stack App)

```
You are a senior software architect. I want to build a full-stack web application for [use case or industry].

Requirements:
- Frontend using [framework] with [UI library] and responsive design
- Backend with [framework] and [DB]
- Authentication, authorization, CRUD for [entities]
- Admin dashboard and user dashboard
- API and WebSocket integration
- Unit tests and CI/CD support

Generate:
1. System architecture (text + component breakdown)
2. Database schema in [ORM or SQL]
3. API endpoint spec (REST or GraphQL)
4. Initial backend code structure with folders and sample code
5. Sample frontend UI code for one screen
6. Project setup instructions
```

---

### 🧩 Feature Development

```
You are a senior developer. I need to implement [feature] in my [framework/language] project.

Context: [brief description or existing code]
Requirements:
- It should support [edge cases, performance goals]
- Must follow [code style or framework conventions]
- Add [tests, types, logging, etc.]

Output:
- Complete implementation with comments
- Sample input/output
- Integration guidance
```

---

### 🧼 Refactoring & Optimization

```
You are a code quality expert. Refactor the following [language] code to:
- Improve performance
- Follow [style guide]
- Use idiomatic patterns
- Add type hints and error handling
[Paste code]
```

---

### 🔍 Code Review / Audit

```
You're a software engineering lead. Review this [language/framework] code and provide:
1. A list of problems or smells
2. Suggestions with reasons
3. A rewritten version following best practices
[Paste code]
```

---

## 🏗 Complex System Templates

### 💡 SaaS App (Multi-Tenant)

```
You're an enterprise architect. I need a multi-tenant SaaS app with:
- Role-based access control
- Organizations and users
- Subscription plans and billing
- REST API and real-time updates
- Admin panel for managing tenants
- PostgreSQL + Redis + background jobs

Deliver:
1. Multi-tenant DB schema (PostgreSQL, with tenant isolation)
2. Role model and permission table design
3. API endpoints spec with versioning
4. Folder structure for backend/frontend
5. Auth flows: signup, login, reset password, invite user
6. Tech stack recommendation and rationale
```

---

### 📱 Mobile App (Flutter/React Native)

```
You are a mobile dev lead. I want a cross-platform app for [use case].

Requirements:
- UI in [Flutter/React Native]
- State management with [e.g. Riverpod, Redux]
- Local storage + API sync
- Camera + file upload + push notifications
- Authentication (JWT or Firebase)

Create:
1. Project folder layout
2. One screen UI with navigation
3. API service abstraction layer
4. Sample login/signup logic
5. Error handling and offline mode strategy
```

---

### ⚙️ Microservices Backend

```
You are a backend systems architect. Design a microservices-based architecture for a platform like [YouTube/Stripe/Airtable].

Requirements:
- Services: user, content, billing, analytics
- Message queue (Kafka or RabbitMQ)
- API gateway and service discovery
- Docker + Kubernetes for orchestration
- CI/CD pipelines with GitHub Actions

Deliver:
1. Service responsibilities
2. Tech stack per service
3. Async messaging patterns and payload examples
4. Database per service design
5. Deployment structure (Dockerfile + Helm charts outline)
```

---

## 📖 Documentation / Planning Templates

### 🗂 API Design

```
You are an API design expert. Define a RESTful API spec for a [resource] with CRUD, pagination, filtering, sorting, and nested relationships.

Include:
- Endpoint paths
- Methods and status codes
- Request and response JSON
- Query param examples
```

---

### 📝 PRD (Product Requirements Document)

```
You're a product manager. Draft a PRD for a feature called [feature name] in our app.

Include:
1. Objective and overview
2. Use cases and user stories
3. UI mockup description (or layout text)
4. Non-functional requirements
5. Metrics for success
```

---

## ⚡ Rapid Engineering Prompts

| Task         | Prompt                                                                              |
| ------------ | ----------------------------------------------------------------------------------- |
| Add Caching  | “Add Redis-based caching to this endpoint for 5 mins. Invalidate on update.”        |
| Add Logging  | “Add structured logging using \[library] to this function.”                         |
| Add Tests    | “Generate unit tests using \[testing framework] for this service.”                  |
| Convert Code | “Convert this JS to TS and add types, interfaces, and JSDoc.”                       |
| Deploy App   | “Write a `Dockerfile` and `docker-compose.yml` to deploy this app with PostgreSQL.” |

---

## 📦 Reusable Role Directives

| Role                                         | Use                                    |
| -------------------------------------------- | -------------------------------------- |
| **“You're a senior software architect”**     | Full system design, scalable decisions |
| **“You're a code reviewer”**                 | Clean code, refactoring, reviews       |
| **“You're a security expert”**               | Secure API, auth, validation, OWASP    |
| **“You're a CI/CD DevOps engineer”**         | Docker, GitHub Actions, K8s            |
| **“You're a frontend performance engineer”** | Optimize Vue/React for speed           |

---

## 🏢 Example 1: Enterprise CRM System (Full-Stack App)

### 🔧 Prompt:

```
You are a senior software architect. I need to design a CRM system for a mid-sized business.

Requirements:
- React frontend with TailwindCSS
- Node.js backend with PostgreSQL (using Sequelize)
- Features: Leads, Contacts, Companies, Opportunities
- Role-based access control (Admin, Sales, Support)
- REST API with OpenAPI documentation
- Background jobs for email reminders
- OAuth2 login with Google
- Dockerized and deployable to AWS ECS

Deliver:
1. System architecture with service boundaries
2. Entity-relationship diagram in SQL format
3. REST API spec for /leads and /contacts
4. Folder structure for backend/frontend
5. Docker setup (Dockerfile and docker-compose.yml)
```

---

## 🧾 Example 2: Invoice Scanning OCR SaaS

### 🔧 Prompt:

```
You are a backend engineer. I'm building an invoice scanning system.

Requirements:
- Python backend with FastAPI
- OCR using PaddleOCR
- Upload image or PDF, extract date, amount, vendor
- Return JSON with confidence scores
- Support Japanese, English, and French
- Logging, validation, and graceful error handling
- CI pipeline with GitHub Actions

Tasks:
1. Define folder layout for modular FastAPI app
2. Write OCR service abstraction with fallback logic
3. Add Pydantic models with types and validators
4. Generate OpenAPI doc and sample POST request
```

---

## 🏭 Example 3: IoT Monitoring Platform (Real-Time Data)

### 🔧 Prompt:

```
You are a systems architect. I need to design an industrial IoT monitoring platform.

Context:
- Devices send telemetry via MQTT (temperature, humidity, battery)
- Backend ingests via MQTT broker (Eclipse Mosquitto)
- Store in time-series database (InfluxDB)
- Display in Vue 3 dashboard (WebSocket for real-time updates)
- Alert rules for threshold breaches
- Admin UI for device config, provisioning, logs

Tasks:
1. End-to-end architecture overview
2. Device-to-cloud message format (JSON schema)
3. WebSocket event payload spec
4. Vue 3 component skeleton for real-time graph
5. Device provisioning API
```

---

## 📱 Example 4: Fintech Mobile App (Cross-Platform)

### 🔧 Prompt:

```
You are a senior mobile engineer. I’m building a Flutter app for personal finance.

Requirements:
- Track income/expenses, bank accounts, savings goals
- Sync data with a Django REST API
- Firebase authentication (email/password, Google)
- Offline-first using Hive
- Responsive UI with dark mode
- State management using Riverpod
- CI/CD pipeline using Codemagic

Deliver:
1. Flutter folder structure and package list
2. Authentication flow logic (provider + UI)
3. Offline sync strategy
4. Sample income/expense form with validation
5. Testing strategy for UI and logic
```

---

## 🎯 Example 5: B2B Analytics SaaS (Multi-Tenant)

### 🔧 Prompt:

```
You are a SaaS systems architect. I need a multi-tenant analytics platform.

Features:
- Each company has users, dashboards, and datasets
- Dashboards support charts and exports (CSV, PDF)
- Backend: Django + PostgreSQL (tenant-aware schema)
- Frontend: React + D3.js for charts
- Auth: JWT, organization scoping
- S3 storage for uploaded datasets
- Background processing with Celery + Redis
- Metrics for billing (API usage, storage)

Tasks:
1. Multi-tenant DB design (PostgreSQL schemas or discriminator field)
2. Dashboard JSON spec for rendering
3. Async data import and transformation worker
4. Secure S3 upload API with presigned URLs
5. Folder layout for backend/frontend
```

---

## 📂 Example 6: Developer Tooling (CLI + API)

### 🔧 Prompt:

```
You're a senior Python developer. I want to build a CLI + REST API tool for managing secrets and configs.

Requirements:
- Python CLI using `click`
- REST API with FastAPI
- AES-256 encryption of values
- YAML config loader
- Dockerfile and CI for lint/test
- Store in SQLite or Postgres
- JSON-based logging with timestamps

Deliver:
1. CLI command structure: `secrets add/get/list`
2. REST endpoints for CRUD with encryption/decryption
3. Secure key storage strategy
4. Sample test cases with pytest
5. Dockerfile and GitHub Actions workflow
```

## 📂 Example 7: Optimize and refactor

### 🔧 Prompt:

You are a code quality expert. Refactor the code in the `frontend` folder built with **React + TypeScript + TailwindCSS** to:

- Improve rendering performance and minimize re-renders (e.g., use `memo`, `useCallback`, `useMemo`)
- Enforce idiomatic React and TypeScript practices
- Ensure consistent and scalable use of Tailwind utility classes
- Refactor components for readability, reusability, and maintainability
- Add TypeScript type annotations and interfaces where missing
- Follow best practices from the [Airbnb React/JSX Style Guide](https://github.com/airbnb/javascript/tree/master/react)
- Handle errors gracefully, especially in async calls and data fetching
- Organize code according to domain-driven component structure (e.g., `components/`, `hooks/`, `utils/`, `types/`)

Make the refactored code production-ready and ensure it adheres to modern frontend development standards.

### Sample

Read the implementation proposal from docs/todo-2.md. i want that you make your own analysis and assumptions since you have higher knowledge and usually implement things better. take the proposal as a starting point. if you're 9/10 sure that you can implement the fix then do it if not come back with clarifying questions.
