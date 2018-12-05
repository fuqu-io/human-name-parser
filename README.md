# human-name-parser
Tweaked a little.  See original.
0. namespaced psr4
0. parser now supports custom key output ->parse(['first' => 'first_name' ...])

A human name parser written in PHP.

Based on Josh Fraser's [PHP-Name-Parser](https://github.com/joshfraser/PHP-Name-Parser). Here, I attempted to rewrite the library to be more understandable (at least to myself) and perhaps more maintainable as a result. Just about all of the original features are maintained.

### Installation

Include in your project, or, install with [Composer](https://getcomposer.org/):

```bash
$ composer require chrisullyott/human-name-parser
```

### Parsing a name

```php
$name = 'Doctor Martin luther King Jr';

$parser = new HumanNameParser($name);
$result = $parser->parse();
```

```
Array
(
    [full]       => Dr. Martin Luther King Jr.
    [salutation] => Dr.
    [first]      => Martin
    [middle]     => Luther
    [last]       => King
    [suffix]     => Jr.
)
```
