<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<hr />

# Ticket Lifecycle Examples (Working Tickets)

This section provides practical, real-world-like examples of how support tickets are managed within the configured osTicket system.

It walks through the complete lifecycle of several mock tickets, demonstrating key interactions such as ticket creation by end-users, routing and assignment to agents, agent responses and internal notes, status updates, and eventual ticket closure.

---

## Ticket Scenario 1: Critical System Outage

-   **End-User Action (from the End-User portal):**
    -   **Create a ticket under username "Karen" with the subject:** "entire mobile/online banking system is down"
        -   **Description:** This simulates a high-priority issue reported by an end-user, indicating a critical service disruption, albeit initially categorized under a less severe label to demonstrate triage.

<p>
  <img width="713" alt="image" src="https://github.com/user-attachments/assets/a2d738ea-574f-4ed8-a6d2-e1e945332d70" />
</p>
<br />
<p>
  <img width="805" alt="image" src="https://github.com/user-attachments/assets/acb2ac3c-7402-4ab5-bbf4-5c69f19b3869" />
</p>
<br />
<p>
  <img width="837" alt="image" src="https://github.com/user-attachments/assets/faf291f3-d51e-4d0c-88ca-d11878b5ccab" />
</p>
<br />
<hr />

#### Help Desk Agent (John) Actions (from the Agent portal):

<p>
  <img width="962" alt="image" src="https://github.com/user-attachments/assets/329477c1-1d9a-4718-aaab-67ed9bdaac6b" />
</p>
<br />

#### Observe the ticket's properties:

<p>
  <img width="963" alt="image" src="https://github.com/user-attachments/assets/dd0ab041-588e-4602-951e-23de3f2b40b3" />
</p>
<br />

-   **Priority:** Observe the default or user-selected priority.
-   **Department:** Note the department the ticket was initially routed to.
-   **SLA:** Verify the applied Service Level Agreement.
-   **Assigned To:** Check if the ticket is automatically assigned.
-   **Overview:** This step emphasizes the agent's initial assessment of a new ticket, understanding its key attributes for effective handling.

<hr />

#### Set Properties to the ticket:

-   **Sev-A (1 hour, 24/7):** Manually set the Severity to A, indicating the highest priority, with a 1-hour resolution SLA and 24/7 support.

<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/69819de7-17bf-4ee6-928b-abf8020f4e5d" />
</p>
<br />

-   **Online Banking Department:** Assign the ticket to the appropriate department.

<p>
  <img width="972" alt="image" src="https://github.com/user-attachments/assets/3504fd0f-aeb5-4728-b6eb-051e6c69a06f" />
</p>
<br />
<p>
  <img width="955" alt="image" src="https://github.com/user-attachments/assets/2ea11231-c275-4ef2-a9e2-19d8542b42e3" />
</p>
<br />

-   **Update Help Topic:** Update help topic to reflect severity.

<p>
  <img width="953" alt="image" src="https://github.com/user-attachments/assets/29572432-33dd-4756-bd8a-bd3d96570e88" />
</p>
<br />

-   **Overview:** This demonstrates how agents can adjust ticket properties to ensure proper prioritization and routing based on the actual issue.

<hr />

#### Work the ticket to completion as Jane:

-   **Description:** This simulates the ticket resolution process, including communication, troubleshooting, and final closure. It also shows how a ticket might be handled by a different agent than initially assigned, reflecting real-world collaboration or escalation.

<p>
  <img width="955" alt="image" src="https://github.com/user-attachments/assets/4ee2aadd-5cd2-4ba7-a78e-6756d69091e7" />
</p>
<br />
<p>
  <img width="941" alt="image" src="https://github.com/user-attachments/assets/cfbd7aa0-be2e-4983-8478-36e4237701de" />
</p>
<br />
<p>
  <img width="953" alt="image" src="https://github.com/user-attachments/assets/7a9a99b0-3ae9-48e7-902c-3b813a1fa9be" />
</p>
<br />
<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/c9b86c85-32f5-4064-8a56-baddd489c8b2" />
</p>
<br />
<p>
  <img width="945" alt="image" src="https://github.com/user-attachments/assets/7d9af2f9-750f-4bea-bd0a-99f14a78c41b" />
</p>
<br />
<p>
  <img width="964" alt="image" src="https://github.com/user-attachments/assets/bfea7ba9-6156-4790-91fb-2161328d2d4d" />
</p>
<br />
<hr />

## Ticket Scenario 2: Software Upgrade Request

-   **End-User Action (from the End-User portal):**
    -   **Create a ticket under username "Ken" with the subject:** "accounting department needs adobe upgrade, broken"
        -   **Description:** This represents a more routine request for software assistance from a specific department. It also demonstrates how a user might request a particular type of assistance but describe a situation that may not directly correlate, requiring deeper investigation by the agent.

<p>
  <img width="831" alt="image" src="https://github.com/user-attachments/assets/5344aad1-35cd-4ab9-b6c3-59465c46820e" />
</p>
<br />
<p>
  <img width="832" alt="image" src="https://github.com/user-attachments/assets/44302d6a-b590-4054-8420-3ba59a52784e" />
</p>
<br />
<hr />

#### Help Desk Agent (John) Actions (from the Agent portal):

<p>
  <img width="957" alt="image" src="https://github.com/user-attachments/assets/68c07035-c621-4f8f-8d00-4f27565a421a" />
</p>
<br />

-   **Observe the ticket's properties:**
    -   **Priority:** Observe the default or user-selected priority.
    -   **Department:** Note the department the ticket was initially routed to.
    -   **SLA:** Verify the applied Service Level Agreement.
    -   **Assigned To:** Check if the ticket is automatically assigned.
    -   **Overview:** Similar to the previous scenario, this step highlights the agent's initial assessment of a new ticket.

<p>
  <img width="954" alt="image" src="https://github.com/user-attachments/assets/21a1f854-9089-46ca-9eb3-ac389857a226" />
</p>
<br />

-   **Assign to myself (John):**
    -   **Description:** This demonstrates how an agent can take ownership of a ticket to manage its resolution.

<p>
<img width="955" alt="image" src="https://github.com/user-attachments/assets/22e0cba3-1199-48ae-9c63-c527f4af4169" />
</p>
<br />
<hr />

-   **Set Properties to the ticket:**
    -   **Sev-C (8 hours, Business Hours):** Set the Severity to C, with an 8-hour resolution SLA and Business Hours support, reflecting a less urgent, standard request.

<p>
  <img width="958" alt="image" src="https://github.com/user-attachments/assets/ac454b47-d4cf-456a-8b91-daa49bcf9a68" />
</p>
<br />

-   **Support:** Verify/Assign the ticket to the general Support department.
    -   **Note:** It is already assigned to this department based on the Help Topic.

<p>
  <img width="958" alt="image" src="https://github.com/user-attachments/assets/38a69187-ff7d-4dc4-a166-cbed07384532" />
</p>
<br />
<hr />

-   **Work the ticket to completion as John:**
    -   **Overview:** Resolving the ticket, including any necessary communication with the user regarding the upgrade, steps taken, and final closure.

<p>
  <img width="967" alt="image" src="https://github.com/user-attachments/assets/b72622d2-c888-4f6e-8107-77d1440cf03d" />
</p>
<br />
<p>
  <img width="954" alt="image" src="https://github.com/user-attachments/assets/75de2952-665b-45ed-b13f-f61f75be7a27" />
</p>
<br />
<p>
  <img width="961" alt="image" src="https://github.com/user-attachments/assets/a36ab99e-b58c-4a7b-ac14-89d5160f1d6e" />
</p>
<br />
<hr />

## Ticket Scenario 3: Hardware Issue

#### End-User Action (from the End-User portal):

-   **Create a ticket under username "Karen" with the subject:** "CFO's laptop will no longer turn on"

<p>
  <img width="839" alt="image" src="https://github.com/user-attachments/assets/358cb9be-9533-4e76-9ad3-6b73ddcbae0a" />
</p>
<br />
<p>
  <img width="954" alt="image" src="https://github.com/user-attachments/assets/f18d672e-b5d3-43ce-838a-ce25e2d63b81" />
</p>
<br />

-   **Overview:** This scenario represents a hardware-related issue affecting a high-profile user (CFO), potentially requiring expedited handling.

<hr />

-   **Help Desk Agent (John) Actions (from the Agent portal):**

<p>
  <img width="964" alt="image" src="https://github.com/user-attachments/assets/374214c6-9df2-43e9-b864-6673eef1382e" />
</p>
<br />

-   **Observe the ticket's properties:**
    -   **Priority:** Observe the default or user-selected priority.
    -   **Department:** Note the department the ticket was initially routed to.
    -   **SLA:** Verify the applied Service Level Agreement.
    -   **Assigned To:** Check if the ticket is automatically assigned.
    -   **Overview:** Initial ticket assessment by the agent to understand the scope and urgency of the issue.

<p>
  <img width="958" alt="image" src="https://github.com/user-attachments/assets/6ac46c33-44fe-412e-9756-cc375f015946" />
</p>
<br />
<hr />

-   **Set Properties to the ticket:**

-   **Priority:** Manually set the Priority to "Emergency" due to the user's importance.

<p>
  <img width="984" alt="image" src="https://github.com/user-attachments/assets/4754906c-ce29-404f-afe2-729e976c8114" />
</p>
<br />

-   **Sev-B (4 hours, 24/7):** Set the Severity to B, with a 4-hour resolution SLA and 24/7 support, reflecting the urgency despite the hardware nature.

<br />

-   **Support:** Verify/Assign the ticket to the general Support department.
    -   **Note:** It is already assigned to this department based on the Help Topic.

-   **Overview:** Adjusting ticket properties to reflect the issue's severity and the affected user, ensuring appropriate handling and prioritization.

<hr />

-   **Work the ticket to completion as John:**

<p>
  <img width="952" alt="image" src="https://github.com/user-attachments/assets/16a06bc2-6ed4-4dbf-91d6-bed07752bfc4" />
</p>
<br />
<p>
  <img width="953" alt="image" src="https://github.com/user-attachments/assets/91428f63-72c7-469f-bd40-8f3b0a458cc2" />
</p>
<br />
<p>
  <img width="956" alt="image" src="https://github.com/user-attachments/assets/823c076e-8e40-49ca-99de-4a7e39e53c59" />
</p>
<br />

-   **Overview:** Resolving the hardware issue, including potential troubleshooting steps, coordination with other teams if necessary, and communication with the user.

<hr />
<br />
