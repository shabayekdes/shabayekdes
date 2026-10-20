<div align="center">

# Esmail Shabayek

**Senior Backend Engineer · Backend Team Lead · Software Architect**

I design and build backend systems that stay reliable, secure and easy to change<br>
as products, traffic and teams grow.

<a href="https://github.com/shabayekdes"><img src="https://img.shields.io/badge/GitHub-shabayekdes-1a1b27?style=flat&logo=github&logoColor=white" alt="GitHub profile: shabayekdes"></a>
<a href="https://linkedin.com/in/shabayekdes"><img src="https://img.shields.io/badge/LinkedIn-shabayekdes-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn profile: shabayekdes"></a>

</div>

---

## About me

I'm a backend engineer and technical lead with **8+ years** of experience designing and scaling SaaS, e-commerce and mobile backends.

- **Backend & APIs:** multi-tenant SaaS architecture, RESTful API design, authentication and RBAC, caching, background jobs and third-party integrations, mostly in PHP/Laravel, Node.js and Python/Django.
- **Leadership:** promoted from Backend Team Lead to Software Tech Lead; I own architecture and build-vs-buy decisions, lead code reviews and set engineering standards across backend, frontend, mobile, QA and DevOps.
- **Cloud & delivery:** AWS and GCP infrastructure, Docker, CI/CD, monitoring and disaster-recovery planning.

## Highlights from production work

- Designed a **multi-tenant SaaS architecture** with isolated tenant databases and role-based access control for a platform serving car service centers.
- Led **full platform overhauls**: refactoring queries, caching and background jobs, and modernizing infrastructure for a subscription learning platform and its mobile apps.
- Integrated **ZATCA e-invoicing**, accounting, payment gateways and shipping carriers through REST APIs and SDKs.
- Improved e-commerce search with **Elasticsearch** custom mappings and queries.
- Built **CI/CD pipelines** (Jenkins, GitLab CI/CD) with automated testing and fast rollback, and tuned **AWS** (EC2, RDS, S3, ElastiCache) for availability and cost.

## Engineering focus

| Area | What it means in practice |
| --- | --- |
| **Backend architecture** | Clear module boundaries, explicit trade-offs, designs a team can evolve |
| **Multi-tenant SaaS** | Tenant isolation (shared schema or separate databases), tenant-scoped data and permissions |
| **API engineering** | Versioned REST APIs, OAuth2/JWT, validation, consistent errors, OpenAPI contracts |
| **Data & search** | Relational modeling, indexing, caching with Redis, search with Elasticsearch |
| **Integrations** | Payments, e-invoicing, accounting, shipping and SMS providers |
| **Cloud infrastructure** | AWS, GCP, Linux, Nginx, Docker, CI/CD |
| **Technical leadership** | Architecture reviews, code reviews, mentoring, engineering standards |

## Tech stack

**Backend**

<p>
  <img src="https://skillicons.dev/icons?i=php,laravel,symfony,nodejs,nestjs,express,python,django&theme=dark" alt="PHP, Laravel, Symfony, Node.js, NestJS, Express, Python and Django">
</p>

**Data & search**

<p>
  <img src="https://skillicons.dev/icons?i=mysql,postgres,mongodb,redis,elasticsearch&theme=dark" alt="MySQL, PostgreSQL, MongoDB, Redis and Elasticsearch">
</p>

**Cloud & DevOps**

<p>
  <img src="https://skillicons.dev/icons?i=aws,gcp,linux,nginx,docker,jenkins,gitlab,githubactions,git&theme=dark" alt="AWS, Google Cloud, Linux, Nginx, Docker, Jenkins, GitLab, GitHub Actions and Git">
</p>

**Currently learning & building with**

<p>
  <img src="https://skillicons.dev/icons?i=go,ts&theme=dark" alt="Go and TypeScript">
</p>

## Featured projects

### [FleetOps](https://github.com/shabayekdes/nestjs-fleetops) · NestJS · TypeScript · PostgreSQL

A B2B multi-tenant fleet management platform (vehicles, drivers, assignments, maintenance and fuel records), built in documented phases to learn the Node.js/NestJS ecosystem with production-grade practices.

- **Multi-tenancy:** shared schema with an `organizationId` on every tenant-owned table, tenant-scoped uniqueness, and tenant context taken only from the access token, never from the request body or URL.
- **Security by default:** a global JWT guard on every route unless it opts out, Argon2id password hashing, uniform login failures with timing mitigation, per-account and per-IP rate limiting, and roles.
- **API contract:** versioned REST API with a committed OpenAPI document; CI fails if the contract or the generated frontend types drift.
- **Testing & delivery:** unit and end-to-end suites per module, including unauthenticated and cross-tenant cases; Playwright tests for the Next.js web app; Docker images and automated deployment with database migrations.
- **Telemetry:** an optional MongoDB store for append-only vehicle readings with retention and geospatial queries, kept apart from the transactional PostgreSQL core.

### [Laravel Payment](https://github.com/shabayekdes/laravel-payment) & [Laravel SMS](https://github.com/shabayekdes/laravel-sms) · Open source

Two open-source Laravel packages, published on Packagist ([payment](https://packagist.org/packages/shabayek/laravel-payment), [SMS](https://packagist.org/packages/shabayek/laravel-sms)), that put third-party integrations behind a single, driver-based API.

- **Payment:** a unit-tested package with Paymob, Mastercard and cash-on-delivery drivers, a `Billable` trait for customer data, and callback verification. Still early-stage: its README marks it as not production-ready.
- **SMS:** support for multiple SMS providers (SMS EG, SMS Misr, Victory Link, Ooredoo), OTP send and verify, Arabic/English messages, and a contract for adding custom gateways.

### [CloudKit CLI](https://github.com/shabayekdes/cloudkit-cli) · Bash · AWS · Google Cloud

Shell helpers for AWS and Google Cloud: source one file to get interactive session management, service wrappers and a color-coded prompt across both clouds.

- **Sessions:** profile and configuration pickers for AWS (SSO, static keys, chained role assumption) and gcloud, with a prompt showing the active account and project, and warnings before AWS credentials expire.
- **AWS:** EC2 over SSM (interactive sessions, port forwarding, file upload with checksum verification) and ECS (clusters, services, tasks, logs, `exec` into containers).
- **Google Cloud:** GCE instance listing, SSH and SCP, plus rolling restart and replace for managed instance groups.
- **Quality:** ShellCheck and credential-free smoke tests run in GitHub Actions on every push and pull request.

<!--
  PulseFlow: no public repository was found under github.com/shabayekdes.
  When it is public, replace the placeholders below and remove this comment wrapper.

### [PulseFlow](https://github.com/shabayekdes/REPLACE-WITH-REPO-NAME) · REPLACE-WITH-STACK

One-sentence purpose of the project.

**Implemented**
- REPLACE: only what is built and working today.

**In progress / planned**
- REPLACE: learning-stage or roadmap items.
-->

## Currently exploring

- **Go** and its concurrency model: goroutines, channels and patterns for bounded, cancellable work
- **Distributed systems:** consistency, messaging, idempotency and handling partial failure
- **System design** for high availability and horizontal scalability
- **Cloud infrastructure, observability and reliability:** tracing, metrics and resilience patterns

## Engineering principles

- **Maintainability over cleverness.** Prefer the simplest design that meets today's needs and leaves room for tomorrow's.
- **Make trade-offs explicit.** Write down why a decision was made and what it costs.
- **Reliability, security and performance are features.** Design for failure, least privilege and measured performance from the start.
- **Code should be testable and readable.** If it's hard to test, the design usually needs work.
- **Build systems teams can operate.** Good defaults, clear logs and boring deployments.

## GitHub activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=shabayekdes&show_icons=true&include_all_commits=true&rank_icon=github&theme=tokyonight&hide_border=true" alt="GitHub statistics for shabayekdes">
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=shabayekdes&layout=compact&langs_count=6&exclude_repo=alx-backend,alx-backend-javascript,alx-backend-python,alx-backend-storage,alx-backend-user-data,alx-files_manager,alx-higher_level_programming,alx-interview,alx-low_level_programming,alx-system_engineering-devops,alx-pre_course,alx-zero_day,zero_day,printf,simple_shell,binary_trees,sorting_algorithms,AirBnB_clone,AirBnB_clone_v2,AirBnB_clone_v3,AirBnB_clone_v4,Fix_My_Code_Challenge,what-happens-when,leetcode-problems&theme=tokyonight&hide_border=true" alt="Most used languages in shabayekdes's public project repositories">
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=shabayekdes&theme=tokyonight&hide_border=true" alt="GitHub contribution streak for shabayekdes">
</p>

<sub>Statistics are generated by third-party services and may occasionally be unavailable. Language breakdown reflects code in public project repositories (coursework excluded), not proficiency.</sub>

## Contact

The best way to reach me is on [LinkedIn](https://linkedin.com/in/shabayekdes). You can find my code here on [GitHub](https://github.com/shabayekdes).
