# PHP Naming Conventions

[![Release](https://img.shields.io/github/v/release/ixnode/php-naming-conventions)](https://github.com/ixnode/php-naming-conventions/releases)
[![](https://img.shields.io/github/release-date/ixnode/php-naming-conventions)](https://github.com/ixnode/php-naming-conventions/releases)
![](https://img.shields.io/github/repo-size/ixnode/php-naming-conventions.svg)
[![PHP](https://img.shields.io/badge/PHP-^8.2-777bb3.svg?logo=php&logoColor=white&labelColor=555555&style=flat)](https://www.php.net/supported-versions.php)
[![PHPStan](https://img.shields.io/badge/PHPStan-Level%20Max-777bb3.svg?style=flat)](https://phpstan.org/user-guide/rule-levels)
[![PHPUnit](https://img.shields.io/badge/PHPUnit-Unit%20Tests-6b9bd2.svg?style=flat)](https://phpunit.de)
[![PHPCS](https://img.shields.io/badge/PHPCS-PSR12-416d4e.svg?style=flat)](https://www.php-fig.org/psr/psr-12/)
[![PHPMD](https://img.shields.io/badge/PHPMD-ALL-364a83.svg?style=flat)](https://github.com/phpmd/phpmd)
[![Rector - Instant Upgrades and Automated Refactoring](https://img.shields.io/badge/Rector-PHP%208.2-73a165.svg?style=flat)](https://github.com/rectorphp/rector)
[![LICENSE](https://img.shields.io/github/license/ixnode/php-api-version-bundle)](https://github.com/ixnode/php-api-version-bundle/blob/master/LICENSE)

> This library translate a given string or convention into another convention.
> The following conventions are supported:

| Convention     | Representation         |
|----------------|------------------------|
| `raw`          | A raw string           |
| `words`        | ['a', 'raw', 'string'] |
| `title`        | A Raw String           |
| `pascalCase`   | ARawString             |
| `camelCase`    | aRawString             |
| `under_scored` | a_raw_string           |
| `config`       | a.raw.string           |
| `constant`     | A_RAW_STRING           |

## Installation

```bash
composer require ixnode/php-naming-conventions
```

```bash
vendor/bin/php-naming-conventions -V
```

```bash
php-naming-conventions 0.1.0 (12-18-2022 01:17:26) - Björn Hempel <bjoern@hempel.li>
```

## Usage

```php
use Ixnode\PhpNamingConventions\NamingConventions;
```

```php
$rawString = 'Group Private';

print (new NamingConventions($rawString))->getTitle();
// (string) Group Private

print (new NamingConventions($rawString))->getPascalCase();
// (string) GroupPrivate

print (new NamingConventions($rawString))->getCamelCase();
// (string) groupPrivate

print (new NamingConventions($rawString))->getUnderscored();
// (string) group_private

print (new NamingConventions($rawString))->getConstant();
// (string) GROUP_PRIVATE

print (new NamingConventions($rawString))->getConfig();
// (string) group.private

print (new NamingConventions($rawString))->getSeparated();
// (string) group-private

print (new NamingConventions($rawString))->getRaw();
// (string) Group Private

print (new NamingConventions($rawString))->getWords();
// (array) [[0] => group, [1] => private]
```

## Development

```bash
git clone git@github.com:ixnode/php-naming-conventions.git && cd php-naming-conventions
```

```bash
composer install
```

```bash
composer test
```

## License

This tool is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details