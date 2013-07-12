# Writing Posts

- [Introduction](#introduction)
- [Drag and Drop](#drag-drop)
- [Post Slug](#slug)
- [Post Author](#author)
- [Status](#status)
- [Adding Tags](#tagging)
- [Publish Date](#publish-date)

<a name="introduction"></a>
## Introduction

Wardrobe is designed to keep the focus on writing and because of this all writing options are tucked away as they are secondary to your content. This page will highlight all these extra options.

<a name="drag-drop"></a>
## Drag and Drop

Prefer to write locally? Wardrobe supports drag and drop posting. Locally create a new file with this structure:

    ---
    title: My Title
    slug: my-title
    date: Tomorrow 9am
    tags: [sample, post]
    ---

    This is the *markdown* content

Save it and then drag and drop into your wardrobe admin. You will then be forwarded to the Write page with all the fields filled out. This gives you an opportunity to verify all the fields and content is correct before saving.

<a name="slug"></a>
## Post Slug

The post "slug" is the URI string used for displaying the post on the frontend. So for example if you post is titled "My Summer" then the slug will be "my-summer". Which will make the post available at: `site.com/post/my-summer`

This will be generated automatically based on your title but sometimes you will want to change it. This field is found in the [Advanced Options](#advanced-options).

<a name="author"></a>
## Post Author

If you have multiple authors and wish to change the author you can open the [Advanced Options](#advanced-options) to edit.

<a name="status"></a>
## Post Status

Currently you can set the status of a post to either active or draft. Draft posts are only visible in the admin and for previewing. This setting is found in [Advanced Options](#advanced-options)

<a name="tagging"></a>
## Tagging

If you wish to add post tags you can click the <i class="icon-tags"></i> tags icon in the post bar. By tagging it will allow you to categorize posts for easy retrieval later.

<a name="publish-date"></a>
## Publish Date

You can change the post date by clicking the <i class="icon-calendar"></i> calendar icon. Setting the date to the future will prevent the post from displaying until that date and time is present.

This field is a free form input field that utilizes php's [strtotime](http://php.net/strtotime). This makes it flexible in that you can use common language to represent your post date. Some examples could be:

* Tomorrow 8am
* Next Tuesday 10am
* May 1 2014
* Now
* 1 April 2014
* etc...

> Please note that dates in the m/d/y or d-m-y formats are disambiguated by looking at the separator between the various components: if the separator is a slash (/), then the American m/d/y is assumed; whereas if the separator is a dash (-) or a dot (.), then the European d-m-y format is assumed.

<a name="advanced-options"></a>
## Advanced Options

You can click the arrow <i class="icon-chevron-sign-right"></i> beside the title to expand the advanced options. This will then display the slug, author, and status.
