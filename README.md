[![Build Status](https://cloud.drone.io/api/badges/dtf-ein/drupal-stack/status.svg)](https://cloud.drone.io/dtf-ein/drupal-stack)

# Drupal 8 Stack

Drupal 8 stack running on Apache with MySQL.  
:warning: Only meant for local development.

# Run

Change `drupal_core_owner` in `/vars/play_webserver.yml` to a user on the your system that is a sudoer.

```bash
# Setup your system
ansible-galaxy install -r ./requirements.yml
ansible-playbook play_webserver.xml -i inv_localhost

# Docker container you can use to test
docker run -it -v /path/to/drupal-stack:/root -p 80:80 geerlingguy/docker-ubuntu1804-ansible:latest /bin/bash
```

# Credit

Based on the [geerlingguy/ansible-role-drupal](https://github.com/geerlingguy/ansible-role-drupal).
