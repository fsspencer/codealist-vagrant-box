# Codealist Vagrant Box 
This is a simple vagrant box initially created for Magento 2 usages. It has been built using PuPHPet with a couple of modifications and agregations to it.
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
Clone the repository 
>git clone https://github.com/fsspencer/codealist-vagrant-magento2 

Turn on your vagrant box
>vagrant up

You can make any change you want within the puphpet/config.yaml file, after you modify it you need to provision your vagrant box by executing the following:
>vagrant provision

Once you get your vagrant initialized, go to your web browser and enter the following URL:
>http://local.codealist.net

The output should be a phpinfo()
## Add a new site
Within your local environment (NOT the vagrant box) execute the following
>sh addsite

This script will ask you for a couple of parameters in order to create a new virtual host in your vagrant box, after that it will reload and provision it by creating your new site.

Your project code will be located in the directory projects/[YOUR-SITE-URL].

After that you need to login via ssh to your vagrant and add your database.
## Paramters
- **IP:** 192.168.56.101
- **HOSTNAME:** local.codealist
- **RAM:** 4096
- **CPUS:** 2
- **SSH PORT:** 22
- **MYSQL ROOT PWD:** root

## Credits
Francis S. Spencer - https://codealist.net/