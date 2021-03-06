Google Analytics Bundle
=======================

*By [endroid](http://endroid.nl/)*

[![Latest Stable Version](http://img.shields.io/packagist/v/endroid/google-analytics-bundle.svg)](https://packagist.org/packages/endroid/google-analytics-bundle)
[![Build Status](https://secure.travis-ci.org/endroid/EndroidGoogleAnalyticsBundle.png)](http://travis-ci.org/endroid/EndroidGoogleAnalyticsBundle)
[![Total Downloads](http://img.shields.io/packagist/dt/endroid/google-analytics-bundle.svg)](https://packagist.org/packages/endroid/google-analytics-bundle)
[![Monthly Downloads](http://img.shields.io/packagist/dm/endroid/google-analytics-bundle.svg)](https://packagist.org/packages/endroid/google-analytics-bundle)
[![License](http://img.shields.io/packagist/l/endroid/google-analytics-bundle.svg)](https://packagist.org/packages/endroid/google-analytics-bundle)

This bundle integrates Google Analytics in your project. It allows you to
create one or multiple tracking codes and provides easy definition of tracking
script in you templates.

[![knpbundles.com](http://knpbundles.com/endroid/EndroidGoogleAnalyticsBundle/badge-short)](http://knpbundles.com/endroid/EndroidGoogleAnalyticsBundle)

## Installation

Use [Composer](https://getcomposer.org/) to install the bundle.

``` bash
$ composer require endroid/google-analytics-bundle
```

Then enable the bundle via the kernel.

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Endroid\Bundle\GoogleAnalyticsBundle\EndroidGoogleAnalyticsBundle(),
    );
}
```

## Configuration

### config.yml

Multiple trackers can be defined via the configuration. A tracker can either
be created using the short syntax or using the long syntax in case you want
to change one of the optional parameters.

```yaml
endroid_google_analytics:
    trackers:
        default: UA-XXXX-Y
        another: { property_id: UA-XXXX-Z, require_display_features: true }
        
```

## Usage

After installation and configuration, the tracker can be rendered using the
following Twig syntax.

```twig
<html>
    <head>
        ...
        {{ google_analytics_tracker('default') }}
    </head>
    ...
```

## Versioning

Version numbers follow the MAJOR.MINOR.PATCH scheme. Backwards compatibility
breaking changes will be kept to a minimum but be aware that these can occur.
Lock your dependencies for production and test your code when upgrading.

## License

This bundle is under the MIT license. For the full copyright and license
information please view the LICENSE file that was distributed with this source code.
