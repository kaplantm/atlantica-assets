# alantica-assets

Static file repository for Alantica MC

Text files use markdown for formatting [Markdown Guide](https://guides.github.com/features/mastering-markdown/)
HTML can also be used.

Editing files in this repository updates the contents of the RAD Atlantica site

In addition to markdown files, there are two config files the site uses.

### Navigation Config

The navigation-config file controls the navigation bar at the top right of the page.
It holds a list of items in the navigation bar.

For example:

```
{
  "navigation": [
    { "title": "Home", "file": "home" },
    {
      "title": "Donate",
      "route": "https://www.paypal.com/pools/c/8nfrLk8JoJ",
      "type": "external"
    }
  ]
}

```

This will setup a navigation bar with just two items. Items in the navigation bar will appear in the order they are in the list, with the first item in the list being the leftmost navigation link.

The first item:
It will be labelled "Home" and link to a page that shows the contents of the `home.md` file in the `pages/` directory.

The second item:
It will be labelled "Donate". `"type": "external"` sets this as an external link to the `route` that is set. All links are assumed to be internal unless specified.

### News Config

The navigation-config holds a list of items on the news page.

For example:

```
{
  "news": [
    {
      "file": "we-moved",
      "published": "3/10/2020",
      "title": "RAD1 Server Reset",
      "type": "warning"
    }
  ]
}

```

This will setup the news page to show one post. The title of the post is RAD1 Server Reset. It will show that it was published 3/10/2020. It will be styled like a warning. (Options for type are: "normal", "warning" and "alert". If left blank, it will be a "normal" post.) This post will display the contents of the `we-moved.md` file in the `pages/news/` directory.

News items will appear in the order they are in the list, with the first item in the list being the top most post on the news page.
