# Arlo Timber
### A Wordpress/Composer framework. Using Timber/Twig for templating

[![GitHub issues](https://img.shields.io/github/issues/asha23/arlo-timber-framework.svg)](https://github.com/asha23/arlo-timber-framework/issues) [![GitHub forks](https://img.shields.io/github/forks/asha23/arlo-timber-framework.svg)](https://github.com/asha23/arlo-timber-framework/network) [![GitHub stars](https://img.shields.io/github/stars/asha23/arlo-timber-framework.svg)](https://github.com/asha23/arlo-timber-framework/stargazers)

This assumes prior knowledge of how to set up WordPress themes. Feel free to make improvements to this.

It's very (very) loosely based on how Bedrock approach things, but with a much more simplified method for differentiating between dev/staging/production databases.

If you like Bedrock, then great! It's pretty awesome, so fill your boots. But if, like me, you find it a little over complicated, then this framework/approach might be more up your alley as I've deliberately tried to keep it all really simple.

You can get up and running with a complete WordPress environment in about a minute.

## Basic installation instructions

* Create a new repository for your project
* Download this as a zip file and unzip into the repository - https://bitbucket.org/this-is-pegasus-team/pegasus-wordpress-composer/get/master.zip
* Open a terminal and browse to the folder you are using
* Install Composer - https://getcomposer.org/
* Install Node - https://nodejs.org/en/
* Install Bower - https://bower.io/
* Install Yarn - https://yarnpkg.com/
* Rename .env-example to .env and fill out the relevant fields.
* Once you have Composer installed, then you need to run ```$ composer install```. This will install all the base plugins and a seed theme into the correct directories.
* Send an initial commit to your repository
* Get started.

You can alternatively create a fork of this framework. If you want the composer file to stay up to date.

Requirements
============

You should get a license for Advanced Custom Fields pro for this framework.

Getting started
===============

There is a Vagrant file in the folder which uses a version of Scotchbox for Vagrant:  
Run ```vagrant up``` from the root folder (Not currently tested) - Your website will then be available on

```
192.168.33.10
```

#### The following information should be used to connect to the database

MySql Host: 127.0.0.1  
Username: root  
Password: root

SSH Host: 192.168.33.10  
SSH User: vagrant  
SSH Password: vagrant  

Alternatively, just use MAMP. Or something like https://www.themejuice.it, which provides an excellent and user-friendly environment for locally developing with WordPress. Or any other method you like for deploying locally.

Vagrant is the recommended method as it keeps everything self contained.

## .env-example file

There is a .env-example file in the root. You should fill out the relevant information in this file and then re-save it as .env. Once you have done this, you can then edit the web/wp-config.php file and add salts, or do other configurations.

There is information for 3 environments contained here, development, production and staging. Filling out this information correctly will make sites easier to deploy as it will auto-detect which database to use depending on your environment.

Add your ACF Pro key to here as well.

## Notes on the .gitignore.

This installation by default ignores everything but your theme. You will need to create a deployment of wordpress on your production environment and run composer install.

If you can't do this simply upload the files as required. I decided to not include all the WordPress stuff in the repo because in the most part it's an uneccesary step really.

Feel free to edit the .gitignore file though if you want to change this.

## Notes about the seed theme

[You can view the seed theme repo here](https://github.com/asha23/wp-seed-timber)

This theme uses Gulp for compilation and Bower for JavaScript dependency management. It is also based around SASS Bootstrap 3.

The main folder structure is as follows:

```
web/content
web/wp
```

The content folder contains all the themes, plugins and files for the front-end.

The wp folder is the base WordPress installation - You should not change anything in here.

### Arlo? What?

Arlo is the name of my son. So this is dedicated to him, the little monster.
