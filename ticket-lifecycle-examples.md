<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<hr />

# Ticket Lifecycle Examples (Working Tickets)

This lab focuses on simulating real-world ticket interactions from both the end-user and help desk agent perspectives.

It walks through the complete lifecycle of several mock tickets, demonstrating key interactions such as ticket creation by end-users, routing and assignment to agents, agent responses and internal notes, status updates, and eventual ticket closure.

---

## Ticket Scenario 1: Critical System Outage

-   **End-User Action (from the End-User portal):**

    -   **Create a ticket under username "Karen" with the subject:** "entire mobile/online banking system is down"

 #### This simulates a high-priority issue reported by an end-user, indicating a critical service disruption, *but using an less-severe category/label*
 
<p>
  <img width="713" alt="image" src="https://github.com/user-attachments/assets/a2d738ea-574f-4ed8-a6d2-e1e945332d70" />
</p>
<p>
  <img width="805" alt="image" src="https://github.com/user-attachments/assets/acb2ac3c-7402-4ab5-bbf4-5c69f19b3869" />
</p>
<p>
  <img width="837" alt="image" src="https://github.com/user-attachments/assets/faf291f3-d51e-4d0c-88ca-d11878b5ccab" />
</p>
        
#### Help Desk Agent (John) Actions (from the Agent portal):

<p>
  <img width="962" alt="image" src="https://github.com/user-attachments/assets/329477c1-1d9a-4718-aaab-67ed9bdaac6b" />
</p>
  
#### Observe the ticket's properties:

<p>
  <img width="963" alt="image" src="https://github.com/user-attachments/assets/dd0ab041-588e-4602-951e-23de3f2b40b3" />
</p>

-   **Priority:** Observe the default or user-selected priority.
-   **Department:** Note the department the ticket was initially routed to.
-   **SLA:** Verify the applied Service Level Agreement.
-   **Assigned To:** Check if the ticket is automatically assigned.
-   **Overview:** This step emphasizes the agent's initial assessment of a new ticket, understanding its key attributes for effective handling.
        
#### Set Properties to the ticket:
  
- **Sev-A (1 hour, 24/7):** Manually set the Severity to A, indicating the highest priority, with a 1-hour resolution SLA and 24/7 support.
    
<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/69819de7-17bf-4ee6-928b-abf8020f4e5d" />
</p>

- **Online Banking Department:** Assign the ticket to the appropriate department.

<p>
  <img width="972" alt="image" src="https://github.com/user-attachments/assets/3504fd0f-aeb5-4728-b6eb-051e6c69a06f" />
</p>

<p>
  <img width="955" alt="image" src="https://github.com/user-attachments/assets/2ea11231-c275-4ef2-a9e2-19d8542b42e3" />
</p>


- **Update Help Topic:** Update help topic to reflect severity

<p>
  <img width="953" alt="image" src="https://github.com/user-attachments/assets/29572432-33dd-4756-bd8a-bd3d96570e88" />
</p>

- **Overview:** This demonstrates how agents can adjust ticket properties to ensure proper prioritization and routing.

        
#### Work the ticket to completion as Jane:

- This simulates the ticket resolution process, including communication, troubleshooting, and final closure. It also shows how a ticket might be handled by a different agent than initially assigned.

<p>
  <img width="955" alt="image" src="https://github.com/user-attachments/assets/4ee2aadd-5cd2-4ba7-a78e-6756d69091e7" />
</p>

<p>
  <img width="941" alt="image" src="https://github.com/user-attachments/assets/cfbd7aa0-be2e-4983-8478-36e4237701de" />
</p>

<p>
  <img width="953" alt="image" src="https://github.com/user-attachments/assets/7a9a99b0-3ae9-48e7-902c-3b813a1fa9be" />
</p>

<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/c9b86c85-32f5-4064-8a56-baddd489c8b2" />
</p>

<p>
  <img width="945" alt="image" src="https://github.com/user-attachments/assets/7d9af2f9-750f-4bea-bd0a-99f14a78c41b" />
</p>

<p>
  <img width="964" alt="image" src="https://github.com/user-attachments/assets/bfea7ba9-6156-4790-91fb-2161328d2d4d" />
</p>

---

## Ticket Scenario 2: Software Upgrade Request

-   **End-User Action:**
  
    -   **Create a ticket with the subject:** "accounting department needs adobe upgrade, broken"
        -   **Overview:** This represents a more routine request for software assistance from a specific department.
          
-   **Help Desk Agent (John) Actions:**
  
    -   **Observe the ticket's properties:**
        -   **Priority:** Observe the default or user-selected priority.
        -   **Department:** Note the department the ticket was initially routed to.
        -   **SLA:** Verify the applied Service Level Agreement.
        -   **Assigned To:** Check if the ticket is automatically assigned.
        -   **Overview:** Similar to the previous scenario, this step highlights the agent's initial assessment.
          
    -   **Set Properties to the ticket:**
        -   **Sev-B (4 hours, 24/7):** Set the Severity to B, with a 4-hour resolution SLA and 24/7 support.
        -   **Support:** Assign the ticket to the general Support department.
        -   **Overview:** Adjusting ticket properties according to the request's urgency and nature.
          
    -   **Work the ticket to completion as John:**
        -   **Overview:** Resolving the ticket, including any necessary communication, steps taken, and final closure.

<hr />

## Ticket Scenario 3: Hardware Issue

-   **End-User Action:**
  
    -   **Create a ticket with the subject:** "CFO's laptop will no longer turn on"
        -   **Overview:** This scenario represents a hardware-related issue affecting a high-profile user (CFO).
          
-   **Help Desk Agent (John) Actions:**
  
    -   **Observe the ticket's properties:**
        -   **Priority:** Observe the default or user-selected priority.
        -   **Department:** Note the department the ticket was initially routed to.
        -   **SLA:** Verify the applied Service Level Agreement.
        -   **Assigned To:** Check if the ticket is automatically assigned.
        -   **Overview:** Initial ticket assessment by the agent.
          
    -   **Set Properties to the ticket:**
        -   **Sev-B (4 hours, 24/7):** Set the Severity to B, with a 4-hour resolution SLA and 24/7 support.
        -   **Support:** Assign the ticket to the general Support department.
        -   **Overview:** Adjusting ticket properties to reflect the issue's severity and appropriate handling.
          
    -   **Work the ticket to completion as John:**
        -   **Overview:** Resolving the hardware issue, including troubleshooting steps and communication with the user.

---

## Ticket Escalation and Access Control

-   **Scenario:**
  
    -   **Set Properties to all the tickets; do SEV-A (SysAdmins last), observe ticket becomes inaccessible.**
        -   **Overview:** This demonstrates how changing ticket properties, specifically department assignments, can impact agent access due to department-based permissions.
          
    -   **Switch to admin panel and assign yourself View-access to Sys Admins.**
        -   **Overview:** This shows how an administrator can modify agent permissions to grant access to specific departments.
          
    -   **Switch to agent panel and observe the escalated ticket.**
        -   **Overview:** Verifying that the permission change in the admin panel is reflected in the agent panel, allowing the agent to now view the escalated ticket.
          
    -   **Observe that you can no longer make changes to it.**
         -   **Overview:** This highlights the difference between viewing a ticket and having the ability to modify it, even after gaining department access.


<br />
