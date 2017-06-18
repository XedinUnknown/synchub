## Overview
This repository tracks changes for [SyncHub].

## What's Involved
1. This project is based on [Bedrock]. Therefore,
its code is managed by [Git] and [Composer].
This is why there is no [WordPress], or plugin/theme code here: these are all
merely **dependencies** of this project, and are automatically and recursively
installed at their most appropriate for the environment versions.
2. This project uses [Capistrano] for deployment, and relevant configs are
derived from the [bedrock-capistrano] project.
3. For local development server, this projetct derives relevant configuration
from [ScotchBox], albeit slightly modifying it to cater for specifics.

## Local Setup

1. Install [Git](https://git-scm.com/downloads);

This is the version control software used to manage this project's code.
Installing this on Windows will also install [Git Bash], which is a Unix shell
emulator. If you're on Windows, every time you are told to run something in [CLI],
this is what you should use.

2. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads);

This allows bringing up a virtual server locally, on your computer, and run the website inside it.

3. Install [Vagrant](https://www.vagrantup.com/downloads.html);

Vagrant is a way to configure and manage virtual environments.

4. [Clone](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#_git_cloning) this repository;

This will download the project files to your computer.

5. In the project's folder, run `composer update` in [CLI];

This will install project dependencies. It can take some time to download WordPress.

6. In the project's folder, run [`vagrant up`](https://www.vagrantup.com/docs/cli/up.html) in [CLI];

This may take 15 minutes the first time, due to Vagrant downloading the virtual image.

7. Navigate to [192.168.33.10](http://192.168.33.10/) in your browser;

The first time WordPress installation steps would need to be completed.

## Deployment
This project includes configuration files that allow very easy, atomic,
and reversible deployments. Therefore, in order to deploy this project,
[Capistrano] is required, and in turn requires [Ruby]. It can take some time and
effort to configure everything the first time. Due to this, it is recommended
to leave the development and deployment of this project to a professional.

1. Install [Ruby](https://www.ruby-lang.org/en/documentation/installation);
2. Install [Bundler];
3. Install project dependencies by running `bundle install`, which will install [Capistrano], among other things;
4. Run `bundle exec cap production deploy` to deploy, which will ask for SSH password.

[SyncHub]:                              http://synchub.org
[Git]:                                  https://git-scm.com/
[Git Bash]:                             https://superuser.com/a/1053657/268433
[Bedrock]:                              https://github.com/roots/bedrock
[Composer]:                             https://getcomposer.org/
[Ruby]:                                 https://www.ruby-lang.org
[Capistrano]:                           http://capistranorb.com/
[Bundler]:                              http://bundler.io/
[WordPress]:                            https://wordpress.org/
[bedrock-capistrano]:                   https://github.com/roots/bedrock-capistrano
[ScotchBox]:                            https://box.scotch.io/

[CLI]:                                  https://en.wikipedia.org/wiki/Command-line_interface
