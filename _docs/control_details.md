---
layout: documentation
title: Compliance Control Details
keywords: compliance security vulnerability incontrol
toc: false
---

This section displays all information about the selected compliance control.

![Control](/in_control_docs/docs/images/control-details.jpg)

## Details table

The top part of the page contains all available details for the selected compliance control.

![Control details](/in_control_docs/docs/images/control-details-table.jpg)

| Item | Description |
| --- | --- |
| Description| A brief description of the compliance control. This text is taken from the CIS document|
| Rationale| The reason for the control. This text is taken from the CIS document|
| Impact| The potential impact of implementing the control on your system. This field is usually empty, but an empty field does not necessarily indicate no impact.|
| Module| The Puppet module that contains the compliance control|
| Priority| The priority the customer has assigned to this control|

The priority of a compliance control is the priority that you assign to it. The higher the number, the higher the priority for this control. You can use this to sort the priority of the failing controls detected. This list is displayed in order of priority on the [dashboard page](/docs/in_control/dashboard.html).

When you click the edit button, you will be taken to a page where you can [change the priority of the selected control](#TODO). For every change, you will have to provide a reason. Every change in priority will be logged in the [audit trail](/docs/in_control/audit_trail.html).

## Used on nodes

![Control used on nodes](/in_control_docs/docs/images/control-details-used-on-nodes.jpg)

This table provides information on the selected compliance control for each node:

| Column | Description |
| --- | --- |
| Node| The name of the node. Clicking this takes you to the [Node details page](/docs/in_control/node_details.html)|
| Environment| The name of the Puppet environment the node runs in. Clicking this takes you to the [Environment details page](/docs/in_control/environment_details.html)|
| Messages| Compliance messages when the control was checked|
| State| The state of the control on the node|
| Overall Control State	| A concise graphical overview of the current compliance state of the node|
| Action | The Puppet action for this node (See explanation below table)|

The action determines what Puppet will do with this compliance control. InControl offers the following:

- Puppet default
- Enforce only
- Validate only
- Validate & Enforce
- Skip

### Puppet default

When you select `Puppet default`, Puppet applies the action specified when adding the InControl Client to the node. Check [here](/docs/in_control/client.html#default_operation) for more information.

### Enforce Only

This is how regular Puppet code works: Puppet applies the classes and enforces the configuration for the (CIS) compliance controls. When you use this action, check the Puppet console for changes that Puppet made to the configuration. **No** other reporting is done to InControl. Compliance results will not appear in the InControl console.

### Validate Only

This is what sets InControl apart from regular Puppet compliance modules. When you select this action, Puppet does not make any system changes. Instead, it inspects your system and assesses the validity of the (CIS) compliance controls. In other words, it identifies which controls are compliant and which ones are not. Depending on the value of your `report_as `parameter, the results are communicated either back to Puppet or to the InControl Console. This feature is useful for those wanting a more detailed understanding of their compliance status. A full report of the controls not in compliance gives a better understanding of where the system is vulnerable and what changes are necessary to achieve full compliance. This helps stay ahead of potential threats and maintain a high level of security for the system.

### Validate & Enforce

When you select `Validate & Enforce` as the action, Puppet checks the configuration of your environment and reports the results back to either Puppet or the InControl Console. This provides a detailed overview of your environment's current state, including any deviations from the expected configuration.

After reporting, Puppet enforces the classes for the specified CIS control. Puppet fixes any deviations found from the configuration detailed in the CIS control, ensuring that the environment is in compliance with the specified security requirements.

Reporting is done first, followed by fixing. This process ensures that any manual changes that break compliance are detected and reported to InControl. It provides a complete overview of your environment's compliance status, crucial for maintaining a secure and compliant environment.

In summary, selecting `Validate & Enforce` as the default operation in Puppet ensures that your environment is always in compliance with the specified security requirements. The process of reporting and fixing ensures that any deviations from the expected configuration are identified and addressed. This provides you with a complete overview of your environment's compliance status, important for maintaining a secure and compliant environment.

When you select `Validate & Enforce` as the default operation, Puppet checks the configuration of your system/database/cloud environment and reports back the results to either Puppet or the InControl Console. After that, Puppet enforces the classes for the specified security (CIS) control and fixes any deviations it finds from the configuration detailed in the CIS control. Beware that reporting is done first, followed by fixing. This ensures that any manual changes that break compliance are always detected and reported to InControl, so you get a complete overview.

### Skip

Not all (CIS) compliance controls may be relevant to your specific situation. If you choose not to change the current configuration and opt out of certain controls, it is important to note that you may be leaving your system vulnerable to potential security risks. One option is to select `Skip` as the default operation for controls not applicable to your environment. This prevents InControl from reporting any failures on those specific controls **and** enforcing changes so the system is in the state demanded by the control. However, it is recommended to review and reassess your compliance needs periodically to ensure that your system remains secure and up-to-date with the latest industry standards. Taking such proactive measures can help you stay ahead of potential security threats and maintain a strong security posture for your organization.

## Changing the Action

If you want to change the `action` for one or more nodes, either click the 'Edit' button or select the nodes you want to change and press the 'Edit selected' button. This takes you to [the edit page](#TODO). Here you can change the action. For every change, provide a rationale. The change with its rationale is written to the [audit trail](/docs/in_control/audit-trail.html).
