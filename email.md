# Email Config

- [Introduction](#introduction)
- [From](#from)
- [Mail Driver](#driver)

<a name="introduction"></a>
# Introduction
In order for Wardrobe to send emails for password resets and similar functionality, the Mail settings must be setup. You can edit these settings in `app/config/mail.php`.

Here are some of the relevant configurations:

<a name="from"></a>
## From

You can change the "from" address of all sent emails with the `from` setting:

    return array(
        // More up here
        'from' => array('address' => 'john@doe.com', 'name' => 'John Doe'),
        // More down here
    );

<a name="driver"></a>
## Mail Driver

By default, the mail settings are set to the `smtp` driver:

    return array(
        'driver' => 'smtp',
        // More down here
    );

Here are some of the available drivers:

### Mail

This is the simplest option. If your web server supports sending email via PHP's `mail()` method, you can most likely simply change this setting to `mail` and be done with it.

### SMTP

If you have an email provider such as [Postmark](https://postmarkapp.com/), you can use the default `smtp` setting. You'll need to set a few other configurations for this to work:

    return array(
        // More up here
        'host' => 'smtp.mailgun.org',
        'port' => 587,
        'username' => 'my-smtp-username',
        'password' => 'my-smptp-password',
        // More down here
    );

You'll need to set the `host` for your email service provider. Postmark uses the host `smtp.mailgun.org`, which is the default setting in Wardrobe. The `host` configuration will change per email service, however.

Because SMTP mail often requires authentication, your email service will also give you other information you'll need to fill in, such as:

1. Port
2. Username
3. Password

### Sendmail

If you have Sendmail installed on your server you can use the `sendmail` driver. If you do, you should also check to make sure that the `sendmail` configuration is properly set to the location of the 'sendmail' program on your server.

A sensible (common) default is used in Wardrobe:

    return array(
        // More up here
        'sendmail' => '/usr/sbin/sendmail -bs',
    );

If you're unsure if `/usr/sbin/sendmail` is correct for you, you can SSH into your server and use the following command to output the path of the program:

    # Outputs location, such as /usr/sbin/sendmail
    $ which sendmail

## More Info

More information on mail settings can be found in the [Laravel Documentation](http://laravel.com/docs/mail#configuration).
