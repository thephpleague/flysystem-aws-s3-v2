# Flysystem Adapter for AWS S3 SDK v2

[![Author](http://img.shields.io/badge/author-@frankdejonge-blue.svg?style=flat-square)](https://twitter.com/frankdejonge)
[![Build Status](https://img.shields.io/travis/thephpleague/flysystem-aws-s3-v2/master.svg?style=flat-square)](https://travis-ci.org/thephpleague/flysystem-aws-s3-v2)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/thephpleague/flysystem-aws-s3-v2.svg?style=flat-square)](https://scrutinizer-ci.com/g/thephpleague/flysystem-aws-s3-v2/code-structure)
[![Quality Score](https://img.shields.io/scrutinizer/g/thephpleague/flysystem-aws-s3-v2.svg?style=flat-square)](https://scrutinizer-ci.com/g/thephpleague/flysystem-aws-s3-v2)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Packagist Version](https://img.shields.io/packagist/v/league/flysystem-aws-s3-v2.svg?style=flat-square)](https://packagist.org/packages/league/flysystem-aws-s3-v2)
[![Total Downloads](https://img.shields.io/packagist/dt/league/flysystem-aws-s3-v2.svg?style=flat-square)](https://packagist.org/packages/league/flysystem-aws-s3-v2)


## Installation

```bash
composer require league/flysystem-aws-s3-v2
```

## Usage

```php
use Aws\S3\S3Client;
use League\Flysystem\AwsS3v2\AwsS3Adapter;
use League\Flysystem\Filesystem;

$client = S3Client::factory(array(
    'key'    => '[your key]',
    'secret' => '[your secret]',
    'region' => '[aws-region]',
));

$adapter = new AwsS3Adapter($client, 'bucket-name', 'optional-prefix');

$filesystem = new Filesystem($adapter);
```
