Zend Developer Tools
====================

Module providing debug tools for working with the [Zend Framework 2](https://github.com/zendframework/zf2) MVC
layer.

Installation
============

1. Install the module via composer by running:

   ```sh
   composer require zendframework/zend-developer-tools:dev-master
   ```
   or download it directly from github and place it in your application's `module/` directory.
2. Add the `ZendDeveloperTools` module to the module section of your `config/application.config.php`
3. Copy `./vendor/zendframework/zend-developer-tools/config/zenddevelopertools.local.php.dist` to
   `./config/autoload/zenddevelopertools.local.php`. Change any settings in it
   according to your needs.
4. If server version of PHP is lower than 5.4.0 add the following in your `index.php`:
   ```php
   define('REQUEST_MICROTIME', microtime(true));
   ```

   **Note:** The displayed execution time in the toolbar will be highly inaccurate
    if you don't define `REQUEST_MICROTIME` in PHP < 5.4.0.

Extensions
==========

* [BjyProfiler](https://github.com/bjyoungblood/BjyProfiler) - profile `Zend\Db` queries
* [OcraServiceManager](https://github.com/Ocramius/OcraServiceManager) - track dependencies within your application
* [SanSessionToolbar](https://github.com/samsonasik/SanSessionToolbar) - preview Zend\Session data
