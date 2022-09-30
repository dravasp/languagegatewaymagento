German (DE) language internationalisation Gateway Module for Magento 2.4x
==========================================================================

[![GitHub issues](https://img.shields.io/github/issues/dravasp/languagegatewaymagento?logo=github&style=flat-square)](https://github.com/dravasp/languagegatewaymagento/issues)
[![GitHub forks](https://img.shields.io/github/forks/dravasp/languagegatewaymagento?logo=github&style=flat-square)](https://github.com/dravasp/languagegatewaymagento/network)
[![GitHub stars](https://img.shields.io/github/stars/dravasp/languagegatewaymagento?logo=github&style=flat-square)](https://github.com/dravasp/languagegatewaymagento/stargazers)
![Amazon Web Services on Bitnami](https://img.shields.io/badge/Adobe%20Magento%20Commerce-on%20awsCloud%20Bitnami-blue)
![Github language](https://img.shields.io/github/languages/code-size/dravasp/languagegatewaymagento?style=flat-square)
![Packagist](https://img.shields.io/packagist/dt/dravasp/languagegatewaymagento?style=flat-square)
![Packagist](https://img.shields.io/packagist/stars/dravasp/languagegatewaymagento?style=flat-square)
![YouTube Channel](https://img.shields.io/youtube/channel/subscribers/UCZ4IFVouPuErDC8aq4KyFIQ)
![Github Followers](https://img.shields.io/github/followers/dravasp?style=social)
![Brand Website](https://img.shields.io/website?down_color=not%20running&down_message=site%20under%20maintainence&style=flat-square&up_message=active%20and%20running&url=https%3A%2F%2Fweskyprint.com)

Making en_DE (German) Language available to Magento 2.4x Bitnami

Install using SSH
```
cd /opt/bitnami/magento
composer require dravasp/languagegatewaymagento:dev-master
sudo magento-cli setup:upgrade
```

Login to Magento Admin > Sotres > Configuration > Locale Options > Locale > Select (Any One) German (Austria) / German (Germany) / German (Switzerland)

Instructions:
==================

[] Allows Magento Bitnami users to change Locale to German

[] Enabling the module and configuring it with your Magento Installation
  - Login to your Magento Admin and go to Magento Admin > Sotres > Configuration > Locale Options > Locale > Select (Any One) German (Austria) / German (Germany) / German (Switzerland)
   
[] You will now be able to integrate German (DE) language internationalisation Gateway Module with your existing Bitnami Magento Installation of Choice.

Benefits of German (DE) language internationalisation Gateway Module as opposed to standard Integration - 
```
Get an pre-defined Locale Option for Scalable Installation on AWS
```

[] Install using `composer require dravasp/languagegatewaymagento:dev-master`
  - Please Do Not Run composer with sudo or install in project root directory / Please Do Not Upload Static Files to Webserver.
  - Request Integration Support or Seek Guidance from Repo Maintainers
   
```
  - BASE_Locale - en_DE (Currently Enabled)
```
  - For Testing File Integrity checksum 
		md5 <filename>

  - Example
	```
	md5 /opt/bitnami/magento/var/log/system.log
	```
	inside SSH Terminal to provide verification to VAS Team
 
  Uninstall
```	
	sudo magento-cli module:disable ActionOne_LanguageGateway
	composer remove dravasp/languagegatewaymagento
	sudo magento-cli setup:upgrade
	sudo magento-cli module:status
```	

  Hard Delete an Plugin / Extension
```
	sudo nano /bitnami/magento/app/etc/config.php
	Page Down to ActionOne_LanguageGateway
	Delete and make sure there are no trailing spaces
	CTRL/CMD + X and Click Y to Save without Renaming the file
```
```	composer dump-autoload
	sudo magento-cli setup:upgrade
```
```	Wait for a few minutes RUN command
	sudo /opt/bitnami/ctlscript.sh restart
	Wait for a few minutes and Re-check
```
