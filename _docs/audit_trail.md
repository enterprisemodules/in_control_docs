---
layout: documentation
title: Audit Trail
keywords: compliance security vulnerability incontrol
toc: false
---

The audit trail page is an important tool that displays the audit trail of **all** actions across **all** nodes. This can provide you with a comprehensive view of what has happened to your systems, including changes to detected vulnerabilities and configuration settings that are protected by (CIS) compliance controls. This information can help you identify vulnerabilities and other issues that require attention.

In addition to operational changes, the audit trail also includes a list of management changes, which refer to changes made by you or a colleague to the settings of InControl. These changes can have a significant impact on the security of your systems, and it is important to keep track of them. For instance, changing the "action" setting of a control from "Enforce" to "Skip" will appear in the audit trail, allowing you to see who executed the change and the reason they specified for the change.

By regularly reviewing the audit trail, you can identify patterns of behavior and detect potential compliance and security issues before they become a problem. This can help you to proactively manage your systems and keep them secure.

<img src="/in_control_docs/docs/images/audit-trail.jpg">

The audit trail table is a crucial feature in the InControl system. It contains six columns that provide valuable information about the changes made to the system. Let's take a closer look at each of these columns:

| Column | Description |
| --- | --- |
| Date/Time| This column shows the date and time the audit record was registered in InControl. If the change is backed by a Vulnerability- or Compliance report containing the relevant change, clicking the date takes you to the connected report. This feature ensures that users can easily access important information about changes made to the system.|
| Type| The type of audit record is displayed in this column. It is key to understand the type of record in order to know what kind of change was made. See the list of types [below](#audit-trail-record-types)|
| Environment| The name of the Puppet environment the node is running in. Clicking this will take you to the [Environment details page](/docs/in_control/environment_details.html)|
| Node | The name of the node. Clicking this will take you to the [Node details page](/docs/in_control/node_details.html)|
| Message| A brief message describing the sort of change registered at a meta level is displayed in this column. This is useful when trying to get a high-level understanding of what changes were made.|
| Reason| The reason the user cited for the change in the settings is displayed in this column. This is important for understanding the thought process behind the change.|
| User| The InControl user who registered the change is displayed in this column. This is only stored for changes in InControl settings. For changes in the operational state, no user is stored and the column is empty. This information is valuable for tracking who made changes to the system.|


### Audit Trail record types

InControl provides a comprehensive set of Audit Trails that enable users to monitor various aspects of their system. These Audit Trails are categorized as follows:

- Initial Vulnerability State: This Audit Trail records the initial Vulnerability report.
- Initial Compliance State: This Audit Trail records the initial Compliance report.
- Vulnerability State Change: This Audit Trail tracks changes in detected vulnerabilities, including both additions and removals. By clicking on the date field, users can inspect the underlying report and determine if any actions need to be taken.
- Compliance State Change: This Audit Trail tracks changes in compliance state, including both increases and decreases in compliance. By clicking on the date field, users can inspect the underlying report and determine if any actions need to be taken.
- Vulnerability Node Setting: This Audit Trail records when an InControl user modifies the action to be taken on a detected vulnerability. This provides users with a detailed record of any changes made to their system.
- Control Change: This Audit Trail records when an InControl user modifies the action to be taken for a specified compliance control. By having a detailed record of any control changes, users can ensure that their system is always in compliance.
- Compliance Node Setting: This Audit Trail records when an InControl user modifies the settings of a node. This is particularly useful for users who have multiple nodes and need to keep track of changes made to each.
- User Change: This Audit Trail records when an InControl administrator modifies a user. This provides users with an added layer of security by ensuring that all user changes are documented and can be tracked if necessary.