# Wardrobe Config

- [Introduction](#introduction)
- [Theme](#theme)
- [Title](#title)
- [Per Page](#per_page)
- [Installed](#installed)

<a name="introduction"></a>
## Introduction
You can change the configuration for Wardrobe in the `app/config/wardrobe.php` file. During installation this file will be generated automatically. If you need to make changes at a later point you can edit it manually. Here are the available options:

    return array(
        'theme' => 'my-theme',
        'title' => 'My Blog Title',
        'per_page' => 5,
        'installed' => true,
    );

<a name="theme"></a>
## Theme
This is the name of your theme. The options currently available out of the box are `default`, `simple` and `blocky`.

Themes are found in the `public/themes` directory. If your `theme` setting is `my-theme`, then Wardrobe will search for theme files in the `public/themes/my-theme` directory. **This means that your theme name is directly tied to your theme's folder name.**

More information on themes is [here](/docs/themes).

<a name="title"></a>
## Title
This is the title of your blog, which is usually output globally in your theme. This name is available via the theme helper method `site_title()` and might, for example, appear in your theme layout file like this:

    <header>
        <h1><a href="{{ url('/') }}">{{ site_title() }}</a></h1>
    </header>

<a name="per_page"></a>
## Per Page
The `per_page` option is the default number of articles which will appear on your site per page.

<a name="installed"></a>
## Installed
This is to let the system know that the system is installed. This should generally not be manually changed.
