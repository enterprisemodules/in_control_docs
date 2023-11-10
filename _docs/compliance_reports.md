---
layout: documentation
title: Compliance Reports
keywords: compliance security vulnerability incontrol
toc: false
---

This section shows you an overview of all compliance reports through time for all nodes.

<img src="/in_control_docs/docs/images/compliance-reports.jpg">

## Search

In the search field, you can enter node and Pupept environments to narrow doen the reports shown in the table.

## Reports table

The reports table provides the following information for each compliance report:

| Column | Description |
| --- | --- |
| Date/Time| The date and time the report was registered in InControl. Clicking this will take you to a more detailed overview of the corresponding [compliance report](/docs/in_control/compliance_reports.html)|
| Node| The name of the node. Clicking this will take you to the [Node details page](/docs/in_control/node_details.html)|
| Environment| The name of the Puppet environment the node is running in. Clicking this will take you to the [Environment details page](/docs/in_control/environment_details.html)|
| Passed|The number of Passed controls in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Failed| The number of Failed controls in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Skipped| The number of Skipped controls in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Compliance Overview| A concise graphical overview of the compliance state of the node in this report|

# Compliance Report details

This section provides a comprehensive overview of one of the selected compliance report. 

<img src="/in_control_docs/docs/images/compliance-report-details.jpg">

## Report statistics

At the top of the InControl page, detailed statistics are displayed to provide you with an overview of your controls. These statistics provide information on the number of passed, failed, and skipped controls. For each type, InControl will show you the current and previous numbers of controls in that state. Moreover, if there is a change between the current and previous numbers, InControl will display the difference as an absolute number and as a percentage, so that you can see at a glance how your controls have been performing. The color of the indicator will also inform you whether it is an improvement or a decline. Green indicates an improvement, and red indicates a decline. Therefore, these statistics are incredibly useful for monitoring the progress of your controls and identifying areas for improvement.

<img src="/in_control_docs/docs/images/compliance-report-details-statistics.jpg">

## Report change log

While the statistics at the top of the page provide a useful overview, it is important to delve deeper into the data to gain a full understanding of the changes that have occurred. InControl recognizes this need and offers a change log to help users identify the differences between the previous and current reports.

The change log displays a detailed account of how controls have transitioned from one state to another. It highlights which controls have been added, and which ones have been removed, allowing users to gain a comprehensive understanding of the changes that have occurred. By using the change log, you can quickly identify areas that require attention and address them before they become problematic.

Moreover, the log provides a complete history of changes made to the controls, which can be extremely useful for tracking and auditing purposes. It ensures that all changes made to the controls are recorded accurately, enabling users to easily review and approve them.

<img src="/in_control_docs/docs/images/compliance-report-details-change-log.jpg">

## Report controls

This table contains a list of all the (CIS) Compliance controls that where checked for this report.  The table contains the next columns:

<img src="/in_control_docs/docs/images/compliance-report-details-controls.jpg">


| Column | Description |
| --- | --- |
| Control | This column displays the name of the control. The first part of the name before the :: indicates the module that contains the control. The second part is shot description of the function of the control.|
| Environment | This column displays the name of the Puppet environment in which the node is currently running. Clicking on this column will take you to the [Environment details page](/docs/in_control/environment_details.html). |
| Node | This column displays the name of the node. Clicking on this column will take you to the [Node details page](/docs/in_control/node_details.html). |
| Target | This column displays the target used for each control. Some controls may target multiple instances, such as Oracle database controls that can target multiple databases. |
| Messages | This column displays the results of the control compliance checks. A control can contain multiple checks. The message color indicates whether the check passed or failed. |
| Action | This column displays the Puppet action for this node. For more information, please see the explanation below the table. |
| State | This column displays the overall state of the control on this target. |

### Action

The action determines what Puppet will do with this compliance control. InControl offers the following:

- Puppet default
- Enforce only
- Validate only
- Validate & Enforce
- Skip

## Edit control

To modify the behavior of the control for a specific target, simply click on the "Edit" button. This will take you the the [Edit control form](/docs/in_control/control_edit_action.html)