startup
===========================

PHP extension for creating startup snapshot. Storing initialized runtime context into heap.

REF: <https://marc.info/?l=php-internals&m=146056551131554&w=2>

```php
<?php
if (!startup_snapshot_load('myapp')) {
    require 'vendor/autoload.php';
    startup_snapshot_create('myapp');
}
```


TODO
----

- [ ] Load op array caches from opcache.
- [ ] Load the execution data, context and states.
- [ ] Ability to copy initialized zval into persistent memory.
 - [ ] Zend object
 - [ ] Array
 - [ ] Long number
 - [ ] String
