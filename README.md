Melody - One-file composer scripts
==================================

Create a file named `test.php`:

```php
<?php
<<<CONFIG
packages:
    - "symfony/finder: ~2.5"
CONFIG;

$finder = Symfony\Component\Finder\Finder::create()
    ->in(__DIR__)
    ->name('*.php')
;

foreach ($finder as $file) {
    echo $file, "\n";
}
```

And simply run it:

```bash
melody run test.php
```

More Information
----------------

Read the [documentation](http://melody.sensiolabs.org) for more information.
