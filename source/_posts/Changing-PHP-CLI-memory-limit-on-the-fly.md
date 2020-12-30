---
title: Changing PHP CLI memory limit on the fly
date: 2020-04-24 20:05:28
tags:
  - bytesize
  - php
  - laravel
  - artisan
category:
  - codes
---

<img src="/images/posts/20200424/peter-maselkowski-N135eczYTAs-unsplash.jpg" title="Photo by Peter Masełkowski on Unsplash" alt="Photo by Peter Masełkowski on Unsplash" style="width: 500px" />
<span>Photo by <a href="https://unsplash.com/@maselkowski?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Peter Masełkowski</a> on <a href="/s/photos/php?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

There are some tasks in laravel that a `php artisan` would just be enough.

But there are tasks that would just consume the php config `memory_limit`.

You can always update your `php.ini` file and increase the `memory_limit=1G` for example or you can do this in your `cli`:

```shell
php -d memory_limit=1G heavy_script.php
```

or

```shell
php -d memory_limit=1G artisan command:name
```

{% post_link Checking-PHP-ini-and-version-file-via-CLI-or-file-script %}

Cheers!
