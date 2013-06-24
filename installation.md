# Installation 

- [Install Composer](#install-composer)
- [Install Wardrobe](#install-wardrobe)
- [Requirements](#requirements)

<a name="install-composer"></a>
## Install Composer

Wardrobe utilizes [Composer](http://getcomposer.org) to manage its dependencies. First, download a copy of the `composer.phar`. Once you have the PHAR archive, you can either keep it in your local project directory or move to `usr/local/bin` to use it globally on your system. On Windows, you can use the Composer [Windows installer](https://getcomposer.org/Composer-Setup.exe).

<a name="install-wardrobe"></a>
## Install Wardrobe

### Via Git and Composer

You may install Wardrobe by cloning the project and then running `composer install` command in your terminal:

    git clone git@github.com:ericbarnes/wardrobe.git && cd wardrobe
    php composer.phar install

Next modify the [app/config/database.php](/docs/database) file to match your host settings. 

Finally visit `site.com/install` and follow the steps. 

### Via Download

Coming soon!

<a name="requirements"></a>
## Requirements

Wardrobe has a few server requirements:

- PHP >= 5.3.7
- MCrypt PHP Extension
- Database support (mysql, postgres, sqlite)

Administration requirements:

- Only tested against the **latest** browsers. 

> If you need < ie9 support please find another project. Sorry but I don't have time to worry about anything behind the latest release. 

