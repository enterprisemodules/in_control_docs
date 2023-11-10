---
layout: documentation
title: Node groups page
keywords: compliance security vulnerability incontrol
toc: false
---
The "Node Groups" page displays a table of all registered node groups. 

<img src="/in_control_docs/docs/images/node-groups.jpg">

## The Node Groups Table

This table provides the following information for each node group:

| Column | Description |
| --- | --- |
| Node group name | The name of the node group. Clicking the name will take you to the node group details page. |
| Description | A short description of the node group|
| Number of nodes | The number of nodes that belong to this node group. |
| Compliance State | A small graphical overview of the compliance state of this node group. |
| Vulnerability State | A small graphical overview of the vulnerability state of this node group. |

## Searching the Table

To filter the results, simply enter a search query into the search field located at the top of the page. You can search on node group names.

## Node group details

This section displays node details and provides all the information that InControl has collected about all nodes in your node group..

![Node group details](/in_control_docs/docs/images/node-group-details.jpg)

## Compliance graph

The compliance graph on the left provides statistics for compliance controls on all the nodes in the selected node group. At the top of the graph, the total number of controls for the node is displayed. The graph shows the percentages of failed, passed, and skipped controls.

At the bottom left of the graph, you can find a link to the "Current compliance details". Clicking on [this link](/docs/in_control/controls.html) will take you to a detailed overview of the state of all controls applied to this node group.

At the bottom right of this graph, you can find a link to "Compliance through time". Clicking on [this link](#TODO) will take you to an overview of the compliance through time.

![Compliance Graph](/in_control_docs/docs/images/node-group-details-compliance-graph.jpg)

## Vulnerability graph

The vulnerability graph on the right displays statistics for all detected vulnerabilities on the selected nodes in the node group. At the top of the graph, the total number of detected vulnerabilities for the node is displayed. The graph shows the percentages of critical, high, medium, and low vulnerabilities.

![Vulnerability Graph](/in_control_docs/docs/images/node-group-details-vulnerability-graph.jpg)

At the bottom left of the graph, you can find a link to the "Current vulnerability details". Clicking on [this link](/docs/in_control/controls.html) will take you to a detailed overview of the state of all vulnerabilities detected on this node group.

At the bottom right of this graph, you can find a link to "Vulnerability through time". Clicking on [this link](#TODO2) will take you to an overview of the detected vulnerabilities through time.

## Tab Recent Compliance reports

This tab shows a table of the 10 most recent compliance reports for the nodes this node group . By clicking on a report, you will see a more detailed overview of the corresponding compliance report.

![Tab Recent Compliance Reports](/in_control_docs/docs/images/node-group-details-recent-compliance-reports.jpg)

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

## Tab Recent Vulnerability reports

This tab shows a table of the 10 most recent vulnerability reports for the nodes this node group. By clicking on a report, you will see a more detailed overview of the corresponding vulnerability report.

![Tab Recent Vulnerability reports](/in_control_docs/docs/images/node-group-details-recent-vulnerability-reports.jpg)

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

## Tab Nodes in group

This tab shows a list of all nodes that are part of the node group.

![Nodes in node group](/in_control_docs/docs/images/node-group-details-nodes-in-group.jpg)

Clicking on a will take you to the [node details page](/docs/in_control/node_details.html)