# ansible-role-azure-ad-app
Ansible role to manage Azure AD App Registrations and associated Service Principals

What the role does:
- Create an Azure AD App Registration
- Create an associated Service Principal (optional)
- Create/Manage client secrets for the Azure AD App Registration (optional):
    - Create new client secret if there are none
    - Create new client secret if existing secret/secrets are expiring soon
    - Remove already expired client secrets
- Create Key Vault Secret containing the client secret that was created and update it (optional)
- Assign the Service Principal Azure RBAC Roles


# Notes
- Designed to be run on a single server (I prefer Ansible Controller), not intended to be run on multiple servers in parallel.
- Is opinionated about App Registration display names, will not allow you to create an App Registration if another exists with the same name, even though it is possible in Azure.

# Requirements
- Ansible 2.10 or later
- azure.azcollection 2.4.0

# Role Variables
All settable variables with explanations and links are located in the defaults/main.yml

## Future plans
- Create Action to publish to Ansible Galaxy
- Write Molecule tests
- Create Action to run Molecule tests
- Create CI
- Add examples to readme
- Add option to delete/clean up all created resources