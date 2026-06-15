# Dynamic-Configuration-Templating-

Project Description – Dynamic Configuration Templating:

In this challenge, you are implementing a common DevOps practice called configuration management through templating. Instead of maintaining separate configuration files for different environments (Staging, Production, etc.), you create a single Jinja2 template and let Ansible dynamically generate the final configuration files using variables stored in the inventory.

Objectives
Create a reusable Spring Boot configuration template
Use Jinja2 placeholders ({{ variable_name }}) in application.properties.j2.
Replace hardcoded values with environment-specific variables from the inventory.
Deploy environment-specific configurations
Use the Ansible template module to render the template.
Generate different application.properties files for each server automatically.
Improve security
Store sensitive values such as database passwords in inventory variables rather than source code.
Restrict permissions on the generated configuration file using mode 0600.
Support multiple environments
Staging and Production servers can have different:
Application ports
Environment profiles
Database URLs
Database usernames
Database passwords
The same playbook and template work for all environments.
Skills Demonstrated
Ansible Playbooks
Jinja2 Templating
Inventory Variables
Configuration Management
Infrastructure Automation
Security Best Practices
Environment-Specific Deployments
Expected Outcome

After running the playbook:

Ansible reads application.properties.j2.
Variables are pulled from inventory.ini.
A customized application.properties file is created on each server.
The file is placed at:
{{ root }}/etc/myapp/config/application.properties
File permissions are secured:
0600
Both web_stage and web_prod receive their own correctly configured Spring Boot settings without maintaining separate configuration files.

This challenge simulates a real-world DevOps workflow where a single codebase is deployed across multiple environments while keeping configurations secure, maintainable, and automated.
