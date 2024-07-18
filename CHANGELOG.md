# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## Releases

### [0.1.3] - 2024-07-18

* Upgrading phpstan/phpstan (1.9.4 => 1.11.7)
* Upgrading friendsofphp/php-cs-fixer (v3.13.1 => v3.59.3)
* Upgrading ixnode/bash-version-manager (0.1.3 => 0.1.8)
* Upgrading phpmd/phpmd (2.13.0 => 2.15.0)
* Upgrading phpunit/phpunit (9.5.27 => 9.6.20)
* Upgrading povils/phpmnd (v3.0.1 => v3.5.0)
* Upgrading rector/rector (0.15.1 => 0.15.25)

### [0.1.2] - 2024-07-18

* Add more CHANGELOG.md examples
* Add CHANGELOG.md badges
* Fix namespace within test
* Add version output to test scripts

### [0.1.1] - 2022-12-19

* Fix PSR-4 Autoloading Standard

### [0.1.0] - 2022-12-18

* Initial release
* Add src
* Add tests
  * PHP Coding Standards Fixer
  * PHPMND - PHP Magic Number Detector
  * PHPStan - PHP Static Analysis Tool
  * PHPUnit - The PHP Testing Framework
  * Rector - Instant Upgrades and Automated Refactoring
* Add README.md
* Add LICENSE.md

## Add new version

```bash
# Checkout master branch
$ git checkout main && git pull

# Check current version
$ vendor/bin/version-manager --current

# Increase patch version
$ vendor/bin/version-manager --patch

# Change changelog
$ vi CHANGELOG.md

# Push new version
$ git add CHANGELOG.md VERSION && git commit -m "Add version $(cat VERSION)" && git push

# Tag and push new version
$ git tag -a "$(cat VERSION)" -m "Version $(cat VERSION)" && git push origin "$(cat VERSION)"
```
