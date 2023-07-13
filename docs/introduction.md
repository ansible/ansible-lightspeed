
# Introduction to Ansible Lightspeed with Watson Code Assistant

Ansible Lightspeed with Watson Code Assistant is a joint project between IBM and Red Hat that offers access to Ansible content recommendations through the use of natural language automation descriptions. This project is accessible through the integration of an IBM AI cloud service operated by Red Hat and the Ansible VSCode plugin, and is offered to the Ansible community to use, without cost. This service uses, among other data, roles and collections that are available through the community website, [Ansible Galaxy][galaxy].

This documentation covers how to use Ansible Lightspeed with Watson Code Assistant to help you write automation content, how to participate in model training through Ansible Galaxy settings, and how Red Hat uses machine learning to create content recommendations.

## Automation content creators

Ansible Lightspeed with Watson Code Assistant intends to be your expert reference for writing Ansible content. Like all machine learning products, Ansible Lightspeed with Watson Code Assistant requires constant user feedback to ensure that recommendations are technically accurate and useful. Red Hat describes below what content is collected through automation development to improve the quality of the service.

## Understanding data telemetry

The Ansible VS Code extension, with Ansible Lightspeed with Watson Code Assistant features enabled, automatically collects recommendations, usage telemetry, and playbook state through automated events. Ansible Lightspeed with Watson Code Assistant telemetry is used to improve the service over time. The following table identifies all of the data collected from the VS Code extension and returned to Ansible Lightspeed with Watson Code Assistant.

Telemetry collected will be shared with Red Hat and IBM.  You can opt out of this data being provided back to Ansible Lightspeed with Watson Code Assistant by disabling the Ansible Lightspeed with Watson Code Assistant setting in the Ansible VS Code extension. Opting-out of telemetry does not remove telemetry data already sent to Red Hat and IBM.

**_NOTE:_** The Ansible extension can be configured to collect data that is not used by Ansible Lightspeed with Watson Code Assistant. This table identifies only data used by Ansible Lightspeed with Watson Code Assistant.

| Metric                                                                          | Description                                                                                                                                                                                                                                                   |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Recommendation accepted                                                         | Captured to indicate that a content suggestion was accepted by the user to include in the actively developed playbook.                                                                                                                                        |
| Recommendation rejected                                                         | Captured to indicate that a content suggestion was rejected by the user to include in the actively developed playbook.                                                                                                                                        |
| Task Prompt                                                                     | The contents of the name property of the task used to request a recommendation from Ansible Lightspeed with Watson Code Assistant. This is used to determine what automation developers are prompting Ansible Lightspeed with Watson Code Assistant to offer. |
| Playbook/Role Context                                                           | The contents of a playbook file that exist prior to the task prompt used in the current recommendation. This is used to provide additional context for a recommendation beyond a task prompt.                                                                 |
| Playbook State (captured at various stages before and after the recommendation) | The contents of an Ansible playbook. This is captured to help Ansible Lightspeed with Watson Code Assistant understand what components of a recommendation were valuable or not once a recommendation is provided.                                            |
| Anonymized document URI                                                         | Used to determine the kind of Ansible document (playbook/role/etc).                                                                                                                                                                                           |
| Request and response timestamps                                                 | Captured in UTC format.                                                                                                                                                                                                                                       |
| Anonymized user id                                                              | Captured at (~/.redhat/anonymousid).                                                                                                                                                                                                                          |
| Anonymized suggestion id                                                        | Auto-generated session id associated with service request.                                                                                                                                                                                                    |

## Terms of service

[Click here][terms] to view the Ansible Lightspeed with Watson Code Assistant terms of service.

[galaxy]: https://galaxy.ansible.com
[terms]: tos/index.md
