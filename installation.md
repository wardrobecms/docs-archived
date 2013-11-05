# Installation

- [Install  Wardrobe](#install-wardrobe)
- [Setup Configuration](#set_config)
- [Requirements](#requirements)

<a name="install-wardrobe"></a>
## Install Wardrobe

Wardrobe utilizes [Composer](http://getcomposer.org) to manage its dependencies. First, download a copy of the `composer.phar`. Once you have the PHAR archive, you can either keep it in your local project directory or move to `usr/local/bin` to use it globally on your system. On Windows, you can use the Composer [Windows installer](https://getcomposer.org/Composer-Setup.exe).

Once composer is setup you can install wardrobe by running:

    composer create-project wardrobe/wardrobe

Or if you prefer to live on the edge:

    composer create-project wardrobe/wardrobe --stability=dev

<a name="set_config"></a>
## Setup the Configuration

Next modify the [app/config/database.php](/docs/database) file to match your host settings.

Then set the permissions on the following folders so the server has write access:

    chmod -R 777 app/storage
    chmod 777 public/img

Finally visit `site.com/install` and follow the steps. After finishing the install you can visit `site.com/wardrobe` to
access the admin area.

<a name="requirements"></a>
## Requirements

Wardrobe has a few server requirements:

- PHP >= 5.3.7
- MCrypt PHP Extension
- Database support (mysql, postgres, sqlite)

Administration requirements:

- Only tested against the **latest** browsers.

> If you need < ie9 support please find another project. Sorry but I don't have time to worry about anything behind the latest release.

