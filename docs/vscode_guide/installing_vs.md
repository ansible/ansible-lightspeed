# Installing the Ansible VS Code extension

You need the latest version of the Ansible VS Code extension to access Project Wisdom functionality.

Prerequisites

* You have [installed VS Code][vs-code].

To install this extension:

1. Open VS Code.

   ```bash
   code .
   ```

2. Click the **Extensions** icon on the left sidebar.
3. Search for **Ansible** in the search box.
4. Click the **Ansible**  language support extension that is published by Red Hat.
5. Click **Install** to install the extension.

To verify your installation:

1. Open a new file and select **Ansible** as the language.
2. Start writing a test playbook. You should see contextual aids as you create your content.

## Configuring the Ansible VS Code extension

**_NOTE:_** Access to this new service is currently open to participants through a rolling release.  If you wish to sign up for access, see [Service Sign-Up][sign-up] for details.

To configure the Ansible VS Code extension for Project Wisdom:

1. Open VS Code.

   ```bash
   code .
   ```

2. Click **File>Preferences>Settings**.
3. In the Search settings bar, type `wisdom`.
4. Check all of the following boxes if they are not already selected:
    1. **Ansible>Wisdom**: Enabled.
    2. **Ansible>Wisdom>Suggestions**: Enabled.
5. In **Ansible>Wisdom: Base Path**, enter the following: [https://pilot.wisdom.testing.ansible.com/][base-path].
6. In **Ansible>Wisdom: Auth Token**, paste the authentication token you collected above.
7. Close the **Settings** tab.

[vs-code]: https://code.visualstudio.com/
[sign-up]: ../introduction.md#signing-up-for-project-wisdom
[base-path]: https://pilot.wisdom.testing.ansible.com/
