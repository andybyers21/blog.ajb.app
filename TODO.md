#### Built-in shortcodes

- **`image`** (prop required: **`src`**; props optional: **`alt`**, **`position`** (**left** is default | center | right), **`style`**)
  - eg: `{{< image src="/img/hello.png" alt="Hello Friend" position="center" style="border-radius: 8px;" >}}`
- **`figure`** (same as `image`, plus few optional props: **`caption`**, **`captionPosition`** (left | **center** is default | right), **`captionStyle`**
  - eg: `{{< figure src="/img/hello.png" alt="Hello Friend" position="center" style="border-radius: 8px;" caption="Hello Friend!" captionPosition="right" captionStyle="color: red;" >}}`
- **`imgproc`** Hugo shortcode for image processing, plus additional **`position`** param [ left | center | right ] (optional).
  - eg: `{{< imgproc "img/hello.png" Resize "250x" center />}}`
  - More detailed info on processing commands at [https://gohugo.io/content-management/image-processing/](https://gohugo.io/content-management/image-processing/)
- **`code`** (prop required: **`language`**; props optional: **`title`**, **`id`**, **`expand`** (default "△"), **`collapse`** (default "▽"), **`isCollapsed`**)

  - eg:

  ```go
  {{< code language="css" title="Really cool snippet" id="1" expand="Show" collapse="Hide" isCollapsed="true" >}}
  pre {
    background: #1a1a1d;
    padding: 20px;
    border-radius: 8px;
    font-size: 1rem;
    overflow: auto;

    @media (--phone) {
      white-space: pre-wrap;
      word-wrap: break-word;
    }

    code {
      background: none !important;
      color: #ccc;
      padding: 0;
      font-size: inherit;
    }
  }
  {{< /code >}}
  ```

#### Code highlighting

By default the theme is using PrismJS to color your code syntax.

**Supported languages**: bash/shell, css, clike, javascript, apacheconf, actionscript, applescript, c, csharp, cpp, coffeescript, ruby, csp, css-extras, diff, django, docker, elixir, elm, markup-templating, erlang, fsharp, flow, git, go, graphql, less, handlebars, haskell, http, java, json, kotlin, latex, markdown, makefile, objectivec, ocaml, perl, php, php-extras, r, sql, processing, scss, python, jsx, typescript, toml, reason, textile, rust, sass, stylus, scheme, pug, swift, yaml, haml, twig, tsx, vim, visual-basic, wasm.

**NOTE:** Please keep in mind that currently main menu doesn't support nesting.

## How to add a cover image to your posts

Adding a cover image to your post is simple and there are two options when you edit your `index.md` file in `content/posts/blog-entry-xy/index.md`:

- Use `cover = "/path/to/absolute/img.jpg"` to link an absolute image
  - Resulting in `https://www.yourpage.com/path/to/absolute/img.jpg`
- Use `cover = "img.jpg"` and `useRelativeCover = true` to link the image relative to the blog post folder
  - Resulting in `https://www.yourpage.com/posts/blog-entry-xy/img.jpg`
- Use `coverAlt = "description of image"` to add custom alt text to the cover image (defaults to post or page title as alt text)
- Use `coverCaption = "Image Credit to [Barry Bluejeans](https://unsplash.com/)"` to add a caption for the cover image.

## How to display the Last Modified Date in your posts

Add `lastModDisplay = "[your display text]"` to `config.toml` to enable last modified date on your posts. Note - an empty string value `""` does not display anything.

Example: `lastModDisplay = "Modified:"` --> "Modified: Jan 01, 0001"

:octocat: Hugo's `enableGitInfo` option is a nice complement to this feature.

## Add-ons

- **Archive** — Theme has built-in `archive` page for main content (see `contentTypeName` variable in config). If you need archive on your blog just copy https://github.com/panr/hugo-theme-hello-friend/blob/master/exampleSite/content/archive.md to your `content` dir. If you need multilangual archives, duplicate `content/archive.md` and add `.Lang` variable, eg: `content/archive.pl.md` (remember to change `url` in duplicated file).
- **Comments** — for adding comments to your blog posts please take a look at `layouts/partials/comments.html` https://github.com/panr/hugo-theme-terminal/blob/master/layouts/partials/comments.html.
- **Prepended `<head>`** — if you need to add something inside `<head>` element, and before any of the theme's `<script>` and `<link>` tags are declared, please take a look at `layouts/partial/prepended_head.html` https://github.com/panr/hugo-theme-hello-friend/blob/master/layouts/partials/prepended_head.html
- **Extended `<head>`** — if you need to add something inside `<head>` element, after all of all of the theme's `<script>` and `<link>` tags are declared, please take a look at `layouts/partial/extended_head.html` https://github.com/panr/hugo-theme-hello-friend/blob/master/layouts/partials/extended_head.html
- **Extended `<footer>`** — if you need to add something before end of `<body>` element, please take a look at `layouts/partial/extended_footer.html` https://github.com/panr/hugo-theme-hello-friend/blob/master/layouts/partials/extended_footer.html

## `Hello Friend` theme user?

I'd be happy to know more about you and what you are doing. If you want to share it, please make a contribution and [add your site to the list](https://github.com/panr/hugo-theme-hello-friend/blob/master/USERS.md)! 🤗
