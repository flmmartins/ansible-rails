ansible-rails
========

Clone your repo, install your gems (including rails) and run rake

Requirements
------------


* Make a bundle file with all your gems and ansible will install them for you. Make sure to add gem 'thin' to it

* Also make your Rake file so the rake tasks will work

* Edit the task/repo.yml and add your repository (where the bundle file and all is). Your repository will be cloned so you need to authorize your machine to clone from that repo

Role Variables
--------------

app_path: The destination folder for your cloned repository. Ansible will create that folder

user: The machine user in which you are going to clone the repository


Inside defaults:

rails_env: Is set to production - if you wanna to change this be sure to check rake.yml to correct a failure check in the playbook
port: Your rail server port

Dependencies
------------

Check my repository for ruby, database and more installation

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: ansible-rails, app_path: blabla, port: 4567 }


Author Information
------------------

Fernanda Martins (flmmartins@gmail.com)
LinkedIn: https://www.linkedin.com/in/flmmartins
