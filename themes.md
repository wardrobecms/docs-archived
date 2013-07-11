# Themes

- [Introduction](#introduction)
- [Location](#location)
- [Config](#config)
- [Helpers](#helpers)
- [Searching](#searching)
- [Post Tags](#posts)
- [Syntax](#syntax)

<a name="introduction"></a>
## Introduction

Wardrobe supports a pretty powerful theme system. This article is meant as a guide to explain and show some of the advanced options available.

<a name="location"></a>
## Location

By default all themes are stored in public/themes/:yourtheme: To create your own just duplicate the default theme and then change the theme used in app/config/wardrobe.php

<a name="config"></a>
## Config

Your theme may include it's own config.php file which will allow you to set theme specific options. Inside your theme folder create a file named config.php with the following:

    <?php
    return array(
      'copyright' => '&copy; Your Name',
    );

Then inside any of your theme files you can display this with:

    {{ Config::get('theme.copyright') }}

<a name="helpers"></a>
## Theme Helpers

Currently Wardrobe offers the following helpers:

### url()

    url('path')

This will prefix the path with the url to the install. This is useful for running Wardrobe in a sub folder or a strange location.

### theme_path()

    theme_path($path)

This can be used for generating the path to your theme assets. Some examples could be:

    // Extends the themes/yourtheme/layout
    @extends(theme_path('layout'))

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
      {{ $item['title'] }}
    @endforeach

Currently it supports passing an array as a param. So if you wanted to limit to a certain number then this would work:

    @foreach (Wardrobe::posts(array('per_page' => 5)) as $item)
      {{ $item['title'] }}
    @endforeach

<a name="searching"></a>
## Searching

If you wish to allow searching of posts you can add the following form to any of your theme views:

    <form method="get" action="{{ url('archive') }}">
      <input type="text" name="q" value="" placeholder="Search">
    </form>

<a name="posts"></a>
## Post Tags

All posts can display the following tags:

    {{ $post->title }} - The post title
    {{ $post->content }} - The raw markdown content
    {{ $post->parsed_content }} - The parsed content. Converts from markdown to html
    {{ $post->publish_date }} - The date time of the post. Can be converted to any format such as:
    {{ date("M/d/Y", strtotime($post->publish_date)) }}
    {{ $post->slug }} - The "slug" or uri string
    {{ $post->user->first_name }} - The author first name
    {{ $post->user->last_name }} - The author last name
    {{ $post->user->email }} - The author email

<a name="syntax"></a>
## Syntax

You can use straight php in the view files or you can use [Laravel blade](http://laravel.com/docs/templates#blade-templating) which is the default.

