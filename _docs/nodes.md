---
layout: documentation
title: Nodes page
keywords: compliance security vulnerability incontrol
toc: false
---
The "Nodes" page displays a table of all registered nodes.

<img src="/in_control_docs/docs/images/nodes.jpg">

## The Nodes Table

This table provides the following information for each node:

| Column | Description |
| --- | --- |
| Node name | The name of the node. Clicking the name will take you to the Node details page. |
| Environment | The number of nodes that belong to this Puppet environment. |
| Compliance State | A small graphical overview of the compliance state of this node. |
| Vulnerability State | A small graphical overview of the vulnerability state of this node. |

## Searching the Table

To filter the results, simply enter a search query into the search field located at the top of the page. You can search on node and environment names.

![Node details](/in_control_docs/docs/images/node-details.jpg)

# Node details

## Compliance graph

The compliance graph on the left provides statistics for compliance controls on the selected node. At the top of the graph, the total number of controls for the node is displayed. The graph shows the percentages of failed, passed, and skipped controls.

At the bottom left of the graph, you can find a link to the "Current compliance details". Clicking on [this link](/docs/in_control/controls.html) will take you to a detailed overview of the state of all controls applied to this node.

At the bottom right of this graph, you can find a link to "Compliance through time". Clicking on [this link](#TODO) will take you to an overview of the compliance through time.

![Compliance Graph](/in_control_docs/docs/images/node-details-compliance-graph.jpg)

## Vulnerability graph

The vulnerability graph on the right displays statistics for all detected vulnerabilities on the selected node. At the top of the graph, the total number of detected vulnerabilities for the node is displayed. The graph shows the percentages of critical, high, medium, and low vulnerabilities.

![Vulnerability Graph](/in_control_docs/docs/images/node-details-vulnerability-graph.jpg)

At the bottom left of the graph, you can find a link to the "Current vulnerability details". Clicking on [this link](/docs/in_control/vulnerability_occurrences.html) will take you to a detailed overview of the state of all vulnerabilities detected on this node.

At the bottom right of this graph, you can find a link to "Vulnerability through time". Clicking on [this link](#TODO2) will take you to an overview of the detected vulnerabilities through time.

## Tab Recent Compliance reports

This tab shows a table of the 10 most recent compliance reports for this node. By clicking on a report, you will see a more detailed overview of the corresponding compliance report.

![Tab Recent Compliance Reports](/in_control_docs/docs/images/node-details-recent-compliance-reports.jpg)

This table provides the following information for each compliance report:

| Column | Description |
| --- | --- |
| Date/Time| The date and time the report was registered in InControl. Clicking this will take you to a more detailed overview of the corresponding [compliance report](/docs/in_control/compliance_reports.html)|
| Node| The name of the node. Clicking this will take you to the [Node details page](/docs/in_control/node_details.html)|
| Environment| The name of the Puppet environment the node is running in. Clicking this will take you to the [Environment details page](/docs/in_control/environment_details.html)|
| Passed|The number of Passed controls in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Failed| The number of Failed controls in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Skipped| The number of Skipped controls in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Compliance Overview| A concise graphical overview of the compliance state of the node in this report|

At the bottom of the table, you will find a link named ["All compliance reports for *node*"](/docs/in_control/compliance_reports.html) that will take you to an overview of **all** compliance reports for the selected node.

## Tab Recent Vulnerability reports

This tab shows a table of the 10 most recent vulnerability reports for this node. By clicking on a report, you will see a more detailed overview of the corresponding vulnerability report.

![Tab Recent Vulnerability reports](/in_control_docs/docs/images/node-details-recent-vulnerability-reports.jpg)

This table provides the following information for each vulnerability report:

| Column | Description |
| --- | --- |
| Date/Time| The date and time the report was registered in InControl. Clicking this will take you to a more detailed overview of the corresponding [vulnerability report](/docs/in_control/vulnerability_reports.html)|
| Node| The name of the node. Clicking this will take you to the [Node details page](/docs/in_control/node_details.html)|
| Environment| The name of the Puppet environment the node is running in. Clicking this will take you to the [Environment details page](/docs/in_control/environment_details.html)|
| Critical| The number of Critical vulnerabilities in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| High| The number of High vulnerabilities in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Medium| The number of Medium vulnerabilities in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Low| The number of Low vulnerabilities in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Skipped| The number of Skipped vulnerabilities in this report. When there are differences compared to the previous report, statistics of the differences will also be displayed.|
| Vulnerability Overview| A concise graphical overview of the vulnerability state of the node in this report|


At the bottom of the table, you will find a link named ["All vulnerability reports for *node*"](/docs/in_control/vulnerability_reports.html) that will take you to an overview of **all** vulnerability reports for the selected node.

## Tab Node facts

This tab shows a table of **all** facts Puppet has fetched for this node.

![Tab Node facts](/in_control_docs/docs/images/node-details-node-facts.jpg)

This table provides the following information for each fact:

| Column | Description |
| --- | --- |
| Fact| The full name of the fact.|
| Value| The value of the fact. If the fact is a structured fact, this column will show all elements of the fact|

## Tab Audit Trail

This tab shows a table of **all** facts Puppet has fetched for this node.

![Audit Trail](/in_control_docs/docs/images/node-details-audit-trail.jpg)

This table provides the following information for each audit trail record:

| Column | Description |
| --- | --- |
| Date/Time | Indicates the date and time when the change was registered. Clicking the date/time takes you to the details of the change, if available. |
| Type | Shows the type of audit trail record. Refer to [here](#TODO) for more information on types of audit trail records. |
| Node | Displays the name of the node. Clicking this will take you to the [Node details page](/docs/in_control/node_details.html). |
| Environment | Shows the name of the Puppet environment the node is running in. Clicking this will take you to the [Environment details page](/docs/in_control/environment_details.html). |
| Message | Provides a description of the content of the change. |
| Reason | Explains the reason for the change. |
| User | Displays the InControl user who executed the change. |

