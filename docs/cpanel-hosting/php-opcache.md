# PHP OPcache <small>FAQ</small>

## Introduction

[The PHP Group](http://php.net/) describes [PHP OPcache](http://php.net/manual/en/intro.opcache.php) as improving `#!cirru PHP` performance by storing precompiled script bytecode in shared memory, thereby removing the need for `#!cirru PHP` to load and parse scripts on each request.

!!! note ""
    To learn more about the overwhelming benefits of using `#!cirru OPcache` we suggest starting with this AppDynamics article: [Why Every PHP Application Should Use an OpCache](https://blog.appdynamics.com/engineering/why-every-php-application-should-use-an-opcache/)

---

## Configuring OPcache

Complete `runtime configuration` is provided to each `#!cirru cPanel` account by default. Methods of configuration include exposing `#!cirru OPcache` functions for scripts, allowing configuration controls within `#!cirru .htaccess` files, and directly within `#!cirru cPanel`.

---

### Flush OPcache

<small>**Flushing OPcache on demand is recommended for most situations**</small>

* **Create a `#!cirru PHP` file with the following code:**
``` php
<?php
    opcache_reset();
    print("Done.");
?>
```

    **That's it!** Now, any time you request that `#!cirru PHP` script in your browser it will flush the server side cache, so that you can keep the performance benefits in place, while also ensuring any `#!cirru PHP` code changes are brought into effect as required.

!!! tip 

    More details about `#!cirru PHPs` `#!cirru opcache_reset` function can be found in the [PHP Manual for opcache_reset](http://php.net/manual/en/function.opcache-reset.php) along with further code snippets and examples.


---

### Toggle OPcache On/Off

<small>**Generally completely disabling OPcache in this way is not recommended**</small>

Within `#!cirru cPanel` Navigate to `Select PHP Version`:

[![cPanel > Select PHP Version](/img/opcache/cPanel-SelectPHP.png)](/img/opcache/cPanel-SelectPHP.png)

Next, simply `Check` or `Uncheck` the `#!cirru opcache` <small>(and `#!cirru zend_guard_loader` if present)</small> extensions and then `Save` to apply the change:

[![cPanel > Select PHP Extensions/Modules](/img/opcache/cPanel-SelectPHP-opcache.png)](/img/opcache/cPanel-SelectPHP-opcache.png)

---

# Further Resources

> Still in need of help? For speedy assistance our friendly staff are always ready to help via our [helpdesk](https://helpdesk.hostnetworks.com.au/core/), on [Twitter](https://twitter.com/HostNetworks), through our [website](https://hostnetworks.com.au/), or directly via [email to support](/contact/).

---
