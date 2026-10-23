# Uconnect: student-only social platform

**Status:** Staging / active development  
**Stack:** FastAPI, PostgreSQL, Redis, Alembic, Docker, React Native, Expo, TypeScript

## Product idea

Uconnect is a student-focused social platform connecting verified university users through profiles, feeds, messaging and communities, with additional features under development.

## My engineering work

The architecture uses FastAPI services, PostgreSQL for relational records, Redis for supporting workloads and a React Native / Expo mobile client. Work includes authentication, authorisation, student verification, schema migrations, API contracts, testing and staging deployment.

A recorded mobile verification run completed **94 tests across 19 suites**. Additional API, database and integration tests have been used during development.

## Engineering concerns

- Student verification and identity boundaries
- Role-based authorisation and secure API contracts
- Data consistency and schema changes
- Repeatable Docker-backed development and staging checks
- Application behaviour on Android and web clients

This repository is a high-level public case study; the application source and staging data are not included here.
