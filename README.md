# Tumble

A tumblelog theme for [Hugo](https://gohugo.io/).

This is very alpha so don't expect anything to be clean, tidy or even work.

Content types currently supported:

- aside
- image
- quote
- post
- video

## Important!

This theme relies heavily on its own archetypes to generate the different content types. Your local archetypes in `/archetypes` will override the theme archetypes in `/themes/tumble/archetypes` so move or delete your local `/archetypes/default.md`.

## Installation

From the root of your Hugo site:

    $ git clone https://github.com/adrianshort/tumble.git themes/
    
Enable the theme in your `/config.toml` file:

    theme = "tumble"
    
### Installing in a subfolder

If you want the root of your tumblelog in `https://example.org/deep/nested/folder/` rather than `https://example.org/` it should mostly work although image relative URLs in `post`s might not work right. This needs tidying up so that `relativeURLs = true` in your `config.toml` is respected properly. Leave that set to false for now.

## Creating content

All content types except `post` are set to `draft: false` for immediate publication.

All content types have a common set of tags, which is the only taxonomy supported.

### Asides

An aside is a short piece of text, typically one or two sentences. Asides don't have titles so it's easiest just to number them sequentially.

    $ hugo new asides/1.md
    
### Images

A single image with an optional caption (the `title`) and body text.

    # hugo new images/my-image-title.md
    
Then copy the image file itself to `/static/images/` and update `image_filename` in the front matter if required.

Set `show_title: true` to display the `title` as a caption beneath the image.

### Posts

A traditional blog post with mandatory title and body text.

    $ hugo new posts/my-post-title.md

### Quotes

A quotation usually by someone else, with attribution to the `author` and optionally to the `work` and `year`.

    $ hugo new quotes/shakespeare-hamlet.md
    
### Videos

An embedded video from YouTube, Vimeo etc. This is currently quite clunky as you have to get the full embed URL from the video hosting site.

So for [this video](https://www.youtube.com/watch?v=2-aWEYezEMk):

    $ hugo new videos/grimes-vanessa.md
    
Then set the frontmatter:

    embed_url: https://www.youtube.com/embed/2-aWEYezEMk
    




