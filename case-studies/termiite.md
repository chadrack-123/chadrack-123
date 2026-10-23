# Termiite: secure private-access and proposal automation

**Role:** Full-stack implementation and cloud deployment  
**Stack:** React, Vercel, Cloudflare Workers, Cloudflare D1, Turnstile, email templates  
**Public website:** https://termiite.co.za/

## Problem

The business needed a controlled way for authorised visitors to access private content and submit proposal requests. The system also needed automated notifications and low ongoing infrastructure costs.

## Approach

I developed the React frontend and a small backend API for authentication and proposal submission. The deployed design uses Cloudflare Workers with a D1 database. Security controls include session cookies, input-size limits, Origin validation, Turnstile verification and rate limits.

GitHub Copilot supported implementation and test development. I reviewed suggestions and validated the final behaviour rather than treating generated code as automatically correct.

## What went wrong

The initial backend design relied on Firebase Functions. To meet the project's free-tier constraints, I migrated the API to Cloudflare Workers and D1. During deployment, the Worker could not access D1 because the database binding was not configured correctly.

I investigated the deployment output and configuration, corrected the binding and redeployed. I then ran the Worker tests and checked the authentication and proposal request flows. The Worker suite passed **27 tests** in the recorded verification run.

## Lessons learned

- Deployment configuration is part of the application, not an afterthought.
- AI suggestions accelerate development but still require careful review and testing.
- Clear logs, repeatable checks and explicit security constraints make small services more reliable.

> This case study intentionally omits private configuration values, secrets, user data and client-specific implementation details.
