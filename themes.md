Wardrobe supports a pretty powerful theme system. This article is meant as a guide to explain and show some of the advanced options available. 

## Location

By default all themes are stored in public/themes/:yourtheme: To create your own just duplicate the default theme and then change the theme used in app/config/wardrobe.php 

## Theme Helpers

Currently Wardrobe offers the following helpers: 

### url()

    url('path')

This will prefix the path with the url to the install. This is useful for running Wardrobe in a sub folder or a strange location. 

### theme_path()

    theme_path($path)

This can be used for generating the path to your theme assets. Some examples could be: 

* @extends(theme_path('layout')) // Extends the themes/yourtheme/layout
* <link href="/{{ theme_path('css/style.css') }}" rel="stylesheet" media="screen"> // Generating a css link.

### Wardrobe::tags()

The method `Wardrobe::tags()` allows you to generate a list of all tags currently stored. An example usage could be: 

    @foreach (Wardrobe::tags() as $item)
      @if ($item['tag'] != "")
        <li>{{ $item['tag'] }}</li>
      @endif
    @endforeach

### Wardrobe::posts()

The method `Wardrobe::posts()` allows you to generate a list of posts on any page. Here is an example: 

    @foreach (Wardrobe::posts() as $item)
      {{ $item['title']}}
    @endforeach

Currently it supports passing an array as a param. So if you wanted to limit to a certain number then this would work: 

    @foreach (Wardrobe::posts(array('per_page' => 5)) as $item)
      {{ $item['title']}}
    @endforeach

## Syntax

You can use straight php in the view files or you can use [Laravel blade](http://laravel.com/docs/templates#blade-templating) which is the default. 
