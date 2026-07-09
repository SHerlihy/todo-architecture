# Business Requirements Questions v1.0

### 1.2

How much work is missed?
This is not yet quantified in the BRD. The intended business outcome is to reduce missed work, so the project should be measured against a baseline after launch.

What personal or team organization improvements are expected?
Users should be able to capture tasks quickly, keep work organized by list/category, and review open, completed, and overdue items without extra process overhead.

### 1.3

What is a user?
- internal
- customer
- all of the above
For this project, a user is an end user of the task tracker. The current BRD does not narrow that to internal-only or customer-only use, so "all of the above" is the safest interpretation.

What time is "at a glance"?
Immediately on opening the main task view, without needing extra navigation or onboarding.

What modern browsers specifically?
Current versions of Chrome, Firefox, Safari, and Edge.

### 2.1

What data is in a task?
Title, description, due date, priority, status, and list/category assignment.

How does a user enter details for authentication?
Through a standard sign-in flow using secure credentials; the BRD does not define a specific method beyond secure authentication.

### 5

what is the nature of data in task details?
Primarily plain text and structured task metadata such as dates, status, and priority.

will they be permitted to paste in a gif?
No. File attachments are out of scope, so pasted GIF content should not be treated as supported task data.

### 6.1

How do we define "common actions"?
- already known?
- user feedback?
- observability mechanisms?
Common actions are the core workflow actions the BRD already names: create, edit, complete, delete, filter, and sort tasks. The exact prioritization can later be validated with usage data or user feedback.

### 6.2

what is main task view?
The default list view showing the user’s tasks, with open/completed/overdue states visible and accessible.

what is quickly? sub 100ms or 10ms?
The BRD only requires that task updates feel immediate in normal use. It does not commit to a hard latency target.

what is immediatly after save? again 100ms or 10ms?
or optimistic?
The safest interpretation is optimistic UI behavior where the saved change appears right away, with error handling if persistence fails.


### 6.3

what level of failed saves is allowed?
The BRD does not define an error budget. The requirement is that failed saves are clearly reported and user data is not lost during normal operation.

### 6.4

transmitted securely
- end to end encryption
- encryption at rest
- why is it PII? medical info?
At minimum, transport should use HTTPS/TLS and stored data should be protected at rest. The BRD does not classify the task data as sensitive PII or medical information.
