# Sanoma Devops Challenge

## Goal
Create a vagrant setup that runs a default mezzanine site. Running vagrant up should bring up a fully configured machine, running a empty mezzanine project. The machine should run apache + mod_wsgi or ngnix + gunicorn. Use sqlite as the database.

## Tasks
* Fork the repo on github.
* Add a ‘VagrantFile’ to the repo, that brings up a machine with this image, and the hostname ‘sanoma.local’. Make sure vagrant provisions the machine using puppet.
* Add a ‘deploy’ directory’ to the repo. 
* Add the nessecary files to the repo, so that provisioning does at least the following things:
  * Creates an user called ‘sanoma’ with the password ‘devops’.
  * Installs the checkout using ‘pip’.
  * Creates an mezzanine project in the home folder of the ‘sanoma’ user.
  * Overrides the ‘local_settings.py’ file in the mezzanine project with
  * Installs and configures apache + mod_wsgi or ngnix + gunicorn.
  * Commit and push your changes back to your fork on github.

## Hints
* To install mezzanine using pip, add the epel repo to your yum configuration.
* You will probably need the python-devel yum package.
