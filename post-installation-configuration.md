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

#### Agent Panel
<p>
  <img width="983" alt="image" src="https://github.com/user-attachments/assets/b164a86c-bd76-4d0f-9d7f-efe0c426a348" />
</p>

#### Admin Panel
<p>
  <img width="971" alt="image" src="https://github.com/user-attachments/assets/365250d1-488f-494c-9b04-b7d3b3be28b2" />
</p>

---

### Configure Roles (for grouping permissions)

-   **Navigation:** Admin Panel -> Agents -> Roles
-   **Overview:** Roles define a set of permissions that can be assigned to agents. This allows for granular control over what actions different agents or groups of agents can perform within the system. Creating roles simplifies permission management by grouping related permissions together.
-   **Example:**
    -   **Supreme Admin:** This role would typically encompass all available permissions, granting full control over the osTicket system.
 
#### View Only Role - Has no permissioning for Tickets, Tasks, or Knowledgebase

<p>
  <img width="702" alt="image" src="https://github.com/user-attachments/assets/ff54d4f3-ff82-446d-a5f2-459814d4c268" />
</p>

#### Expanded Access Role - Many more permissions (but less than "All Access"/Administrator)

<p>
  <img width="673" alt="image" src="https://github.com/user-attachments/assets/01bf5867-7d30-408e-9004-dd5074d0125c" />
</p>

#### Custom Roles Can Also Be Created via "Add New Role" and Custom Permissions Attached

<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/414e9bc1-acbe-4c43-a9c2-cfcb81c93d6c" />
</p>

#### Create New Role -> "Supreme Admin"

<p>
  <img width="962" alt="image" src="https://github.com/user-attachments/assets/56546311-9bd4-4423-859a-05f6669bcade" />
</p>

#### Grant All Permissions for Tickets, Task, and Knowledgebase

<p>
  <img width="955" alt="image" src="https://github.com/user-attachments/assets/f9675af1-7426-4dbc-9a48-8e298d8aea5c" />
</p>

#### Save

<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/2bbc434c-de96-419f-add5-e22340dee93b" />
</p>

---

### Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)

-   **Navigation:** Admin Panel -> Agents -> Departments
-   **Overview:** Departments logically group agents based on their area of expertise or responsibility. Departments also control ticket visibility, allowing you to restrict access to tickets based on an agent's department. This ensures that agents only see and work on tickets relevant to their skills.
-   **Example:**
    -   **SysAdmins:** Agents in this department would likely handle tickets related to server issues, network infrastructure, and other system-level problems.

#### Add New Department

<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/c873b739-3dfa-4436-b0b8-797a93aa1ee2" />
</p>

#### Name is SysAdmins

<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/eb53400c-bf0f-43fb-9a0b-590d352aa3dc" />
</p>

#### Save

<p>
  <img width="967" alt="image" src="https://github.com/user-attachments/assets/4350d099-cc16-44b0-8bcb-411a9932af7b" />
</p>

---

### Configure Teams

-   **Navigation:** Admin Panel -> Agents -> Teams
-   **Overview:** Teams allow you to group agents from different departments together for collaborative ticket handling. This is useful for situations where multiple agents with diverse skills need to work on the same ticket. Teams can also be used for load balancing and ensuring ticket coverage.
-   **Example:**
    -   **Online Banking:** This team might include agents from the general support department and the systems administration department to handle complex issues related to the online banking platform.

#### Create a New Team

<p>
  <img width="958" alt="image" src="https://github.com/user-attachments/assets/e10b856d-72d1-499f-9c2f-a5c0e83bebde" />
</p>

#### Name It

<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/e7358aab-f876-46fc-8ca1-bf90231cad26" />
</p>

#### Save

<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/e6c68709-86d9-4c14-bbb7-1057372c9da4" />
</p>

---

### Allow anyone to create tickets

-   **Navigation:** Admin Panel -> Settings -> User Settings
-   **Overview:** These settings control who is allowed to submit support tickets to the system.
-   **Configuration:**
    -   **UNCHECK: unregistered users can create tickets:** By unchecking this option, you are requiring users to have an account (either registered or created by an agent) before they can submit a ticket.
    -   **Registration Required: Require registration and login to create tickets:** Enabling this option forces all users to register and log in to the system before they can create a new support ticket. This can help with tracking and managing user requests.
 
<p>
  <img width="959" alt="image" src="https://github.com/user-attachments/assets/1999b884-2cdd-45a1-adfa-56d66e49f97d" />
</p>

---

### Configure Agents (workers)

-   **Navigation:** Admin Panel -> Agents -> Add New
-   **Overview:** Agents are the support staff who will be managing and resolving support tickets. This section involves creating agent accounts and assigning them to specific departments.
-   **Examples:**
    -   **Jane (Dept: SysAdmins):** Jane is created as an agent and assigned to the SysAdmins department, indicating her primary area of responsibility.
    -   **John (Dept: Support):** John is created as an agent and assigned to the Support department, likely handling more general user inquiries.
 
#### Add New Agents

<p>
  <img width="955" alt="image" src="https://github.com/user-attachments/assets/8d81e333-3c13-4f0e-9b4f-d659a5ff3223" />
</p>

<p>
  <img width="951" alt="image" src="https://github.com/user-attachments/assets/7e8e1d97-fd05-493a-8334-11df7bbc450f" />
</p>

#### Make Jane Doe part of *"SysAdmins"* Department with a *"Supreme Admin"* Role on the *"Online Banking"* Team

<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/6265b8d0-f1a6-4531-9222-0d6a01587890" />
</p>

<p>
  <img width="959" alt="image" src="https://github.com/user-attachments/assets/39f9e105-8d7a-48d1-8d6a-6c535147415b" />
</p>

#### Make John Doe part of *"Support"* Department with a *"Read Only"* Role and not on a team

<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/f57871ec-a862-4d98-a60b-4f9e3ab9f52c" />
</p>

<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/fc5ca33e-15d3-4532-af33-d752f9469e7a" />
</p>

#### Save

<p>
  <img width="951" alt="image" src="https://github.com/user-attachments/assets/71526246-0e78-456a-879e-d811d1f23ebb" />
</p>

---

### Configure Users (customers)

-   **Navigation:** Agent Panel -> Users -> Add New
-   **Overview:** Users are the customers or end-users who will be submitting support tickets. While users can often register themselves (depending on the system settings), agents can also manually create user accounts.
-   **Examples:**
    -   **Karen:** A user account is created for Karen.
    -   **Ken:** A user account is created for Ken.

#### In the Agent Panel, Create Karen and Ken

<p>
  <img width="957" alt="image" src="https://github.com/user-attachments/assets/d75eccf9-4e56-452d-9697-a6c440328b6e" />
</p>

<p>
  <img width="957" alt="image" src="https://github.com/user-attachments/assets/034c97dd-eb38-49c3-90fe-de0bd5545923" />
</p>

---

### Configure SLA (Service Level Agreements)

-   **Navigation:** Admin Panel -> Manage -> SLA
-   **Overview:** Service Level Agreements (SLAs) define the timeframes within which support tickets should be addressed and resolved based on their severity. SLAs help ensure timely responses and set expectations for both support agents and users. They often include grace periods and operating schedules.
-   **Examples:**
    -   **Sev-A (Grace Period: 1 hour, Schedule: 24/7):** Tickets with Severity A (highest priority) should receive an initial response within 1 hour and are subject to a 24/7 operational schedule.
    -   **Sev-B (Grace Period: 4 hours, Schedule: 24/7):** Severity B tickets require a response within 4 hours and also follow a 24/7 schedule.
    -   **Sev-C (Grace Period: 8 hours, Business Hours):** Severity C tickets have an 8-hour response grace period and are only actively managed during defined business hours.

<p>
  <img width="957" alt="image" src="https://github.com/user-attachments/assets/e5129d70-4cb8-49cf-ada1-a6676b50ce70" />
</p>

<p>
  <img width="958" alt="image" src="https://github.com/user-attachments/assets/19a5f229-6fa6-42ed-9f25-f3b3f141e7ac" />
</p>

<p>
  <img width="949" alt="image" src="https://github.com/user-attachments/assets/ab35f555-432f-4872-b599-be194b12d6bc" />
</p>

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

<p>
  <img width="959" alt="image" src="https://github.com/user-attachments/assets/1cdcd53b-4489-40c3-8cf8-b97467adbd82" />
</p>
<p>
  <img width="948" alt="image" src="https://github.com/user-attachments/assets/ce3238f9-95b4-430d-a43f-0aad3c2f5ef1" />
</p>
<p>
  <img width="952" alt="image" src="https://github.com/user-attachments/assets/43d4c6d4-8283-4b46-bc59-e2f3ee363e9d" />
</p>



