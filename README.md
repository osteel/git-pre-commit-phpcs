# Pre-commit hook for Git running PHP_CodeSniffer

This a basic pre-commit hook for Git running [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) on newly committed changes and offering to fix violations automatically when possible.

## Installation

Download the [pre-commit file](https://raw.githubusercontent.com/osteel/git-pre-commit-phpcs/master/pre-commit) and put it under `.git/hooks` at the root of your project.

Make sure it is executable:

```
$ chmod +x pre-commit
```

Install PHP_CodeSniffer following one of the [suggested methods](https://github.com/squizlabs/PHP_CodeSniffer#installation).

I personally like to install it for the projects that need it only, as a Composer dependency:

```
$ composer require --dev squizlabs/php_codesniffer
```

## Configuration

The default standard is [PSR-12](https://www.php-fig.org/psr/psr-12/), but you can change it by updating the `STANDARD` variable at the top of the file.

Likewise, the script assumes that PHP_CodeSniffer's `bin` folder is at the same level as the `.git` folder by default, but you can set a different location by updating the `BIN` variable.

For other standards and options, please visit the [usage page](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Usage).

## Contribute

While this repository is not intended to grow, PRs are welcome, especially since my Bash-fu isn't very strong.