# ansible-role-azure-ad-app
Ansible role to create Azure AD App Registrations, create/rotate their passwords and optionally save them in an Azure KeyVault.

# Notes
- Designed to be run on an Ansible Controller, not intended to be run on multiple servers in parallel.
- Is opinionated about App Registration display names, does not allow you to create more than 1 App registration with the same name, and will fail if 2 App Registrations with the same name exist, even though it is possible in Azure.

# Requirements
- Ansible 2.10 or later
- azure.azcollection 2.4.0

# Role Variables
All settable variables with explanations and links are located in the defaults/main.yml

## TODO
- Create Action to publish to Ansible Galaxy
- Write Molecule tests
- Create Action to run Molecule tests
- Create CI
- Add examples to readme

###