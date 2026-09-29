# Technology Stack

| Layer | Technology |
|---|---|
| Frontend | Blazor WebAssembly |
| Language | C# |
| Scheduling UI | FullCalendar |
| Backend | ASP.NET Core Web API |
| Framework | .NET 6 |
| Data Access | Dapper |
| Database | Microsoft SQL Server |
| Authentication | JWT |
| Authorisation | RBAC |
| API Protection | Middleware / API key controls |
| Location | Google Maps / location services |
| Notifications | Twilio SMS |
| Bot Protection | Google reCAPTCHA |
| Web Server | NGINX |
| OS | Ubuntu / Linux |
| Security | HTTPS / TLS |
| Source Control | GitHub |

## Engineering Approach

The platform separates:

1. Presentation
2. API and business workflows
3. Authentication and authorisation
4. Data access
5. External integrations
6. Infrastructure

This separation helps keep business rules maintainable and allows external integrations to evolve independently.
