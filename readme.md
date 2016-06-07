# Generic Vagrant
I got tired of copying vagrant files all over for my many projects. This
basically extracts Vagrantfile as a single ruby script to be included,
perhaps by cloning a git submodule.

## Setting it Up

First we set the project as a submodule in our current project

```bash
git submodule add git@github.com:jamescarr/generic-vagrant.git

```

Next up we create `Vagrantfile in the root of our project with this in
it.

```ruby
# -*- mode: ruby -*-
# vi: set ft=ruby :
require_relative 'generic-vagrant/vagrant'

```

Create an ansible directory for ansible that looks like this:

```
ansible
├── ansible.cfg
├── main.yml
├── requirements.yml
└── roles

```

And that's it! Godspeed!



