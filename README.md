Congruence Standard
===================

Strengthening Congruence between the people, process, and technology of development teams.

Consistency through standards, harmony through self-actualization. A developers guide for creating  
evolutionary and amazing user experiences for desktop, embedded and mobile platforms.

One document at a time.


## Facts

* Version 0.1.0
* [Repository](https://github.com/thedarksociety/congruence-standard/)


## Developer

Rye Miller
 * [Website](https://ryemiller.io)
 * [Twitter](http://twitter.com/ryemiller)
 * [Github](http://github.com/iods)


## License

[GNU General Public License v3.0](http://www.gnu.org/licenses/#GPL)







#ECG Magento Code Sniffer Coding Standard

This is a Fork of https://github.com/magento-ecg/coding-standard

ECG Magento Code Sniffer Coding Standard is a set of rules and sniffs for PHP_CodeSniffer tool.

It allows automatically check your code against some of the common Magento and PHP coding issues, like:

raw SQL queries;
SQL queries inside a loop;
direct instantiation of Mage and Enterprise classes;
unnecessary collection loading;
excessive code complexity;
use of dangerous functions;
use of PHP superglobals;
and many others.

#Installation & Usage

Before starting using our coding standard install PHP_CodeSniffer.

Clone or download this repo somewhere on your computer or install it with Composer. To do so, add the dependency to your composer.json file and run the php composer.phar install command:

{
"require": {
"aoepeople/magento-coding-standard": "dev-master"
}
}
Run CodeSniffer:

phpcs --standard=/path/to/Ecg/standard /path/to/code
#Requirements

PHP 5.4 and up.

Checkout the php-5.3-compatible branch to get the PHP 5.3 version.

#Contribution

Please feel free to contribute new sniffs or any fixes or improvements for the existing ones.


## Copyright

Copyright (C) 2021, Rye Miller

https://github.com/magento/magento-coding-standard
Magento Coding Standard
A set of Magento rules for PHP_CodeSniffer tool.

Installation within a Magento 2 site
To use within your Magento 2 project you can use:

composer require --dev magento/magento-coding-standard
Due to security, when installed this way the Magento standard for phpcs cannot be added automatically. You can achieve this by adding the following to your project's composer.json:

"scripts": {
"post-install-cmd": [
"([ $COMPOSER_DEV_MODE -eq 0 ] || vendor/bin/phpcs --config-set installed_paths ../../magento/magento-coding-standard/)"
],
"post-update-cmd": [
"([ $COMPOSER_DEV_MODE -eq 0 ] || vendor/bin/phpcs --config-set installed_paths ../../magento/magento-coding-standard/)"
]
}
Installation for development
You can install Magento Coding Standard by cloning this GitHub repo:

git clone git@github.com:magento/magento-coding-standard.git
cd magento-coding-standard
composer install
It is possible also to install a standalone application via Composer

composer create-project magento/magento-coding-standard --stability=dev magento-coding-standard
Verify installation
Command should return the list of installed coding standards including Magento2.

vendor/bin/phpcs -i
Usage
Once installed, you can run phpcs from the command-line to analyze your code MyAwesomeExtension

vendor/bin/phpcs --standard=Magento2 app/code/MyAwesomeExtension
Fixing issues automatically
Also, you can run phpcbf from the command-line to fix your code MyAwesomeExtension for warnings like "PHPCBF CAN FIX THE [0-9]+ MARKED SNIFF VIOLATIONS AUTOMATICALLY"

vendor/bin/phpcbf --standard=Magento2 app/code/MyAwesomeExtension
Contribution
See the community contribution model.

Where to contribute
Documentation of existing rules. See ExtDN PHP CodeSniffer rules for Magento 2 as a good example.
Bug fixes and improvements of existing rules.
Creation of new PHP CodeSniffer rules.
Discussions on new rules (through periodic hangouts or discussions per GitHub issue).
How to contribute
Start with looking into Community Dashboard. Any ticket in Up for grabs is a good candidate to start.
Didn't satisfy your requirements? Create one of three types of issues:
Bug report - Found a bug in the code? Let us know!
Existing rule enhancement - Know how to improve existing rules? Open an issue describe how to enhance Magento Coding Standard.
New rule proposal - Know how to improve Magento ecosystem code quality? Do not hesitate to open a proposal.
The issue will appear in the Backlog column of the Community Dashboard. Once it will be discussed and get accepted label the issue will appear in the Up for grabs column.
Testing
All rules should be covered by unit tests. Each Test.php class should be accompanied by a Test.inc file to allow for unit testing based upon the PHP_CodeSniffer parent class AbstractSniffUnitTest. You can verify your code by running

vendor/bin/phpunit
Also, verify that the sniffer code itself is written according to the Magento Coding Standard:

vendor/bin/phpcs --standard=Magento2 Magento2/ --extensions=php
License
Each Magento source file included in this distribution is licensed under the OSL-3.0 license.

Please see LICENSE.txt for the full text of the Open Software License v. 3.0 (OSL-3.0).
