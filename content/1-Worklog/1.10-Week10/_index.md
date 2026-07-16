---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives

- Complete the TrustBite development environment and PostgreSQL database.
- Build the backend foundation and deploy Repository Harness.
- Study soft delete, role management, and the team's story-based workflow.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | **Docker Compose Environment**<br>- Configured Docker Compose for PostgreSQL, Redis, LocalStack, and pgAdmin.<br>- Ran npm run docker:up and checked the status and logs of all containers.<br>- Connected to PostgreSQL through pgAdmin and verified local service communication. | 06/29/2026 | 06/29/2026 | [Source](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Docs](https://github.com/NguyenSonnt04/docs_trustbite) |
| 3 | **Database Schema and Migrations**<br>- Built 001_init_schema.sql for core and supporting business tables.<br>- Enabled pgcrypto and PostGIS for UUID and geospatial data.<br>- Set up automatic migrations and schema_migrations for database version tracking. | 06/30/2026 | 06/30/2026 | [Source](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Docs](https://github.com/NguyenSonnt04/docs_trustbite) |
| 4 | **Layered Backend Foundation**<br>- Built the backend with Express and Native ES Modules.<br>- Organized source code into config, routes, controllers, services, models, and middlewares.<br>- Standardized snake_case requests and camelCase responses. | 07/01/2026 | 07/01/2026 | [Source](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Docs](https://github.com/NguyenSonnt04/docs_trustbite) |
| 5 | **Repository Harness**<br>- Read Repository Harness and work classification documentation.<br>- Installed Harness CLI on Windows and initialized the local Harness database.<br>- Executed test matrix queries and completed story TB-HARNESS as implemented. | 07/02/2026 | 07/02/2026 | [Source](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Docs](https://github.com/NguyenSonnt04/docs_trustbite) |
| 6 | **Soft Delete, Roles, and Story Workflow**<br>- Created a decision record for restaurant soft delete and added is_deleted and deleted_at to restaurants.<br>- Studied roles, user_roles, rank_definitions, and account lifecycle states.<br>- Reviewed feature intake, coding conventions, domain rules, and story packet structure through a sample story. | 07/03/2026 | 07/03/2026 | [Source](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Docs](https://github.com/NguyenSonnt04/docs_trustbite) |

### Week 10 Results

- Completed the local PostgreSQL, Redis, LocalStack, and pgAdmin environment.
- Built database migrations, the backend skeleton, and Repository Harness.
- Implemented the initial soft-delete design and learned the role model and story-based workflow.
