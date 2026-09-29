# Help Desk Ticketing Lab — osTicket

A Docker-based osTicket lab covering ticket creation, assignment, response, resolution, and administrator-access recovery.

## Objectives

- Deploy osTicket helpdesk system using Docker
- Practice container troubleshooting on Apple Silicon (ARM64)
- Simulate user support ticket workflow
- Recover admin account via database password reset
- Demonstrate ticket lifecycle:
  - Ticket creation
  - Assignment
  - Response
  - Resolution
## Technologies Used

- Docker / Docker Compose
- osTicket Helpdesk System
- MariaDB Database
- macOS (Apple Silicon M1 environment)
- SQL administration commands
## Deployment Overview

1. Installed Docker Desktop on macOS
2. Created project directory:
   osticket-lab/
3. Configured docker-compose.yml with osTicket image
4. Deployed containers:
   docker compose up -d
5. Accessed web interface via:
   http://localhost:8080
## Incident Simulation

Problem:
Admin login access failed after deployment.

Root Cause:
Password hash mismatch in database.

Resolution Actions:
- Reset bcrypt password hash directly in MariaDB
- Cleared session locks
- Restarted container
- Verified admin access restored
## Ticket Lifecycle Demonstrated

- User created support ticket ("Unable to login")
- Admin assigned ticket
- Admin responded to user
- Ticket marked resolved
## Skills Demonstrated

- Helpdesk ticketing systems (osTicket)
- Docker container deployment & troubleshooting
- SQL database administration
- Authentication troubleshooting
- Incident documentation
- IT support workflow simulation
## Future Improvements

- Email integration for ticket notifications
- SIEM log forwarding
- Role-based access control testing
- Security hardening of containers
