---
title: Checking PHP ini and version file via CLI or file script
date: 2020-04-23 21:36:06
tags:
  - bytesize
  - php
category:
  - codes
---

<img src="/images/posts/20200424/anas-alshanti-feXpdV001o4-unsplash.jpg" title="Photo by Anas Alshanti on Unsplash" alt="Photo by Anas Alshanti on Unsplash" style="width: 500px" />
<span>Photo by <a href="https://unsplash.com/@otenteko?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Anas Alshanti</a> on <a href="/s/photos/cli?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

There are instances that your cli and your file script are having different PHP loaded.

Here are some of the ways to quickly check it out.

## `php.ini` file location

In CLI:

```shell
php --ini

# Configuration File (php.ini) Path: /usr/local/etc/php/7.2
# Loaded Configuration File:         /usr/local/etc/php/7.2/php.ini
# Scan for additional .ini files in: /usr/local/etc/php/7.2/conf.d
# Additional .ini files parsed:      /usr/local/etc/php/7.2/conf.d/ext-opcache.ini,
# /usr/local/etc/php/7.2/conf.d/php-memory-limits.ini
```

In file script:

```php
<?php

var_dump("PHP Ini: " . php_ini_loaded_file())
```

## PHP version

In CLI:

```shell
php --version

# PHP 7.2.24 (cli) (built: Oct 25 2019 11:13:56) ( NTS )
# Copyright (c) 1997-2018 The PHP Group
# Zend Engine v3.2.0, Copyright (c) 1998-2018 Zend Technologies
#     with Zend OPcache v7.2.24, Copyright (c) 1999-2018, by Zend Technologies
```

In file script:

```php
<?php

var_dump("PHP Version: " . phpversion())
```
