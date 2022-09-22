German (DE) language internationalisation Gateway Module for Magento 2.4x
==========================================================================

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