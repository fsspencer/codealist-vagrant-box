# Codealist Vagrant Box 
This is a simple vagrant box initially built using PuPHPet with a couple of modifications and agregations to it.
## Specifications
- Nginx
- PHP 7.0
- PHP Extensions: curl, intl, xml, gd, mcrypt, mbstring, zip, soap, mysql, dom
- MariaDB
- XDebug
- NodeJS
- Grunt / Gulp
- ElasticSearch

## Usage
1 - Clone the repository 
>git clone https://github.com/fsspencer/codealist-vagrant-magento2 

2 - Copy the ./puphpet/config.yaml.sample to ./puphpet/config.yaml

3 - Turn on your vagrant box
>vagrant up

4 - You can make any change you want within the puphpet/config.yaml file, after you modify it you need to provision your vagrant box by executing the following:
>vagrant provision

5 - Once you get your vagrant initialized, go to your web browser and enter the following URL:
>http://local.codealist.net

The output should be a phpinfo()
## Add a new site
Within your local environment (NOT inside your vagrant box) execute the following
>./add-site

This script will ask you for a couple of parameters in order to create a new virtual host in your vagrant box, after that it will reload and provision it by creating your new site.

####Optional Features:
- Download project from Git repository
- Create empty database
- Create and import SQL database

Your project code will be located in the directory projects/**[YOUR-SITE-URL]**.

## Create Project
Within your local environment (NOT inside your vagrant box) execute the following
>./create-project

This script will create an empty project by giving you the following options:

- Empty Project
- Magento Open Source 2
- Magento Commerce 2
- Laravel
- Wordpress
- Slim
- Symfony

Your project code will be located in the directory projects/local.**project-name**.com.

It will also create a database named as your project.
## Parameters
- **IP:** 192.168.56.101
- **HOSTNAME:** local.codealist
- **RAM:** 4096
- **CPUS:** 2
- **SSH PORT:** 22
- **MYSQL ROOT PWD:** root

## Credits
Francis S. Spencer - https://codealist.net/