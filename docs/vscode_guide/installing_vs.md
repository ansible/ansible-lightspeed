# Installing the Ansible VS Code extension

You need the latest version of the Ansible VS Code extension to access Project Wisdom functionality.

Prerequisites

* You have [installed VS Code][vs-code]. A minimum version of 1.70.1 is required.

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
5. In **Ansible>Wisdom: Base Path**, enter the following: [http://c.ai.ansible.redhat.com/][base-path].
6. Close the **Settings** tab.
7. Open the **Ansible** side bar and click **Connect**.
8. Follow the prompts to sign in to Project Wisdom using your GitHub credentials.
9. Carefully review the Terms and **Agree** or **Disagree**. If you click Disagree, you will not be able to complete the login. Lastly, follow the prompt to allow VSCode to interact with Project Wisdom on your behalf.
10. Upon successful completion of the login flow, you should see a “Logged in as <your github id>” message in the Ansible side bar.

[vs-code]: https://code.visualstudio.com/
[sign-up]: ../introduction.md#signing-up-for-project-wisdom
[base-path]: https://pilot.wisdom.testing.ansible.com/
