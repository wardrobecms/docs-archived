# Change Log

- [v1.1](#v1.1)

<a name="v1.1"></a>
## Version 1.1

To see a full list of changes please see the [github milestone](https://github.com/wardrobecms/core/issues?milestone=1&page=1&state=closed).

### New Features

* Added the ability to auto route pages. This is done by creating new files in the public/themes/:yourtheme:/pages/ directory. For example if your page is named about.blade.php then you could access it via yoursite.com/pages/about
* Added ability to over ride default routes on the theme level. The default theme has an example of how this can be done. 
* Added automatic image upload resizing. This is a config setting that can be turned on or off. 
* Added new "cache" config item to turn on caching. It was previously missing. 

### Breaking Changes:

Reworked the `Wardrobe::posts` helper: 

    @foreach (Wardrobe::posts(array('tag' => 'love', 'limit' => 10)) as $item)
        {{ $item['title']}}
    @endforeach

Changed all the primary links to a new helper: 

    {{ Wardrobe::route('posts.archive') }}

