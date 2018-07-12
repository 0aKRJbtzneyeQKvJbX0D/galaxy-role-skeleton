## galaxy-role-skeleton

[![Travis CI](http://img.shields.io/travis/csteel/ansible-rolegalaxy-role-skeleton/default.svg?style=flat)](http://travis-ci.org/csteel/ansible-rolegalaxy-role-skeleton/default)
[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20ubuntu-lightgrey.svg?style=flat)](#)

This is a drop in replacement role skeleton used to create ansible roles with the ansible-galaxy command. Customization is done by modifying files and/or [Jinja2](http://jinja.pocoo.org/) templates found in `skeleton` directory.

## Requirements

- Ansible
- Python

## Recommended

Running Ansible in a virtual environment allows for a lot of testing flexibility.

* [skeleton/docs/ansible-setup](skeleton/docs/ansible-setup.md)

## Variables

List of internal variables used by the generated role:

    fact_controller_home
    fact_controller_user

#### Role Name

##### Roles long name

Used as the roles repository name in cases where you have a single role per repository.

```shell
ansible-role-fetch
```

##### Roles short name

Name used when cloning a single role repository locally. The *short name* for our role in this example is:

```shell
fetch
```

using one of the following methods:

You can replace the default ansble-galaxy role skeleton or point to this one using the ansible-galaxy ROLE_SKELETON option.

#### To use as an alternative role skeleton

```shell
ansible-galaxy init --role-skeleton=ALTERNATIVE_ROLE_SKELETON_PATH new_role_short_name
```

Real world example:

```shell
mkdir ~/projects
cd ~/projects
git clone git@github.com:cjsteel/galaxy-role-skeleton.git
ansible-galaxy init --role-skeleton=~/projects/galaxy-role-skeleton/skeleton -f fetch -vvv
```

#### Replacing the ansible galaxy default role skeleton

```shell
cd ~/miniconda2/envs/ansible/lib/python2.7/site-packages/ansible/galaxy/data/default
mv default default.org
git clone git@github.com:cjsteel/galaxy-role-skeleton.git default
```

### Authors and license

- [Christopher Steel](http://mcin-cnim.ca/) | [e-mail](mailto:christopher.steel@mcgill.ca)

License: [MIT](https://tldrlegal.com/license/mit-license)

### Open Science

The Neuro has adopted the principles of Open Science. We are inspired by the likes of the Allen Institute for Brain Science, the National Institutes of Health's Human Connectome project, and the Human Genome project. For additional information please see [open science at the neuro](https://www.mcgill.ca/neuro/open-science-0).

![MCIN](skeleton/imgs/mcin-logo-brain-140x116.png)          ![neuro](skeleton/imgs/neuro-logo-160x116.png)  

