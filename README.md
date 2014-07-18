joshuaestes/magento-vagrant
===========================

This repository is for quickly setting up a magento installation on a vagrant
box.

# Requirements

* [Virtual Box](https://www.virtualbox.org/)
* [Vagrant](http://www.vagrantup.com/)

# Installation

You will need to update your hosts file, make sure you add `www.localhost.com`
to use 127.0.0.1

```conf
# /etc/hosts
127.0.0.1	localhost   www.localhost.com
```

```bash
git clone https://github.com/JoshuaEstes/magento-vagrant.git
cd magento-vagrant
curl -sS https://getcomposer.org/installer | php
php composer.phar install
vagrant up
php bin/phing vagrant:mage:install
```

Next, open up your browser to http://www.localhost.com:8080

# Configuration

You can edit `n98-magerun.yaml` to change some of the default settings.
