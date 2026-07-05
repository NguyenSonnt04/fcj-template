---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Set up the development environment with Docker Compose and build the PostgreSQL database.
* Build a layered backend framework and deploy the Repository Harness system.
* Design a soft delete mechanism, user role model, and get familiar with team development workflow.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | Set up environment with Docker Compose: simultaneously launch PostgreSQL, Redis, LocalStack, and pgAdmin; verify container status and confirm database connectivity via pgAdmin | 06/29/2026 | 06/29/2026 | |
| 3 | Design the PostgreSQL database via migration 001_init_schema.sql; build core data tables; enable pgcrypto and PostGIS extensions; set up automatic migrations and schema_migrations table | 06/30/2026 | 06/30/2026 | |
| 4 | Build a layered backend framework with Express and Native ESModules; organize source code into config, routes, controllers, services, models, and middlewares; establish snake_case/camelCase conventions | 07/01/2026 | 07/01/2026 | |
| 5 | Study and implement the Repository Harness system; install Harness CLI on Windows and initialize a local Harness database; execute test matrix queries and complete story TB-HARNESS with implemented status | 07/02/2026 | 07/02/2026 | |
| 6 | Study soft delete mechanism for the restaurants table; design roles, user_roles, and rank_definitions tables; learn the feature intake workflow, coding conventions, and story packet structure | 07/03/2026 | 07/03/2026 | |

### Week 10 Achievements:

* Set up the project development environment; installed and configured Docker Compose to simultaneously run PostgreSQL, Redis, LocalStack, and pgAdmin; verified all container statuses and confirmed database connectivity via pgAdmin.
* Designed the initial PostgreSQL database through migration 001_init_schema.sql; built core data tables; enabled pgcrypto and PostGIS extensions; set up automatic migrations with schema_migrations table for version management.
* Built a layered backend framework with Express and Native ESModules; organized source code into config, routes, controllers, services, models, and middlewares; established unified conventions using snake_case for requests and camelCase for responses.
* Studied and implemented the Repository Harness system; installed Harness CLI on Windows and initialized a local Harness database; executed test matrix queries and completed story TB-HARNESS with implemented status.
* Studied the soft delete mechanism for the restaurants table; executed migration to add is_deleted and deleted_at fields.
* Learned the user role and permission management model; researched the design of roles, user_roles, and rank_definitions tables.
* Studied the team's task management workflow and coding conventions; learned the feature intake process and story packet structure.
