ansible-role-msmtp
=========

Installs msmtp for sending emails.  
Stores configuration in `$HOME/.msmtprc`

Based on:  
https://marlam.de/msmtp/msmtp.html


On the host just invoke the command:

```
msmtp recipient@yourdomain.com << EOF
Subject:Greetings from yourdomain
Hello everybody!
EOF
```


Requirements
------------

Debian, Ubuntu OS

Role Variables
--------------

Refer to the docs for variable values  
https://marlam.de/msmtp/msmtp.html

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- name: Install msmtp
  hosts: all
  gather_facts: false
  roles:
  - ansible-role-msmtp
  vars:
    msmtp_host: smtp.gmail.com
    msmtp_port: 587
    msmtp_tls_starttls: "on"
    msmtp_user: gmail_user@gmail.com
    msmtp_from: gmail_user@gmail.com
    msmtp_password: secretpass1234
```

License
-------

GNU GPL v3

Author Information
------------------

(c) 2024 Pawel Idzikowski
