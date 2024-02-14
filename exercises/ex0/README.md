# Understand the scenario
An employee orders IT equipment (mouse, keyboard, monitor). 
- If the order amount is less than Rs 1000, the _Operational Manager_ should approve it.
- If the order amount is more than Rs 1000, then the _Operational Manager_ should approve it first (L1), and then the _Purchasing Manager_ should approve it next (L2).

In this use case, the cost of the equipment ordered by the employee is more than Rs 1000. Therefore, the employee can receive the ordered equipment, only when both the approvals (multi-level approval) are complete.  

# Expected Flow
Employee places an order > Agent determination is triggered based on the cost involved – in this case, it is a multi-level approval process since the amount exceeds Rs 1000 > Agents are determined based on the functions defined for team members in a team > The approval request is first goes to the team member for L1 approval > The approval request then goes to the team member for L2 approval > Order request is approved once both approvals are obtained.

# Apps, Personas/Roles, and Tasks

| App                | Persona/Role     | Tasks                                                             |
|-----------------   |--------------    |-----------------------------------------------------------        |
|Responsibility Management Service, BTP > Manage Teams and Responsibilities|_BusinessProcessSpecialistResponsibilityManagement_|1.	Create a team, _TEST_APPROVER_, for Team Category, _Procurement_, Team Type, _Operational Purchasing_. 2.	Add two team members: _Dakshayani R _and _JohnProcurementApprover_. 3.	Assign functions to team members: - Dakshayani R: _Purchasing Manager_ - JohnProcurementApprover: _Operational Purchaser_|
|SAP Ariba Buying > Create Purchase Request|Employee|1. Order an equipment above Rs 1000 2.	Check the status of your request.|
|My Inbox|- Operational Purchaser - Purchasing Manager|1. Approve the request (L1). 2. Approve the request (L2).|
|Monitor Workflows|Employee|View logs for your approval tasks.|
