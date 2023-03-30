
# Introduction to Project Wisdom

Project Wisdom is a joint project between IBM and Red Hat that offers access to Ansible content recommendations through the use of natural language automation descriptions. This project is accessible through the integration of an IBM AI cloud service operated by Red Hat  and the Ansible VSCode plugin,  and is offered to the Ansible community to use, without cost.  This service uses, among other data, roles and collections that are available through the community website, [Ansible Galaxy][galaxy].

This documentation covers how to use Project Wisdom to help you write automation content, how to participate in model training through Ansible Galaxy settings, and how Red Hat uses machine learning to create content recommendations.

## Automation content creators

Project Wisdom intends to be your expert reference for writing Ansible content. Like all machine learning products, Project Wisdom requires constant user feedback to ensure that recommendations are technically accurate and useful. Red Hat describes below  what content is collected through automation development to improve the quality of the service.

## Understanding data telemetry

The Ansible VS Code extension, with Project Wisdom features enabled, automatically collects recommendations, usage telemetry, and playbook state through automated events.Telemetry regarding how Project Wisdom is used will be an important set of data that allows Red Hat to improve recommendations over time. The following table identifies all of the data collected from the VS Code extension and returned to Project Wisdom. You can opt out of this data being provided back to Project Wisdom by disabling the Project Wisdom setting in the Ansible VS Code extension . Telemetry collected in this manner will be shared with Red Hat and IBM.

**_NOTE:_** The Ansible extension can be configured to collect data that is not used by Project Wisdom. This table identifies only data used by Project Wisdom.

| Metric                                                                          | Description                                                                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recommendation accepted                                                         | Captured to indicate that a content suggestion was accepted by the user to include in the actively developed playbook.                                                                           |
| Recommendation rejected                                                         | Captured to indicate that a content suggestion was rejected by the user to include in the actively developed playbook.                                                                           |
| Task Prompt                                                                     | The contents of the name property of the task used to request a recommendation from Project Wisdom. This is used to determine what automation developers are prompting Project Wisdom to offer. |
| Playbook/Role Context                                                           | The contents of a playbook file that exist prior to the task prompt used in the current recommendation. This is used to provide additional context for a recommendation beyond a task prompt.   |
| Playbook State (captured at various stages before and after the recommendation) | The contents of an Ansible playbook. This is captured to help Project Wisdom understand what components of a recommendation were valuable or not once a recommendation is provided.             |
| Anonymized document URI                                                         | Used to determine the kind of Ansible document (playbook/role/etc).  |
| Request and response timestamps                                                 | Captured in UTC format.  |
| Anonymized user id                                                              | Captured at (~/.redhat/anonymousid).  |
| Anonymized suggestion id                                                        | Auto-generated session id associated with service request.  |

## Signing up for Project Wisdom

 Project Wisdom will be open to participants through a rolling release so that the scalability of the platform can be tested to limit outages. Therefore, access to the service will start with a set of participants, with additional sets of participants added at a regular cadence until the service is open for any registration. If you are interested in registering for Project Wisdom, please complete the [sign-up form][sign-up-form]. Participants will be added in the order they are received. After registering you will need to provide your GitHub ID for service access, as GitHub is used to sign in to Project Wisdom.

## Terms of service

[Click here][terms] to view the Project Wisdom terms of service.

[galaxy]: https://galaxy.ansible.com
[sign-up-form]: https://www.redhat.com/en/engage/project-wisdom#sign-up
[terms]: tos/index.md
