<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Ticket Lifecycle: Intake Through Resolution

This project demonstrates the full lifecycle of a support ticket in osTicket, from the moment a user submits it to the moment it is closed. It is Part 3 of a three-part series and uses the help desk built in Parts 1 and 2.

## Portfolio Project

**Author:** Anthony Maleke

**Contact:** [Linkedin](https://www.linkedin.com/in/anthonymaleke/)

## Video Demonstration

- [YouTube: osTicket Tutorial (Part 3 of 3) - Ticket Lifecycle](https://youtu.be/zBpV7ElqMwc)

## The Series

| Part | Repository | Topic |
|---|---|---|
| 1 | [osticket-prereqs](https://github.com/anthonymaleke/osticket-prereqs) | Azure VM, IIS, PHP, database, osTicket installation |
| 2 | [post-install-config](https://github.com/anthonymaleke/osticket-post-install) | Roles, departments, teams, agents, users, SLAs, help topics |
| 3 | **ticket-lifecycle** (this repo) | A ticket from intake to resolution |

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- osTicket User Portal and Agent Panel

## Operating Systems Used

- Windows Server 2022 Datacenter (Azure Edition)

## Lifecycle Stages

| Stage | Description |
|---|---|
| Intake | A user submits a ticket through the portal, or an agent logs one for a caller |
| Triage | The help topic sets department, priority, SLA and team automatically |
| Assignment | An agent claims the ticket or it is assigned to one |
| Work | The agent investigates, updates the user and records internal notes |
| Escalation | If needed, the ticket moves to a higher tier or another department |
| Resolution | The fix is delivered and the status becomes Resolved |
| Closure | The ticket is closed after the user confirms |

## Scenarios Demonstrated

### Scenario 1: Critical outage

A user reports that the customer portal is unavailable for all staff. The Service Outage help topic routes the ticket to Systems Administration with Emergency priority and the P1 Critical SLA (2 hours, 24/7), and assigns it to the Tier 2 team. The agent works the issue using internal notes and customer replies, resolves it, and closes it.

### Scenario 2: Routine request

A user asks for a PDF editor. The ticket stays with Tier 1 under the P3 Normal SLA (24 hours, business hours). The scenario also shows that a Tier 1 agent has no delete option, which proves the role configuration from Part 2.

### Scenario 3: Agent-created ticket and escalation

An agent logs a VPN problem reported by phone, tries basic troubleshooting, then transfers the ticket to Systems Administration for deeper investigation. The Tier 2 agent resolves it.

### Scenario 4: SLA due dates and overdue tickets

A password reset ticket receives the P2 High SLA and a due date. The due date is moved into the past to show how an overdue ticket appears in the Overdue queue.

## SLA Reference

| Plan | Grace period | Schedule | Typical use |
|---|---|---|---|
| P1 Critical | 2 hours | 24/7 | Outages |
| P2 High | 8 hours | Business hours | A user blocked from working |
| P3 Normal | 24 hours | Business hours | Standard requests and faults |
| P4 Low | 72 hours | Business hours | Non-urgent requests |

## Overview

1. Set up two browser sessions: one as an end user, one as an agent.
2. Run the critical outage scenario from intake to closure.
3. Run the routine request scenario and demonstrate role restrictions.
4. Run the agent-created ticket scenario and escalate it between departments.
5. Show SLA due dates and the overdue queue.
6. Review the dashboard.

## Key Takeaways

- Help topics remove guesswork. The system applies the correct department, priority, SLA and assignee as soon as the ticket is created.
- Internal notes and public replies are separate, so agents can document work without exposing it to the user.
- Escalation keeps the full ticket history, so the next agent never has to ask the user to repeat themselves.
- SLAs make urgency measurable and visible, which is what lets a team prioritize correctly.
- Role-based access means front-line agents can do their job without having the power to delete records.

## Skills Demonstrated

- Cloud VM deployment and network security in Azure
- Windows Server and IIS administration
- PHP and database configuration
- Help desk design: roles, departments, teams, SLAs and routing
- Incident intake, triage, escalation and resolution
- Written communication with end users
- Documentation and technical video production

## Known Limitations

- Outgoing email is not configured, so notifications are shown in the portals rather than delivered to a mailbox.
- The lab runs over HTTP and uses fictional sample data only.

## References

- [osTicket Agent Panel](https://docs.osticket.com/en/latest/Agent%20Panel.html)
- [osTicket User Portal](https://docs.osticket.com/en/latest/User%20Portal.html)
- [osTicket Tutorials](https://www.youtube.com/c/osTicket_tutorials)
