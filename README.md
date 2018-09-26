ec2-iam-role
=========

Create AWS EC2 IAM roles to utilise the IAM permissions system in AWS

Requirements
------------

boto is required for this role

Role Variables
--------------

template_dir specifies the directory containing your templates. In here, you should have:
  - role document
  - policy document

These are then referenced in the iam_templates dict.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      vars:
        template_dir: "{{ playbook_dir }}/templates/"
        iam_templates:
          - role: ec2-default-role.json
            policy: ec2-default-policy.json
            name: ec2-default
            managed: []
            type: role
      roles:
         - { role: ec2-iam-role }

License
-------

GPL

Author Information
------------------

Iain M. Conochie <iain@shihad.org>
