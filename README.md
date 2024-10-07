# Hyva Tooltip &nbsp; [![Latest Stable Version](https://img.shields.io/badge/version-1.0.1-pink)](https://packagist.org/packages/blackbird/hyva-tooltip) [![License: MIT](https://img.shields.io/github/license/blackbird-agency/hyva-tooltip.svg)](./LICENSE)

This Magento 2 module will allow you to easily display tooltip in your Hyvä Theme.

## Installation

```bash
composer require blackbird/hyva-tooltip
```

```bash
php bin/magento setup:upgrade
```

## Usage

```html
<button id="button-<?= $uniqueId ?>"
        x-data="blackbird.tooltip({
            tooltipSelector: '#tooltip-<?= $uniqueId ?>',
        })"
>
    My button
</button>

<div id="tooltip-<?= $uniqueId ?>" blackbird-tooltip>My tooltip</div>
```

```html
<button id="button-<?= $uniqueId ?>">My button</button>

<div id="tooltip-<?= $uniqueId ?>"
     blackbird-tooltip
     x-data="blackbird.tooltip({
         buttonSelector: '#button-<?= $uniqueId ?>',
     })"
>
    My tooltip
</div>
```

```html
<div x-data="blackbird.tooltip({
         buttonSelector: '#button-<?= $uniqueId ?>',
         tooltipSelector: '#tooltip-<?= $uniqueId ?>',
     })">
</div>

<button id="button-<?= $uniqueId ?>">My button</button>
<div id="tooltip-<?= $uniqueId ?>" blackbird-tooltip>My tooltip</div>
```
