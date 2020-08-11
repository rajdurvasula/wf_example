# wf_example

This is a ansible automation project to setup Wildfly Application Server

## Roles
Following ansible roles are defined in this project.

- wf_prereqs
- setup_wildfly
- teardown_wildfly
- sample_app

### wf_prereqs
This role installs of pre-requisite OS packages.
- vim editor
- git
- OpenJdk 1.8.0
- apache maven

#### variables
Following variables are used by this role:
- Path: vars/main.yml
- Variables:
  - packages.*

### setup_wildfly
This role installs wildfly application server, configures basic wildfly settings.

#### variables
Following variables are used by this role:
- Path: vars/main.yml
- Variables:
  - wf.*
  - tmp_home_dir
  - enable_firewall

### teardown_wildfly
This role removes wildfly application server and related files.

#### variables

- Path: vars/main.yml
- Variables:
  - wf.*
  - enable_firewall

### sample_app
This role installs sample web application on wildfly application server.

####  variables

- Path: vars/main.yml
- Variables:
  - sample_app.*
