# Wardrobe Config

You can change the configuration for Wardrobe in the `app/config/wardrobe.php` file. Here are the available options:

  <?php

  return array(
    'theme' => 'My Theme Name',
    'title' => 'My Blog Title',
    'per_page' => 5,
    'installed' => true,
  );

### Theme
This is the name of your theme. The options currently available out of the box are `default`, `simple` and `blocky`.

Themes are found in the `public/themes` directory. If your `theme` setting is `my-theme`, then Wardrobe will search for theme files in the `public/themes/my-theme` directory. **This means that your theme name is directly tied to your theme's folder name.**

More information on themes is [here](/docs/themes).

### Title
This is the title of your blog, which is usually output globally in your theme. This name is available via the theme helper method `site_title()` and might, for example, appear in your theme layout file like this:

  <header>
    <h1><a href="{{ url('/') }}">{{ site_title() }}</a></h1>
  </header>

### Per Page
The `per_page` option is the default number of articles which will appear on your site per page.

### Installed
This is to let the system know that the system is installed. This should generally not be manually changed.
