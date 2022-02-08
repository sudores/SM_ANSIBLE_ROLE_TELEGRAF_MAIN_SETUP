gorobchenkoa.telegraf_main_setup
=========
Main telegraf setup after installation

Requirements
------------


Role Variables
--------------
telegraf_tags - dictionary of variable key is used as tag name, value usead as tag value
`env` - environment metrics tag specified separetely and is obligatory
e.g.:
```yaml
telegraf_tags:
  nginx: true
  tomcat: false

```

Dependencies
------------
this role is dependent on:
- gorobchenkoa.telegraf_installation

Example Playbook
----------------
```yaml
- hosts: all
  roles:
     - role: gorobchenkoa.telegraf_main_setupe
       env: production
       telegraf_tags:
         type: mysql
         smiddle: rec
```
License
-------

BSD
