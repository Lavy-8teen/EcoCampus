# EcoCampus AI — System Architecture

## 1. Overview

EcoCampus AI is planned as a web application for campus environmental awareness, cleanliness reporting, and institutional progress monitoring.

The initial version will support one institution. The architecture should allow multiple institutions to use the platform independently in the future.

## 2. Proposed Architecture

### Frontend
- React
- TypeScript
- Responsive design for desktop and mobile
- Accessible interface for students, staff, and administrators

### Backend and Database
Evaluate Supabase as the initial backend option.
- PostgreSQL database
- Authentication
- Role-based access
- File storage for report evidence
- Row-level security to isolate institution data

### Mapping
- Leaflet for interactive maps
- OpenStreetMap as a potential map-data source
- Manual campus-location configuration when map data is incomplete

### Analytics
- Dashboard charts for reports, resolution times, participation, and cleanliness trends
- Metrics calculated from stored records rather than fabricated demo values

### AI Services
Potential AI-assisted capabilities:
- Institution setup guidance
- Waste-disposal assistance
- Campus issue summaries
- Candidate bin-location recommendations

AI features will be introduced only when their data requirements, costs, and reliability are understood.

## 3. Main Application Modules

1. Institution onboarding
2. Campus map and facilities
3. Waste-disposal guidance
4. Cleanliness reporting
5. Maintenance assignment and resolution
6. Student awareness and eco-missions
7. Rewards and participation records
8. Administrative analytics
9. AI-assisted recommendations

## 4. Initial Data Entities

- Institutions
- User profiles and memberships
- Campus buildings and zones
- Waste bins and disposal facilities
- Waste categories and guidance
- Cleanliness reports
- Report status history
- Maintenance assignments
- Resolution evidence
- Environmental campaigns
- Eco-missions and participation
- Reward ledger
- AI recommendations
- Audit logs

## 5. Security Requirements

- Authenticate users where necessary.
- Enforce permissions on the backend, not only in the user interface.
- Isolate data belonging to different institutions.
- Protect uploaded files.
- Keep API keys and secrets out of frontend code and GitHub.
- Collect only the personal data needed for the service.
- Maintain appropriate records of important administrative actions.

## 6. Reliability

- Provide useful error and loading states.
- Validate user inputs.
- Handle duplicate and unverified reports.
- Keep the reporting workflow usable when AI services are unavailable.
- Label simulated demonstration data clearly.

## 7. Architecture Decisions Pending

The following require validation before implementation:
- Final backend and database choice
- Authentication and institutional membership model
- Map import and editing approach
- AI provider and budget
- Image storage and retention
- Hosting and deployment
- Multi-institution access policies

## 8. Guiding Principle

Build the smallest reliable end-to-end workflow first, then expand the platform without compromising privacy, safety, or data integrity.
