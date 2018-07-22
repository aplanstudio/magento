### Installation

The following stpes will get through Magento's installcation via command line.

##### Part 1: Getting started

###### Preparation:
1. Required `composer` the PHP dependency manager ([GetComposer](https://getcomposer.org/))
2. [Get your authentication keys](https://devdocs.magento.com/guides/v2.0/install-gde/prereq/connect-auth.html), Will use `Public key` as username and `Private key` as password during the installation.

Get the Magento Software, using `composer` as follows:

```
cd <web server docroot directory>
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition magento2
```

##### Part 2: Installing the Magento software

The following example shows how to install using the command line with the following options:

- The Magento software is installed in the `/var/www/html/magento2` directory, which means your storefront URL is http://locahost/magento2/
- The database server is on the same host as the web server. The database name is `magento2`, and the username and password are both `magento2`

```
php /var/www/html/magento2/bin/magento setup:install --base-url=http://localhost/magento2/ \
--db-host=localhost --db-name=magento2 --db-user=magento2 --db-password=magento2 \
--admin-firstname=Magento --admin-lastname=User --admin-email=user@example.com \
--admin-user=admin --admin-password=admin123 --language=en_US \
--currency=USD --timezone=Asia/Bangkok --use-rewrites=1
```
