# Daft Help Desk Theme

This contains the help centre theme for Daft. To run locally please run the command:

```bash
zat theme preview
```

When promted "Enter your Zendesk subdomain or full URL", please inset `https://helpdaft.zendesk.com`

When promted "Enter your username", please inset your zendesk login username, i.e. `aoife@donedeal.ie`

When promted "Enter your password", please inset your zendesk login password.

This theme is derived from the 'Copenhagen' theme, which is the default Zendesk Guide theme. It is designed to be responsive and accessible.
Learn more about customizing Zendesk Guide [here](https://support.zendesk.com/hc/en-us/sections/206670747).

The Copenhagen theme for Help Center consists of a [set of templates](#templates), [styles](#styles), a Javascript file used mainly for interactions and an [assets folder](#assets).

## How to use

You can use your favorite IDE to develop themes and preview your changes locally in a web browser using the Zendesk Apps Tools (ZAT). For details, see [Previewing theme changes locally](https://support.zendesk.com/hc/en-us/articles/115014810447).

### Settings folder

If you have a variable of type file, you need to provide a default file for that variable in the `/settings` folder. This file will be used on the settings panel by default and users can upload a different file if they like.
Ex.
If you would like to have a variable for the background image of a section, the variable in your manifest file would look something like this:

```js
{
  ...
  "settings": [{
    "label": "Images",
    "variables": [{
      "identifier": "background_image",
      "type": "file",
      "description": "Background image for X section",
      "label": "Background image",
    }]
  }]
}

```

And this would look for a file inside the settings folder named: `background_image`

### Adding assets

You can add assets to the asset folder and use them in your CSS, Javascript and templates.
You can read more about assets [here](https://support.zendesk.com/hc/en-us/articles/115012399428)

## Publishing your theme

You can import directly from GitHub - learn more [here](https://support.zendesk.com/hc/en-us/community/posts/360004400007).

## Templates

The theme includes all the templates that are used for a Help Center that has _all_ the features available.
List of templates in the theme:

- Article page
- Category page
- Community post list page
- Community post page
- Community topic list page
- Community topic page
- Contributions page
- Document head
- Error page
- Footer
- Header
- Home page
- New community post page
- New request page
- Requests page
- Search results page
- Section page
- Subscriptions page
- User profile page

You can add up to 10 optional templates for:

- Article page
- Category page
- Section page

You do this by creating files under the folders `templates/article_pages`, `templates/category_pages` or `templates/section_pages`.
Learn more [here](https://support.zendesk.com/hc/en-us/articles/360001948367).

## Styles

The styles that Theming Center needs to use in the theme are in the `style.css` file in the root folder.

The styles for the theme are split using Sass partials, all the partials are under [styles/](/blob/master/styles/), they are all included in the "main" file [index.scss](/blob/master/styles/index.scss) and then compiled to CSS.
If you wish to use SASS you can go to the [using SASS section](#using-sass)

## Assets

These are the images that are needed for the theme.
These include:

- Loader
- Dropdown arrow
