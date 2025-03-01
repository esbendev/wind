# FREE JEKYLL THEME Wind: A Minimalistic, Simple, and Beautiful Blogging Theme

![Theme Logo or Screenshot](https://i.postimg.cc/QMkCmRx2/screenshot.png)

## Description

Wind is a clean, minimalistic Jekyll theme designed to offer a delightful blogging experience. With a focus on simplicity and aesthetics, Wind brings an elegant touch to your blog or personal website.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Features

1. **Responsive Design:** Wind offers a thoughtfully crafted responsive design that ensures your blog looks stunning and functions flawlessly on a variety of devices, including desktops, tablets, and smartphones. Your content remains accessible and visually appealing, no matter how your audience chooses to engage with it.

2. **Blog-Centric Focus:** Wind is tailored for bloggers, putting the spotlight on your content. Its clean and minimalistic design highlights your articles, providing readers with an uncluttered and immersive reading experience.

3. **Tags Page:** Easily categorize and organize your blog posts using tags. Wind includes a dedicated Tags page that allows your readers to find and explore posts by tag, making content discovery and navigation a breeze.

4. **Disqus Integration:** Engage with your audience through the built-in Disqus commenting system. Enable discussions on your blog posts to encourage interaction, receive feedback, and foster a sense of community.

5. **Customizable Head Section:** Wind empowers you to customize the theme's `<head>` section, enabling you to insert various scripts, such as Google Analytics, social media meta tags, or any other third-party integrations you require to enhance your website's functionality and insights.

6. **Dark Mode:** Wind provides a dark mode feature, allowing readers to switch to a more comfortable reading experience in low-light conditions. Enhance accessibility and cater to different user preferences effortlessly.

7. **Go Up Button:** Enhance user navigation with the "Go Up" button. This feature enables users to quickly return to the top of the page, offering a convenient and user-friendly browsing experience.

8. **Social Media Integration:** Seamlessly link your social media profiles to your blog, making it simple for your readers to connect with you on various platforms. Enhance your online presence and grow your social media following by leveraging Wind's integrated social media links.

9. **SEO Optimized:** Wind is designed with search engine optimization (SEO) in mind. Its clean code, structured metadata, and user-friendly URL structure help improve your blog's visibility on search engines, driving organic traffic to your site.

10. **Cross-Browser Compatibility:** Ensure your blog looks and performs consistently across a wide range of web browsers, providing an optimal experience for all visitors.

11. **Accessibility Features:** Wind adheres to accessibility best practices, ensuring that your content is accessible to users with disabilities. This inclusivity enhances the reach and usability of your blog.

12. **RSS Feed Support:** Wind includes RSS feed support, allowing your readers to subscribe to your blog and receive updates when new content is published.

13. **Author Profile:** Personalize your blog by adding an author profile section, allowing you to share information about yourself and connect with your audience on a more personal level.

## Installation

To use the Wind Jekyll theme as a Ruby Gem in your Jekyll site, follow these steps:

1. **Add Wind Gem to your Gemfile:** Open your Jekyll project's `Gemfile` and add the following line to the `jekyll_plugins` group:
```ruby
gem "wind-theme"
```

2. **Install Gems:** In your project's root directory, run the following command to install the Wind Gem and its dependencies:
```
bundle install
```

3. **Configure Wind Theme:** Open your Jekyll project's _config.yml file, and set the theme key to "wind":
```yalm
theme: wind-theme
```

4. **Use the layouts provided by the theme:** open your index.md or index.markdown page of your jekyll site and put it on the Front Matter section:
```
---
layout: home
---

```

5. **Local Development:** Run the following command to preview your Jekyll site locally:
```
bundle exec jekyll serve
```

## Usage

Wind has been scaffolded by the `jekyll new-theme` command and therefore has all the necessary files and directories to have a new Jekyll site up and running with zero-configuration.

### Layouts

Refers to files within the `_layouts` directory, that define the markup for your theme.

  - `base.html` &mdash; The base layout that lays the foundation for subsequent layouts. The derived layouts inject their
    contents into this file at the line that says ` {{ content }} ` and are linked to this file via
    [FrontMatter](https://jekyllrb.com/docs/frontmatter/) declaration `layout: base`.
  - `home.html` &mdash; The layout for your landing-page / home-page / index-page. [[More Info.](#home-layout)]
  - `page.html` &mdash; The layout for your documents that contain FrontMatter, but are not posts. Example about.md page.
  - `post.html` &mdash; The layout for your posts.

#### Home Layout

`home.html` is a flexible HTML layout for the site's landing-page / home-page / index-page. 

##### *Main Heading and Content-injection*

The *home* layout will inject all content from your `index.md` / `index.html` **before** the **`Posts`** section. This will allow you to include non-posts related content to be published on the landing page under a dedicated heading. *I recommended that you title this section with a Heading2 (`##`)*.

### Includes

Refers to snippets of code within the `_includes` directory that can be inserted in multiple layouts (and another include-file as well) within the same theme-gem.

  - `disqus_comments.html` &mdash; Code to markup disqus comment box.
  - `footer.html` &mdash; Defines the site's footer section.
  - `head.html` &mdash; Code-block that defines the `<head></head>` in *default* layout.
  - `custom-head.html` &mdash; Placeholder to allow users to add more metadata to `<head />`.
  - `header.html` &mdash; Defines the site's main header section. By default, pages with a defined `title` attribute will have links displayed here.
  - `navbar.html` &mdash; Defines the site's navbar section. By default, `title` is used in the left section and main pages are displayed in the rigth section.
  - `up_button.html` &mdash; Includes the code related to the up button.


## Configuration

The template needs at least `title` and `author` settings in your `_config.yml` for works fine. The title is used in the nabvar section and the author is displayed in the posts.

### Enabling comments (via Disqus)

Optionally, if you have a Disqus account, you can tell Jekyll to use it to show a comments section below each post.

:warning: `url`, e.g. `https://example.com`, must be set in you config file for Disqus to work.

To enable it, after setting the url field, you also need to add the following lines to your Jekyll site:

```yaml
  disqus:
    shortname: my_disqus_shortname
```

You can find out more about Disqus' shortnames [here](https://help.disqus.com/installation/whats-a-shortname).

Comments are enabled by default and will only appear in production, i.e., `JEKYLL_ENV=production`

If you don't want to display comments for a particular post you can disable them by adding `comments: false` to that post's YAML Front Matter.

## Customization

To override the default structure and style of minima, simply create the concerned directory at the root of your site, copy the file you wish to customize to that directory, and then edit the file.
e.g., to override the [`_includes/head.html `](_includes/head.html) file to specify a custom style path, create an `_includes` directory, copy `_includes/head.html` from minima gem folder to `<yoursite>/_includes` and start editing that file.

### Plugins

Minima comes with [`jekyll-seo-tag`](https://github.com/jekyll/jekyll-seo-tag) plugin preinstalled to make sure your website gets the most useful meta tags. See [usage](https://github.com/jekyll/jekyll-seo-tag#usage) to know how to set it up.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Support or Contact

If you need help or have questions, you can [contact me](mailto:andres.ch@proton.me).



