# Localization

- [Introduction](#introduction)
- [Download](#download)
- [Change Config](#config)

<a name="introduction"></a>
## Introduction

Wardrobe allows you to run the administration in your locale by adding new translation files.

<a name="download"></a>
## Download

You can download all of the localization files from [github](https://github.com/wardrobecms/locales). After downloading overwrite your app/lang directory with these.

<a name="config"></a>
## Change Config

After you have succesfully adding the lang files next open app/config/app.php and modify the following section:

    'locale' => 'en',

Replace 'en' with your locale. Such as 'es'.


