<div align="center">

# Esmail Shabayek

**Senior Backend Engineer · Technical Lead · Backend Architecture**

I design and build backend systems that stay reliable, secure, and easy to change<br>
as products, traffic, and teams grow.

<a href="https://github.com/shabayekdes">
  <img src="https://img.shields.io/badge/GitHub-shabayekdes-1a1b27?style=flat&logo=github&logoColor=white" alt="GitHub profile: shabayekdes">
</a>
<a href="https://linkedin.com/in/shabayekdes">
  <img src="https://img.shields.io/badge/LinkedIn-shabayekdes-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn profile: shabayekdes">
</a>

</div>

---

## About me

I'm a backend engineer and technical lead with **8+ years of experience** designing and scaling SaaS, e-commerce, and mobile backends.

- **Backend & APIs:** Multi-tenant SaaS architecture, REST API design, authentication and RBAC, caching, background jobs, and third-party integrations, primarily with PHP/Laravel, Node.js, and Python/Django.
- **Leadership:** Progressed from Backend Team Lead to Software Tech Lead. I contribute to architecture and build-vs-buy decisions, lead code reviews, and establish engineering standards across backend, frontend, mobile, QA, and DevOps.
- **Cloud & delivery:** AWS and GCP infrastructure, Docker, CI/CD, monitoring, and disaster-recovery planning.

## Highlights from production work

- Designed a **multi-tenant SaaS architecture** with isolated tenant databases and role-based access control for a platform serving car service centers.
- Led **platform overhauls**, including query refactoring, caching, background jobs, and infrastructure modernization for a subscription learning platform and its mobile apps.
- Integrated **ZATCA e-invoicing**, accounting systems, payment gateways, and shipping carriers through REST APIs and SDKs.
- Improved e-commerce search using **Elasticsearch** custom mappings and queries.
- Built **CI/CD pipelines** with Jenkins and GitLab CI/CD, automated testing, and rollback workflows; tuned AWS services including EC2, RDS, S3, and ElastiCache for availability and cost.

## Engineering focus

| Area | What it means in practice |
| --- | --- |
| **Backend architecture** | Clear module boundaries, explicit trade-offs, and designs teams can evolve |
| **Multi-tenant SaaS** | Tenant isolation, separate or shared database strategies, tenant-scoped data, and permissions |
| **API engineering** | Versioned REST APIs, OAuth2/JWT, validation, consistent errors, and OpenAPI contracts |
| **Data & search** | Relational modeling, indexing, Redis caching, and Elasticsearch |
| **Integrations** | Payments, e-invoicing, accounting, shipping, and SMS providers |
| **Cloud infrastructure** | AWS, GCP, Linux, Nginx, Docker, and CI/CD |
| **Technical leadership** | Architecture reviews, code reviews, mentoring, and engineering standards |

## Tech stack

**Backend**

<img src="https://skillicons.dev/icons?i=php,laravel,symfony,nodejs,nestjs,express,py,django&theme=dark" alt="PHP, Laravel, Symfony, Node.js, NestJS, Express, Python, and Django">

**Data stores**

<img src="https://skillicons.dev/icons?i=mysql,postgres,mongodb,redis,elasticsearch&theme=dark" alt="MySQL, PostgreSQL, MongoDB, Redis, and Elasticsearch">

**Infrastructure**

<img src="https://skillicons.dev/icons?i=aws,gcp,linux,nginx,docker,jenkins,gitlab,githubactions,git&theme=dark" alt="AWS, Google Cloud, Linux, Nginx, Docker, Jenkins, GitLab, GitHub Actions, and Git">

**Currently learning**

<img src="https://skillicons.dev/icons?i=go,ts&theme=dark" alt="Go and TypeScript">

## Featured projects

### [FleetOps](https://github.com/shabayekdes/nestjs-fleetops) · NestJS · TypeScript · PostgreSQL

A B2B multi-tenant fleet management platform covering vehicles, drivers, assignments, maintenance, and fuel records. The project is being developed in documented phases to deepen my experience with the Node.js/NestJS ecosystem and production-oriented engineering practices.

- **Multi-tenancy:** Shared-schema design with an `organizationId` on tenant-owned tables, tenant-scoped uniqueness, and tenant context derived from the access token rather than the request body or URL.
- **Security:** Global JWT guard with explicit public-route opt-outs, Argon2id password hashing, uniform login failures with timing mitigation, per-account and per-IP rate limiting, and role-based authorization.
- **API contract:** Versioned REST API with a committed OpenAPI document; CI checks for contract and generated frontend type drift.
- **Testing & delivery:** Unit and end-to-end tests, including unauthenticated and cross-tenant scenarios; Playwright tests for the Next.js web app; Docker images and automated deployment with database migrations.
- **Telemetry:** Optional MongoDB storage for append-only vehicle readings, retention, and geospatial queries, separate from the transactional PostgreSQL core.

**Planned, not implemented yet:** Extracting telemetry into a separate service, Redis caching, a message broker with the outbox pattern, and distributed tracing.

### [Laravel Payment](https://github.com/shabayekdes/laravel-payment) & [Laravel SMS](https://github.com/shabayekdes/laravel-sms) · PHP · Laravel · Open source

Two open-source Laravel packages published on Packagist that provide a driver-based interface for third-party integrations: [Laravel Payment](https://packagist.org/packages/shabayek/laravel-payment) and [Laravel SMS](https://packagist.org/packages/shabayek/laravel-sms).

- **Payment:** Drivers for Paymob, Mastercard, and cash on delivery, a `Billable` trait for customer data, and callback verification. **Early-stage:** the repository README states that it is not production-ready.
- **SMS:** Drivers for multiple SMS providers, including SMS EG, SMS Misr, Victory Link, and Ooredoo; OTP send/verify workflows, Arabic and English messages, and an interface for custom gateways.
- **Testing:** Unit and feature test suites run with PHPUnit in GitHub Actions on pushes and pull requests.

### [CloudKit CLI](https://github.com/shabayekdes/cloudkit-cli) · Bash · AWS · Google Cloud

Shell helpers for AWS and Google Cloud, providing interactive session management, service wrappers, and a color-coded prompt across both cloud environments.

- **Sessions:** Profile and configuration pickers for AWS (SSO, static keys, `credential_process`, and chained role assumption) and gcloud, with the active account/project shown in the prompt and warnings before AWS credentials expire.
- **AWS:** EC2 access through SSM, including interactive sessions, port forwarding, and file uploads with checksum verification; ECS support for clusters, services, tasks, logs, and container exec.
- **Google Cloud:** GCE instance listing, SSH and SCP, plus rolling restart and replacement for managed instance groups.
- **Quality:** ShellCheck and credential-free smoke tests run in GitHub Actions on pushes and pull requests.

## Currently exploring

- **Go and concurrency:** Goroutines, channels, and patterns for bounded, cancellable work
- **Distributed systems:** Consistency, messaging, idempotency, and partial failure
- **System design:** High availability and horizontal scalability
- **Cloud infrastructure and reliability:** Observability, tracing, metrics, and resilience patterns

## Engineering principles

- **Maintainability over cleverness.** Prefer the simplest design that meets today's needs and leaves room for tomorrow's.
- **Make trade-offs explicit.** Document why a decision was made and what it costs.
- **Reliability, security, and performance are features.** Design for failure, least privilege, and measured performance from the start.
- **Code should be testable and readable.** If it's hard to test, the design may need work.
- **Build systems teams can operate.** Use good defaults, clear logs, and predictable deployments.

## GitHub activity

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=shabayekdes&show_icons=true&include_all_commits=true&rank_icon=github&theme=tokyonight&hide_border=true" alt="GitHub statistics for shabayekdes">
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=shabayekdes&layout=compact&exclude_repo=alx-backend,alx-backend-javascript,alx-backend-python,alx-backend-storage,alx-backend-user-data,alx-files_manager,alx-higher_level_programming,alx-interview,alx-low_level_programming,alx-system_engineering-devops,alx-pre_course,alx-zero_day,zero_day,printf,simple_shell,binary_trees,sorting_algorithms,AirBnB_clone,AirBnB_clone_v2,AirBnB_clone_v3,AirBnB_clone_v4,Fix_My_Code_Challenge,what-happens-when,leetcode-problems&theme=tokyonight&hide_border=true" alt="Most used languages in shabayekdes's public repositories, excluding selected coursework">
  <br>
  <img src="https://streak-stats.demolab.com/?user=shabayekdes&theme=tokyonight&hide_border=true" alt="GitHub contribution streak for shabayekdes">
</div>

<sub>Statistics are generated by third-party services and may occasionally be unavailable. Language breakdown reflects code in public repositories, with selected coursework excluded; it is not a measure of proficiency.</sub>

## Contact

The best way to reach me is through [LinkedIn](https://linkedin.com/in/shabayekdes). You can also explore my work on [GitHub](https://github.com/shabayekdes).
