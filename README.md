# Pre-commit hook for Git running PHP_CodeSniffer

This a basic pre-commit hook for Git running [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) on newly committed changes and offering to fix violations automatically when possible.

## Installation

Download the [pre-commit file](https://github.com/osteel/git-pre-commit-phpcs/blob/master/pre-commit) and put it under `.git/hooks` at the root of your project.

Make sure it is executable:

```
$ chmod +x pre-commit
```

Install PHP_CodeSniffer as a Composer dependency:

```
$ composer require --dev squizlabs/php_codesniffer
```

## Configuration

The default standard is [PSR-12](https://www.php-fig.org/psr/psr-12/), but you can change it by updating the `STANDARD` variable at the top of the file.

Likewise, as the `vendor` folder isn't always at the same level as the `.git` folder, you can change its location by updating the `DIR` variable.

For other standards and options, please visit the [usage page](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Usage).
