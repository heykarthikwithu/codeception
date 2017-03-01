# Codeception in Drupal
A drupal application with codeception integration.

Initially do a composer update, which would get the drupal codebase locally.

`$ composer update`

Then to get the codeception to be bootstrapped.

`$ php vendor/bin/codecept bootstrap`

Then add the phantoman congifuration in the `codeception.yml` file.
```
extensions:
    enabled:
        - Codeception\Extension\Phantoman
    config:
       Codeception\Extension\Phantoman:
            path: 'vendor/bin/phantomjs'
            port: 4444
            suites: ['acceptance']
```
