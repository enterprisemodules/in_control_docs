---
layout: documentation
title: Environments page
keywords: compliance security vulnerability incontrol
toc: false
---

The "Environments" page displays a table of all detected Puppet environments.

<img src="/in_control_docs/docs/images/environments.jpg">

## The Environments Table

This table provides the following information for each environment:

| Column | Description |
| --- | --- |
| Environment name | The name of the Puppet environment. Clicking the name will take you to the Environments details page. |
| Number of nodes | The number of nodes that belong to this Puppet environment. |
| Compliance State | A small graphical overview of the compliance state of this Puppet environment. |
| Vulnerability State | A small graphical overview of the vulnerability state of this Puppet environment. |

## Searching the Table

To filter the results, simply enter a search query into the search field located at the top of the page. You can search on environment names.

## Environment Details
This section displays Environment details and provides all the information that InControl has collected about your Environment.

![Environment Details](/in_control_docs/docs/images/environment-details.jpg)

## Compliance graph

The compliance graph on the left provides statistics for compliance controls on the selected environment. At the top of the graph, the total number of controls for the environment is displayed. The graph shows the percentages of failed, passed, and skipped controls.

At the bottom left of the graph, you can find a link to the "Current compliance details". Clicking on [this link](/docs/in_control/controls.html) will take you to a detailed overview of the state of all controls applied to this environment.

At the bottom right of this graph, you can find a link to "Compliance through time". Clicking on [this link](#TODO) will take you to an overview of the compliance through time.

![Compliance Graph](/in_control_docs/docs/images/environment-details-compliance-graph.jpg)

## Vulnerability graph

The vulnerability graph on the right displays statistics for all detected vulnerabilities on the selected environment. At the top of the graph, the total number of detected vulnerabilities for the environment is displayed. The graph shows the percentages of critical, high, medium, and low vulnerabilities.

![Vulnerability Graph](/in_control_docs/docs/images/environment-details-vulnerability-graph.jpg)

At the bottom left of the graph, you can find a link to the "Current vulnerability details". Clicking on [this link](/docs/in_control/vulnerability_occurrences.html) will take you to a detailed overview of the state of all vulnerabilities detected on this environment.

At the bottom right of this graph, you can find a link to "Vulnerability through time". Clicking on [this link](#TODO2) will take you to an overview of the detected vulnerabilities through time.

## Nodes in enviromment

Here you see a list of all nodes that are part of the Puppet enviroment.

![Node Table](/in_control_docs/docs/images/environment-details-node-table.jpg)

This table provides the following information for each node:

| Column | Description |
| Node Name| The date and time the report was registered in InControl. Clicking this will take you to a more detailed overview of the corresponding [compliance report](/docs/in_control/compliance_reports.html)|
| Node name| The name of the node. Clicking this will take you to the [Node details page](/docs/in_control/node_details.html)|
| Environment| The name of the Puppet environment the node is running in. Clicking this will take you to the [Environment details page](/docs/in_control/environment_details.html)|
| Overall Compliance State| A concise graphical overview of the current compliance state of the environment|
| Overall Vulnerability State| A concise graphical overview of the current vulnerability state of the environment|
