# Security

## Authentication

RotaMan uses JWT-based authentication for protected application workflows.

## Authorisation

Role-based access control separates responsibilities between:

- Admin
- Schedule Manager
- Caregiver

The intention is to prevent users from receiving operational capabilities unrelated to their responsibilities.

## Granular Access

Authorisation should be treated as more than a simple authenticated/not-authenticated decision.

Business actions can depend on:

- User identity
- Assigned role
- Operational responsibility
- Current workflow
- Location conditions where applicable

## Location-Aware Controls

Location validation can be used to verify whether an attendance operation occurs within a permitted operational area.

The portfolio design does not represent continuous employee tracking.

## API Protection

Protected API operations are subject to authentication, authorisation and middleware-level controls.

## Transport Security

HTTPS/TLS should be used for production traffic.

## Production Security Checklist

Before production deployment:

- Store secrets outside source control.
- Use managed secret storage where appropriate.
- Enforce HTTPS.
- Review API permissions.
- Enable appropriate logging and monitoring.
- Protect administrative accounts.
- Review access periodically.
- Apply operating-system and dependency updates.
- Configure secure backups.
- Define data retention requirements.
- Minimise collection of personal data.
- Complete applicable privacy and regulatory reviews.

## Portfolio Repository Policy

This repository must never contain:

- Passwords
- API keys
- JWT secrets
- Certificates/private keys
- Database backups
- Production configuration
- Patient information
- Employee personal data
- Private infrastructure information
