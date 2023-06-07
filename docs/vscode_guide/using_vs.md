# Using Ansible Lightspeed with Watson Code Assistant with the VS Code extension

At this time, the Ansible Lightspeed with Watson Code Assistant service is only accessible through the Ansible VS Code extension. See [Installing the Ansible VS Code extension][installing-extension] for instructions on how to get started. This new service is a tool that learns and improves over time. As such, the service may not always generate an output that is expected. Your participation in using Ansible Lightspeed with Watson Code Assistant will inform the service to improve recommendations over time and improve content quality.

## Providing feedback on the service

Ansible Lightspeed with Watson Code Assistant is designed to be improved through feedback on the quality of its suggestions. Technical details of user experiences with Lightspeed can be useful in informing further improvements. We request that all Ansible Lightspeed with Watson Code Assistant users provide constructive feedback to help improve both the recommendations and user experience. Feedback can be submitted directly through the VS Code extension or to the [Ansible Lightspeed with Watson Code Assistant Matrix room: `#ansible-lightspeed:ansible.im`][matrix-room].

To provide feedback through the VS Code extension, click the **Lightspeed** entry in your status bar for options.

## Getting a recommendation

To generate a recommendation from Ansible Lightspeed with Watson Code Assistant:

1. For new files:
     1. Select **File->New Text File** in VS Code.
     2. Click **Select a language** in the new file and select `Ansible`.
     3. Save the file with a YAML extension (`.yml` or `.yaml`).
2. For existing `YAML` files:
     1. Click on the language mode in the bottom right corner of the VS Code editor status bar and set to `Ansible`. If you do not see this section in your editor, you can also select **Configure Language Mode** from the **Command Palette**.
3. Verify that you see an entry for `Lightspeed` in your status bar. If `Ansible` is already selected as the language, then you may need to reselect the language if `Lightspeed` does not appear.
  
      **_NOTE:_** If you see an error message about missing `ansible-lint`, you can install the missing module or disable the linter in **Settings** under **Ansible>Validation>Lint**.

4. Start creating your playbook. Once you have added a task name and press **Enter**, the Ansible Lightspeed with Watson Code Assistant service is engaged. You will see a `Processing` status indicator in the bottom right while Ansible Lightspeed with Watson Code Assistant is preparing your suggestion.

      **_NOTE:_** You will not see a suggestion until you press **Enter** at the end of the task description.

5. Once presented with a suggestion, press `Tab` to accept the recommendation or `Esc` to ignore it.

The actions that you take when a recommendation is provided impact the training process of the
model. If you hit the Esc key to _reject_ a recommendation, then the telemetry process considers
that a rejection of the recommendation. Red Hat and IBM will view that action as the user
determining that the recommendation was not suitable for their task intent.
If you hit enter and _accept_ the recommendation, then the telemetry process considers that
action an acceptance of the recommendation. Red Hat and IBM will view that action as the user
determining that the recommendation was _good enough_ to use over typing an alternative
directly.

If a recommendation is accepted, and then further edits are performed, then the act of changing
the recommendation to something else will be considered a modification of the
recommendation. This will tell Red Hat and IBM that the recommendation required extra action
in order to meet the intended use. And, this information will be used for context in training the
model for similar prompts in the future.

The telemetry data is first anonymized and then sent whenever you switch to a different file in
Visual Studio code or create a new Ansible task in the same Ansible Playbook.

## Improving the recommended guidance

Follow these guidelines to improve the likelihood of a quality recommendation:

* Ensure that your YAML is properly formatted. See [Ansible YAML syntax guidelines][yaml-guidelines] for details.
* Avoid context switching within a single playbook file. Lightspeed attempts to correlate earlier tasks to the active recommendation, and context switching may lead to incorrect recommendations.
* If you do not get a recommendation that aligns with the intent of your task name, then rewording your statement to provide more information on what is desired may lead to different results. Try adding or removing context to see if you get a better response.

## Matching recommendations to training data

The Ansible Lightspeed with Watson Code Assistant machine learning model is trained on content from Ansible Galaxy and other sources.

Given the nature of deep learning technology, as well as the kinds of content used to train and
which are generated by Lightspeed, it is not possible to identify specific training data inputs that
contributed to particular Lightspeed output recommendations. Nevertheless, Lightspeed
includes a feature to help users that are interested in understanding possible origins of
generated content recommendations. When Lightspeed generates a recommendation, it will
attempt to find items in the training dataset that closely resemble the recommendation. In such
cases, Lightspeed will display licensing information and a source repository link for the training
data matches in a panel interface in the VS Code extension.

This feature may enable users to ascertain open source license terms that are associated with
related training data. This feature has been implemented even though it is believed to be unlikely
that either the training data used in fine-tuning or the output recommendations themselves are
generally protected by copyright, or output reproduces training data content controlled by
copyright licensing terms.

Red Hat does not claim any copyright or other intellectual property rights in the suggestions
generated by the Ansible Lightspeed with Watson Code Assistant service.

[installing-extension]: installing_vs.md
[matrix-room]: https://matrix.to/#/#ansible-lightspeed:ansible.im
[yaml-guidelines]: https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html
