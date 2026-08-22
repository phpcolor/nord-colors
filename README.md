# Nord Colors

This package provides access to the Nord color palette, an arctic, north-bluish color scheme.

## Installation

```bash
composer require phpcolor/nord-colors:^2.0
```

The package works standalone. Install `phpcolor/phpcolor` only when using `palette()`:

```bash
composer require phpcolor/phpcolor
```

## Usage

### Create Colors Instance

```php
use PhpColor\Colors\Nord\NordColors as Nord;

$colors = Nord::colors();
```

### Color Names

```php
use PhpColor\Colors\Nord\NordColors as Nord;

$colors = Nord::colors();

$names = $colors->getNames();
// 'nord0', 'nord1', 'nord2', 'nord3', 'nord4', 'nord5',
// 'nord6', 'nord7', 'nord8', 'nord9', 'nord10', 'nord11',
// 'nord12', 'nord13', 'nord14', 'nord15'
```

### Color Values

```php
use PhpColor\Colors\Nord\NordColors as Nord;

$colors = Nord::colors();

echo $colors->nord10;             // #5E81AC
echo $colors->get('nord8');       // #88C0D0

// Or use the id() method
echo $colors->id(10);             // #5E81AC
```

### PHPColor Palette

```php
use PhpColor\Color\Palette\ColorPaletteInterface;
use PhpColor\Colors\Nord\NordColors as Nord;

$palette = Nord::colors()->palette();
assert($palette instanceof ColorPaletteInterface);

echo $palette->get('nord10')->toHex(); // #5e81ac
```

Calling `palette()` without `phpcolor/phpcolor` installed throws a `LogicException` with the installation command.

## Credits

The colors listed in this project are based on the [Nord Theme](https://www.nordtheme.com/).

## License

This [PHPColor](https://phpcolor.dev) package is released under the [MIT license](LICENSE).
