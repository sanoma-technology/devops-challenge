# Sanoma Devops Challenge

## Goal
Create a [Vagrant](https://www.vagrantup.com/) setup that runs a default
[Mezzanine](http://mezzanine.jupo.org/) site. Running `vagrant up` should bring
up a fully configured machine, running a empty *Mezzanine* project. The machine
should run *Apache* + *mod_wsgi* or *Ngnix* + *Gunicorn*. Use *sqlite* as the
database.

## Tasks
* Fork the repo on GitHub.
* Add a `Vagrantfile` to the repo, that brings up a machine with
  [this image](https://s3-eu-west-1.amazonaws.com/snm-nl-hostingsupport-test/vagrant-centos-6-4.box),
  and the hostname `sanoma.local`. Make sure *Vagrant* provisions the machine
  using *Puppet*.
* Add a `deploy` directory to the repo. Add the nessecary files to this
  directory, so that provisioning does at least the following things:
  * Creates an user called `sanoma` with the password `devops`.
  * Installs the source code using `pip`.
  * Creates an *Mezzanine* project in the home directory of the `sanoma` user.
  * Overrides the `local_settings.py` file in the *Mezzanine* project with
    sensible settings.
  * Installs and configures *Apache* + *mod_wsgi* or *Ngnix* + *Gunicorn*.
* Commit and push your changes back to your fork on GitHub.

## Hints
* To install *Mezzanine* using *pip*, add the *EPEL* repo to your *Yum*
  configuration.
* You will probably need the `python-devel` Yum package.
