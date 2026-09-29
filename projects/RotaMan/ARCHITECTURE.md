# Architecture

## High-Level Design

```text
Users
  |
  v
Blazor WebAssembly
  |
  v
ASP.NET Core Web API
  |
  +--> Authentication / Authorisation
  |
  +--> Business Workflows
  |
  +--> Dapper Data Access
  |       |
  |       v
  |     SQL Server
  |
  +--> Location / Maps Services
  |
  +--> Twilio SMS
  |
  +--> reCAPTCHA
  |
  v
NGINX / HTTPS
```

## Frontend

Blazor WebAssembly provides the browser-based application experience and scheduling interface.

## API

ASP.NET Core Web API provides the service boundary for:

- Authentication
- Authorisation
- Workforce operations
- Rota workflows
- Leave
- Shift changes
- Attendance
- Notifications
- Location-aware rules

## Data Access

Dapper provides lightweight data access between the API and Microsoft SQL Server.

## Security Boundary

Authentication and authorisation are applied before protected business operations are performed.

## External Integrations

External services are kept behind integration boundaries so the core application can evolve independently.

## Infrastructure

The application can be hosted on Linux/Ubuntu with NGINX providing reverse-proxy and HTTPS termination responsibilities.

## Architectural Direction

The design supports future additions such as analytics, mobile clients, integrations and AI-assisted workforce planning without requiring the core workflow to be replaced.
