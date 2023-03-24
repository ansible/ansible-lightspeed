# Contributing to Project Wisdom

## Role/Collection/Module Developers

Seasoned Ansible content developers may not need content recommendations for writing automation, but expert content developers can still participate in the Project Wisdom community through continued content development.

## Ansible Galaxy

Project Wisdom integrates with the next generation of [Ansible Galaxy][beta-galaxy]. This solution is based on the [Ansible Galaxy NG][galaxy-ng] project. Content developers will have the option to include or exclude files from their namespace in the training model for Project Wisdom.

### Including or Excluding content

Ansible collections and roles that are submitted to various sources are automatically included in training Project Wisdom models. Despite Project Wisdom being trained on publicly available Ansible content, Red Hat understands that some content developers will not want their roles and collections that were submitted specifically to Ansible Galaxy be used to train machine learning models.

Ansible Galaxy users may choose to exclude their content as follows:

1. Login to [Ansible Galaxy NG][beta-galaxy].
2. Click **Collections->Namespaces** from the left-hand navigation.
3. Click on each namespace you wish to change, and then:
    1. Click the three-vertical-dot icon in the upper right hand corner.
    2. Select `Include` or `Exclude` to change whether your content is included or excluded from training Project Wisdom.

Once you set your include/exclude preferences for your namespaces, your content will be added or removed from the Project Wisdom [model training][model-training] during the next iteration of model training.

[beta-galaxy]: https://beta-galaxy-dev.ansible.com/ui/
[galaxy-ng]: https://galaxyng.netlify.app/
[model-training]: machine_learning.md#model-training
