# SilverStripe SimpleCache module

## Maintainer

Marcus Nyeholt
<marcus (at) silverstripe (dot) com (dot) au>

## Documentation

[GitHub Wiki](http://wiki.github.com/nyeholt/silverstripe-simplecache)

## Licensing

This module is licensed under the BSD license

## Requirements

* QueuedJobs module (http://github.com/nyeholt/silverstripe-queuedjobs)

## Usage

* Define cache config - use the caches.conf.sample file as a guide
* Add the SimpleCachePublisher extension to a publishable data type and publish
  your page. 

```
Controller:
  extensions:
    - SimpleCacheControllerExtension
  
SiteTree:
  extensions:
    - SimpleCachePublisherExtension

```


* Change .htaccess to point to simplecache/frontend-cache.php instead of 
  framework/main.php
* Works in a similar way to static publisher, but uses a cache abstraction
  layer to allow for storing cached data in memcache or apc, or other cache
  platform.



## Configuration



