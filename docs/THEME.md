# Beautiful Jekyll Theme Documentation

This website uses the [Beautiful Jekyll](https://beautifuljekyll.com/) theme by [Dean Attali](https://deanattali.com).

[![Gem Version](https://badge.fury.io/rb/beautiful-jekyll-theme.svg)](https://badge.fury.io/rb/beautiful-jekyll-theme)

> *Copyright 2020 [Dean Attali](https://deanattali.com)*

**Beautiful Jekyll** is a ready-to-use template to help you create a beautiful website quickly. Perfect for personal sites, blogs, or simple project websites. [Check out a demo](https://beautifuljekyll.com) of what you'll get after just two minutes.

## Features

- **SIMPLE**: The primary goal of Beautiful Jekyll is to allow literally *anyone* to create a website in a few minutes.
- **Modern**: Uses the latest best practices and technologies to achieve nearly perfect scores on Google Chrome's Audit.
- **Mobile-first**: Designed to look great on both large-screen and small-screen (mobile) devices.
- **Highly customizable**: Many personalization settings such as changing the background colour/image, adding a logo.
- **Battle-tested**: By using Beautiful Jekyll, you'll be joining tens of thousands of users who used this theme since 2015.
- **Links to your social media**: You can easily add links to any of your social media accounts in the footer of every page.
- **Comments support**: Add comments to any page using either [Disqus](https://disqus.com/), [Facebook comments](https://developers.facebook.com/docs/plugins/comments), [Utterances](https://utteranc.es/), or [Staticman](https://staticman.net).
- **Share blog posts on social media**: By default, all blog posts have buttons to allow people to share on Twitter/Facebook/LinkedIn.
- **Tags**: Any blog post can be tagged with keywords, and an index page showing all the tags is automatically generated.
- **Tracking analytics**: Easily integrate Google Analytics, or other analytics platforms, to track visits to your website.
- **Photos support**: Any page can have a cover photo around its title, and any blog post can have an associated image.

## Supported YAML Parameters

Below is a list of the parameters that **Beautiful Jekyll** supports (any of these can be added to the YAML front matter of any page). Remember to also look in the `_config.yml` file to see additional settings.

### Main Parameters

These are the basic YAML parameters that you are most likely to use on most pages.

| Parameter   | Description |
| ----------- | ----------- |
| title       | Page or blog post title |
| subtitle    | Short description of page or blog post that goes under the title |
| tags        | List of tags to categorize the post. Separate the tags with commas and place them inside square brackets. Example: `[personal, analysis, finance]` |
| cover-img   | Include a large full-width image at the top of the page. You can either give the path to a single image, or provide a list of images to cycle through |
| comments    | If you want to add comments to a specific page, use `comments: true`. Comments only work if you enable one of the comments providers in `_config.yml` file. Comments are automatically enabled on blog posts but not on other pages; to turn comments off for a specific post, use `comments: false`. |

### Less Commonly Used Parameters

These are parameters that you may not use often, but can come in handy sometimes.

| Parameter   | Description |
| ----------- | ----------- |
| readtime    | If you want a post to show how many minutes it will take to read it, use `readtime: true`. |
| show-avatar | If you have an avatar configured in the `_config.yml` but you want to turn it off on a specific page, use `show-avatar: false`. |
| image       | If you want to add an image to your blog post that will show up next to the post's excerpt on the feed and in the post page itself, use `image: /path/to/img`. |
| share-img   | If you want to specify an image to use when sharing the page on Facebook or Twitter, then provide the image's full URL here. |
| social-share | By default, every blog post has buttons to share the page on social media. If you want to turn this feature off, use `social-share: false`. |
| nav-short   | By default, the navigation bar gets shorter after scrolling down the page. If you want the navigation bar to always be short on a certain page, use `nav-short: true` |
| gh-repo   | If you want to show GitHub buttons at the top of a post, this sets the GitHub repo name (eg. `daattali/beautiful-jekyll`). You must also use the `gh-badge` parameter to specify what buttons to show. |
| gh-badge  | Select which GitHub buttons to display. Available options are: [star, watch, fork, follow]. You must also use the `gh-repo` parameter to specify the GitHub repo. |
| layout      | What type of page this is (default is `post` for blog posts and `page` for other pages). See _Page types_ section below for more information. |

### Advanced Parameters

These are advanced parameters that are only useful for people who need very fine control over their website.

| Parameter   | Description |
| ----------- | ----------- |
| footer-extra | If you want to include extra information in the footer, create an HTML file in the `_includes/` folder (for example `_includes/myinfo.html`) and set `footer-extra` to the name of the file (for example `footer-extra: myinfo.html`) |
| language    | HTML language code to be set on the page's &lt;html&gt; element. |
| use-site-title | If you want to use the site title rather than the page title as the HTML document title, use `use-site-title: true`. |
| js          | List of local JavaScript files to include in the page (eg. `/assets/js/mypage.js`) |
| ext-js      | List of external JavaScript files to include in the page (eg. `//cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js`). External JavaScript files that support [Subresource Integrity (SRI)](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) can be specified using the `href` and `sri` parameters. |
| css         | List of local CSS files to include in the page |
| ext-css      | List of external CSS files to include in the page. External CSS files using SRI (see `ext-js` parameter) are also supported. |

## Page Types

- **post** - To write a blog post, add a markdown or HTML file in the `_posts` folder. As long as you give it YAML front matter (the two lines of three dashes), it will automatically be rendered like a blog post.
- **page** - Any page outside the `_posts` folder that uses YAML front matter will have a very similar style to blog posts.
- **home** - The home layout is meant to act as the homepage of your blog posts - it will display all your blog posts, sorted from newest to oldest. A file using the `home` layout must be named `index.html` (not `index.md` or anything else!).
- **minimal** - If you want to create a page with minimal styling (ie. without the bulky navigation bar and footer), assign `layout: minimal` to the YAML front matter.
- If you want to completely bypass the template engine and just write your own HTML page, simply omit the YAML front matter.

## Customizing Parameters for Each Page

**Important**: In order to have your new pages use this template and not just be plain HTML pages, **you must add [YAML front matter](https://jekyllrb.com/docs/front-matter/) to the top of each page**. This is where you'll be able to give each page some extra parameters such as a title, a subtitle, or an image.

If you don't want to use any parameters on a page (this also means having no title), then use the empty YAML front matter:

```yaml
---
---
```

If you do want to use any parameters, write them between these two lines. For example:

```yaml
---
title: Contact me
subtitle: Here you'll find all the ways to get in touch with me
---
```

**Important takeaway: ALWAYS add the YAML front matter, which is two lines with three dashes, to EVERY page. If you have any parameters, they go between the two lines.**

## FAQ

### How do I change the number of posts per page OR the colour of the navigation bar OR the image in the navigation bar?

Beautiful Jekyll is built to be very customizable. Many questions about "how do I change..." can be answered by looking at the `_config.yml` file. The configuration file has many adjustable parameters to customize your site.

### How do I add a favicon to my site?

Easy! Just place a valid `favicon.ico` in the root directory of your project. And then wait! It can take a while to update.

### How do I move the blog to another page instead of having it on the home page?

The default style of Beautiful Jekyll is to feature the blog feed on the front page. To have the blog hosted on a different URL (for example at `<mysite.com>/blog`), copy the `index.html` file into a folder with the same name as the desired page (for example, to `blog/index.html`), and in the `_config.yml` file you need to add a parameter `paginate_path: "/<page name>/page:num/"` (for example `paginate_path: "/blog/page:num/"`).

### What size do you recommend using for the `cover-img` photos?

Unfortunately, this is a no-answer! There isn't a one-size-fits-all solution to this, because every person will view your site on a different browser with different dimensions. The image will always be centered, so the only tip is to make sure the important part of the image is in the middle so that it'll always show.

### How do I use MathJax equations in my posts?

MathJax can be easily integrated into your website with a one-line addition. See [this discussion](https://github.com/daattali/beautiful-jekyll/issues/195) for more information.

## Credits

This template was not made *entirely* from scratch. Special thanks to [Jekyll Now](https://github.com/barryclark/jekyll-now) and [Bootstrap Clean Blog](https://github.com/IronSummitMedia/startbootstrap-clean-blog), from whom several ideas were initially taken.

Thanks also to [Dr. Jekyll's Themes](https://drjekyllthemes.github.io/), [Jekyll Themes](http://jekyllthemes.org/), and another [Jekyll Themes](http://jekyllrc.github.io/jekyllthemes/) for featuring Beautiful Jekyll in their Jekyll theme directories.

## More Information

For more detailed information about Beautiful Jekyll, visit the official website: [https://beautifuljekyll.com](https://beautifuljekyll.com)

For support, visit the [Jekyll support forum](https://talk.jekyllrb.com/).

**If you enjoy this theme, please consider [supporting the creator](http://paypal.me/daattali) or [sponsoring](https://github.com/sponsors/daattali).**
