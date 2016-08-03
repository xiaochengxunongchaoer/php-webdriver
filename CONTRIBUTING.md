# Contributing to php-webdriver

We love to have your help to make php-webdriver better!
 
Feel free to open an [issue](https://github.com/facebook/php-webdriver/issues) if you run into any problem, or
send a pull request (see bellow) with your contribution.

## Workflow when contributing a patch

1. Fork the project on GitHub
2. Implement your code changes into separate branch
3. Make sure all PHPUnit tests passes (see below). We also have Travis CI build which will automatically run tests on your pull request).
4. When implementing notable change, fix or a new feature, add record to Unreleased section of [CHANGELOG.md](CHANGELOG.md)
5. Submit your [pull request](https://github.com/facebook/php-webdriver/pulls) against community branch
 
Note before any pull request can be accepted, a [Contributors Licensing Agreement](http://developers.facebook.com/opensource/cla) must be signed.

When you are going to contribute, please keep in mind that this webdriver client aims to be as close as possible to other languages Java/Ruby/Python/C#.
FYI, here is the overview of [the official Java API](http://seleniumhq.github.io/selenium/docs/api/java/)

### Run unit tests

There are two test-suites: one with unit tests only, second with functional tests, which require running selenium server.

To execute all tests simply run:

    ./vendor/bin/phpunit

If you want to execute just the unit tests, run:

    ./vendor/bin/phpunit --testsuite unit
    
For the functional tests you must first download and start the selenium server, then run the `functional` test suite:

    java -jar selenium-server-standalone-2.48.2.jar -log selenium.log &
    ./vendor/bin/phpunit --testsuite functional