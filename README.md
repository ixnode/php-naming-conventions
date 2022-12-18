# PHP Naming Conventions

This library translate a given string or convention into another convention.
The following conventions are supported:

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
use Ixnode\NamingConventions\NamingConventions;
```

```php
$pascalCase = (new NamingConventions($rawString))->getPascalCase();
```

## License

This tool is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details