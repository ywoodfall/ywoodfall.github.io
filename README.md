## [Showcase](https://ojourmel.github.io/showcase/)

A portfolio type landing page, implemented as a CSS driven SPA. While it is designed for artists, photographers, or other content creators, it is relatively flexible.

Heavy (ab)use of the `:target` selector. Because of this, this site suffers from [page-jump](https://css-tricks.com/on-target/#article-header-id-2). Additionally, it can get a bit glitchy if browsers, like Internet Explorer decide not to render/update CSS rules. This site should be supported by all of the major modern browsers, (not IE8) and mobile devices. It is fully responsive.

This site does not use jQuery.

Inline everything for maximum performance (and simplicity of hosting).

### Installation
1. Add `index.html` to some web server.

### Instructions for Adding Content

Any place that could be edited for content will have a `<!-- - - - CONTENT - - - -->` HTML comment.
Here is the general list, in file order, of what needs to be changed:

1. Title
2. Email
  - This one is a bit weird. In order to (attempt) stopping web crawlers from spamming your email,
    it should be hidden via JavaScript. Follow the instructions in the function.
3. Header
  - This is what shows up at the top of the page. It can be blank.
5. About
  - Example text has been provided. Multiple images, texts, banners, and cursive banners can be used. All are optional.
6. Contact
  - Example text has been provided. Add / remove `contact-link-item`s as needed. The icon pack is [`Ionicons`](http://ionicons.com/) should additional links be needed. Update the `href` link as desired.
7. Work
  - This contains multiple `work-item`s, each with several parts. Any number of `work-item`s are allowed.
  - Several changes must be made in several places to make these things hookup correctly.

  1. Set `work-item-title` as desired.
  2. Update the `work-item`s id to the same (lowercase, all one word, `hyphens-can-be-used`).
  2. Update the `<a href>` directlt below the `work-item` to `"/#id"`, where id is the `work-item`s id.
  3. Set at least one `work-item-image` with the appropriate link (`href`).
  4. At the bottom, in the `work-list` section, add a `work-list-link` with an `href` to `/#id` where id is the same as the `work-item`s id.

### Advanced Changes
All of the CSS styles for the various components are located directly in `index.html`. Fonts, sizes, colors, and all sorts of things can be changed. Be sure to test all of your changes on all the major browsers, and at different sizes to ensure a good look.
