# Installation

- [Download  Wardrobe](#download-wardrobe)
  - [Via Git and Composer](#git-composer) 
  - [Via Download](#download)
- [Setup Configuration](#set_config)
- [Requirements](#requirements)

<a name="download-wardrobe"></a>
## Download Wardrobe

<a name="git-composer"></a>
### Via Git and Composer


Wardrobe utilizes [Composer](http://getcomposer.org) to manage its dependencies. First, download a copy of the `composer.phar`. Once you have the PHAR archive, you can either keep it in your local project directory or move to `usr/local/bin` to use it globally on your system. On Windows, you can use the Composer [Windows installer](https://getcomposer.org/Composer-Setup.exe).


You may install Wardrobe by cloning the project and then running `composer install` command in your terminal:

    git clone git@github.com:ericbarnes/wardrobe.git && cd wardrobe
    php composer.phar install

<a name="download"></a>
### Via Download

Coming soon!

<a name="set_config"></a>
## Setup the Configuration

Next modify the [app/config/database.php](/docs/database) file to match your host settings.

Then set the permissions on the following folders so the server has write access:

    chmod -R 777 app/storage
    chmod 777 public/img

Depending on your server you may also need to make the following files writable as the installation writes config settings:

    app/config/app.php
    app/config/wardrobe.php

Finally visit `site.com/install` and follow the steps.

<a name="requirements"></a>
## Requirements

Wardrobe has a few server requirements:

- PHP >= 5.3.7
- MCrypt PHP Extension
- Database support (mysql, postgres, sqlite)

Administration requirements:

- Only tested against the **latest** browsers.

> If you need < ie9 support please find another project. Sorry but I don't have time to worry about anything behind the latest release.

