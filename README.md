SilverpopBundle
===============

Simple wrapper for the Silverpop PHP API
```
[SilverpopSDK]
    git=git://github.com/smathews/SilverpopPHP.git
    target=/silverpop

[MuriadSilverpopBundle]
    git=git://github.com/smathews/SilverpopBundle.git
    target=/bundles/Muriad/SilverpopBundle

 #app/AppKernel.php
 new Muriad\SilverpopBundle\MuriadSilverpopBundle(),

 #app/autoload.php
    'Muriad'           => __DIR__.'/../vendor/bundles',
    'Silverpop'        => __DIR__.'/../vendor/silverpop/lib',

 #app/config/config.yml
    muriad_silverpop:
      engage_server: %engage_server% 
      username: %engage_user%
      password: %engage_pass%
 
 #app/config/parameters.ini
    engage_server=<engage_server_number>
    engage_user=<email_of_engage_user>
    engage_pass=<users_password>

#Then of course, and a container aware class
    $this->silverpop = $this->container->get('silverpop');

```
