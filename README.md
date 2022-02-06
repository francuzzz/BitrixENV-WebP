# Ansible role for config WebP compression images in BitrixENV

First, let's MAKE the latest version from the source data.

 1. Let's check the latest version in [WebP Develorers Page](https://storage.googleapis.com/downloads.webmproject.org/releases/webp/index.html)
 2. Write it to a variable **./deploy_webp/vars/main.yml**
 3. Check the paths to the Bitrix directories in the file **./deploy_webp/defaults/main.yml**

This role will build the WebP from the source files, make the config for **NGINX** and add the call to the main NGINX config.

Before restarting **NGINX**, there is a check for the validity of the configuration. If something goes wrong, you can always restore the original configuration files, which Ansible will carefully save with the *.bak* extension.

### Run

```
terminal> ansible-playbook playbook-webp.yml
```
