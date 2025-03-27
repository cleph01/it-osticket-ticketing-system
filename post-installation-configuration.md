<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

---

# Post-Installation System Configuration

This section delves into the core configuration of the osTicket help desk system, focusing on customizing its key operational features. 

It details the setup of ticket categorization through topics, departments, and priorities, enabling efficient routing and management of support requests. 

This section outlines user management, including the creation of agents and end-users, and the assignment of roles and permissions. 

These system configuration aspects enable the deployed osTicket instance to meet specific organizational support and help desk needs.

---

## System Configuration Steps

This section outlines the configuration of key elements within the osTicket Admin Panel to tailor the help desk system to operational needs.

---

### Acknowledge Agent Panel vs Admin Panel

-   **Overview:** osTicket distinguishes between the Agent Panel, used by support staff to manage tickets and interact with users, and the Admin Panel, used by administrators to configure system-wide settings, agents, users, and other core components. Understanding this separation is crucial for navigating and managing the system effectively.

---

### Configure Roles (for grouping permissions)

-   **Navigation:** Admin Panel -> Agents -> Roles
-   **Overview:** Roles define a set of permissions that can be assigned to agents. This allows for granular control over what actions different agents or groups of agents can perform within the system. Creating roles simplifies permission management by grouping related permissions together.
-   **Example:**
    -   **Supreme Admin:** This role would typically encompass all available permissions, granting full control over the osTicket system.

---

### Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)

-   **Navigation:** Admin Panel -> Agents -> Departments
-   **Overview:** Departments logically group agents based on their area of expertise or responsibility. Departments also control ticket visibility, allowing you to restrict access to tickets based on an agent's department. This ensures that agents only see and work on tickets relevant to their skills.
-   **Example:**
    -   **SysAdmins:** Agents in this department would likely handle tickets related to server issues, network infrastructure, and other system-level problems.

---

### Configure Teams

-   **Navigation:** Admin Panel -> Agents -> Teams
-   **Overview:** Teams allow you to group agents from different departments together for collaborative ticket handling. This is useful for situations where multiple agents with diverse skills need to work on the same ticket. Teams can also be used for load balancing and ensuring ticket coverage.
-   **Example:**
    -   **Online Banking:** This team might include agents from the general support department and the systems administration department to handle complex issues related to the online banking platform.

---

### Allow anyone to create tickets

-   **Navigation:** Admin Panel -> Settings -> User Settings
-   **Overview:** These settings control who is allowed to submit support tickets to the system.
-   **Configuration:**
    -   **UNCHECK: unregistered users can create tickets:** By unchecking this option, you are requiring users to have an account (either registered or created by an agent) before they can submit a ticket.
    -   **Registration Required: Require registration and login to create tickets:** Enabling this option forces all users to register and log in to the system before they can create a new support ticket. This can help with tracking and managing user requests.

---

### Configure Agents (workers)

-   **Navigation:** Admin Panel -> Agents -> Add New
-   **Overview:** Agents are the support staff who will be managing and resolving support tickets. This section involves creating agent accounts and assigning them to specific departments.
-   **Examples:**
    -   **Jane (Dept: SysAdmins):** Jane is created as an agent and assigned to the SysAdmins department, indicating her primary area of responsibility.
    -   **John (Dept: Support):** John is created as an agent and assigned to the Support department, likely handling more general user inquiries.

---

### Configure Users (customers)

-   **Navigation:** Agent Panel -> Users -> Add New
-   **Overview:** Users are the customers or end-users who will be submitting support tickets. While users can often register themselves (depending on the system settings), agents can also manually create user accounts.
-   **Examples:**
    -   **Karen:** A user account is created for Karen.
    -   **Ken:** A user account is created for Ken.

---

### Configure SLA (Service Level Agreements)

-   **Navigation:** Admin Panel -> Manage -> SLA
-   **Overview:** Service Level Agreements (SLAs) define the timeframes within which support tickets should be addressed and resolved based on their severity. SLAs help ensure timely responses and set expectations for both support agents and users. They often include grace periods and operating schedules.
-   **Examples:**
    -   **Sev-A (Grace Period: 1 hour, Schedule: 24/7):** Tickets with Severity A (highest priority) should receive an initial response within 1 hour and are subject to a 24/7 operational schedule.
    -   **Sev-B (Grace Period: 4 hours, Schedule: 24/7):** Severity B tickets require a response within 4 hours and also follow a 24/7 schedule.
    -   **Sev-C (Grace Period: 8 hours, Business Hours):** Severity C tickets have an 8-hour response grace period and are only actively managed during defined business hours.

---

### Configure Help Topics (For when users create a ticket)

-   **Navigation:** Admin Panel -> Manage -> Help Topics
-   **Overview:** Help Topics provide a categorized list of common issues or request types that users can select when submitting a new ticket. This helps in automatically routing tickets to the appropriate department or agent and provides valuable data for tracking common support issues.
-   **Examples:**
    -   **Business Critical Outage:** For urgent issues that severely impact business operations.
    -   **Personal Computer Issues:** For problems related to individual user workstations.
    -   **Equipment Request:** For users needing new hardware or software.
    -   **Password Reset:** A common request for regaining access to accounts.
    -   **Other:** A general category for issues that don't fit into the specific predefined topics.
