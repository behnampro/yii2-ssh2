SSH2 library for yii2
============

[![Latest Stable Version](https://poser.pugx.org/ourren/yii2-ssh2/v/stable)](https://packagist.org/packages/ourren/yii2-ssh2) [![Total Downloads](https://poser.pugx.org/ourren/yii2-ssh2/downloads)](https://packagist.org/packages/ourren/yii2-ssh2) [![Latest Unstable Version](https://poser.pugx.org/ourren/yii2-ssh2/v/unstable)](https://packagist.org/packages/ourren/yii2-ssh2) [![License](https://poser.pugx.org/ourren/yii2-ssh2/license)](https://packagist.org/packages/ourren/yii2-ssh2)


Pure PHP library widget (based on phpseclib) for Yii2.

modified for integrity and fix confilict with Yii2

by : Behnam mirzaee


## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
composer require behnampro/yii2-ssh2 "*"
```

or add

```
"behnampro/yii2-ssh2": "*"
```

to the require section of your `composer.json` file.


## Usage

### Example

```
use behnampro\yii2ssh\Yii2ssh;

$yii_ssh = new Yii2ssh();
$host = "127.0.0.1";
$auth['username'] = 'admin';
$auth['password'] = 'password';
if($yii_ssh->connect($host, $auth))
{
    $yii_ssh->run_ssh([
        'ls -al',
    ], function($line) {
        echo $line;
    });
}
```

## Ref
The project is modified based on [thelfensdrfer/yii2sshconsole](https://github.com/thelfensdrfer/yii2sshconsole)