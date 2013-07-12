# Configuration

- [Application](#application)
- [Install Wardrobe](#install-wardrobe)
- [Requirements](#requirements)

<a name="application"></a>
## Application Config

The main application config is stored in app/config/app.php inside this is a few settings you may want to adjust to your own needs.

### Timezone

Wardrobe using UTC as the default timezone so it's recommended you change this to suit your location. To find out the time zone you should use please visit the [timezones](http://php.net/manual/en/timezones.php) section of the php docs. For example if you are in the Eastern United States you would use:

    'timezone' => 'America/New_York',

### Debugging

By default debugging is turned off and should be turned off in production but if you are running into issues you can turn it on by changing the following to true:

    'debug' => true,
