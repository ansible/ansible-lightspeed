# Installing the Ansible VS Code extension

You need the latest version of the Ansible VS Code extension to access Ansible Lightspeed with Watson Code Assistant functionality.

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

1. Create a new YAML file using the “.yml” or “.yaml” file extension.
2. Associate the Ansible language type with the new YAML file by clicking on the language
indicator - which is located on the right hand of the Status Bar, and selecting Ansible
from the dropdown.
3. Start writing a test playbook. You should see contextual aids as you create your content.

## Configuring the Ansible VS Code extension

To configure the Ansible VS Code extension for Ansible Lightspeed with Watson Code Assistant:

1. Open VS Code.

      ```bash
      code .
      ```

2. Click **File>Preferences>Settings**.
3. In the Search settings bar, type `lightspeed`.
4. Check all of the following boxes if they are not already selected:
    1. **Ansible>Lightspeed**: Enabled.
    2. **Ansible>Lightspeed>Suggestions**: Enabled.
5. In **Ansible>Lightspeed: Base Path**, enter the following: [http://c.ai.ansible.redhat.com/][base-path].
6. Close the **Settings** tab.
7. Open the **Ansible** side bar icon on the left-hand side of the Visual Studio Code interface and click **Connect**.
8. Follow the prompts to sign in to Ansible Lightspeed with Watson Code Assistant using your GitHub credentials.
9. Carefully review the Terms and **Agree** or **Disagree**. If you click Disagree, you will not be able to complete the login. Lastly, follow the prompt to allow VSCode to interact with Ansible Lightspeed with Watson Code Assistant on your behalf.
10. Upon successful completion of the login flow, you should see a “Logged in as <your github id>” message in the Ansible side bar.

[vs-code]: https://code.visualstudio.com/
[base-path]: http://c.ai.ansible.redhat.com/
