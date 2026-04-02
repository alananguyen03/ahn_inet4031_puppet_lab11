#Lab 11: Configuration as Code (CaC)

## Overview
This lab uses Puppet to manage users and groups on a system and deploy a LAMP stack (Apache, PHP, MariaDB). 

## Files

### lamp_stack_server.pp
Installs and configures LAMP stack, including:

-Apache
-PHP (php, libapache2-mod-php, php-cli, php-mysql) 
-MariaDB

Also deploys a PHP test page to verify the LAMP stack is working.

### phpinfo.php 
A simple PHP test file to verify PHP installation.

### server_users_groups.pp 
Creates and manages users, groups, and home directories. Users and groups included:

- Groups: group1, group2  
- Users: user04, user05, user06, user07 

Passwords are hashed, and managehome automatically creates home directories.

### testing_puppet.pp
A basic Puppet test file.

## How to Run
To apply the Puppet manifest on the server, run the following: 

1. Apply the users and groups manifest:
-sudo puppet apply server_users_groups.pp

2. Apply the LAMP stack manifest:
-sudo puppet apply lamp_stack_server.pp
