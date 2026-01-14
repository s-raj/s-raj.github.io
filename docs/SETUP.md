# Setup and Development Guide

This guide provides detailed instructions for setting up and developing the s-raj.github.io website locally.

## System Requirements

### Minimum Requirements

- **Ruby:** 2.5.0 or higher
- **RubyGems:** Latest version
- **GCC and Make:** For compiling native extensions
- **Git:** For version control
- **Text Editor:** VS Code, Sublime Text, or your preferred editor

### Recommended

- **Ruby:** 2.7.0 or higher
- **Bundler:** 2.x
- **Node.js:** 14.x or higher (for some Jekyll plugins)

## Initial Setup

### 1. Install Ruby

#### On macOS (using Homebrew)

```bash
brew install ruby
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

#### On Ubuntu/Debian

```bash
sudo apt-get update
sudo apt-get install ruby-full build-essential zlib1g-dev
```

#### On Windows

Download and install Ruby from [RubyInstaller](https://rubyinstaller.org/).

### 2. Install Bundler

```bash
gem install bundler
```

### 3. Clone the Repository

```bash
git clone https://github.com/s-raj/s-raj.github.io.git
cd s-raj.github.io
```

### 4. Install Dependencies

```bash
bundle install
```

This will install Jekyll and all required gems specified in the `Gemfile`.

## Running Locally

### Start the Development Server

```bash
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

### Start with Live Reload

```bash
bundle exec jekyll serve --livereload
```

The browser will automatically refresh when you make changes.

### Start with Drafts

```bash
bundle exec jekyll serve --drafts
```

This will include posts from the `_drafts` directory.

### Build for Production

```bash
bundle exec jekyll build
```

The static site will be generated in the `_site` directory.

## Project Structure

### Key Directories

```
s-raj.github.io/
├── _config.yml          # Main configuration file
├── _data/               # Data files (YAML, JSON, CSV)
├── _includes/           # Reusable HTML snippets
├── _layouts/            # Page templates
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── _drafts/             # Draft posts (not published)
├── assets/              # Static files
│   ├── css/            # Stylesheets
│   ├── js/             # JavaScript files
│   └── img/            # Images
├── docs/                # Documentation
└── _site/               # Generated site (git-ignored)
```

### Important Files

- `_config.yml` - Site-wide settings
- `Gemfile` - Ruby dependencies
- `index.html` - Homepage
- `aboutme.md` - About page
- `tags.html` - Tags index page

## Configuration

### Editing Site Settings

Edit `_config.yml` to customize:

- Site title and description
- Author information
- Social media links
- Google Analytics
- Navigation menu
- Theme colors

Example:

```yaml
title: My Home
description: Welcome to my Digital Wall
author: Sharat Raj
url: "https://s-raj.github.io"
```

### Navigation Menu

Update the `navbar-links` section in `_config.yml`:

```yaml
navbar-links:
  About Me: "aboutme"
  Tags: "tags"
  My Blog: "https://blog.s-raj.in"
```

### Social Media Links

Configure social links in `_config.yml`:

```yaml
social-network-links:
  email: "your-email@gmail.com"
  github: username
  linkedin: username
  twitter: username
```

## Creating Content

### Writing a Blog Post

1. Create a new file in `_posts/`:
   ```bash
   touch _posts/2026-01-14-my-new-post.md
   ```

2. Add YAML front matter:
   ```yaml
   ---
   layout: post
   title: "My New Post"
   subtitle: "A brief description"
   date: 2026-01-14
   tags: [tutorial, jekyll]
   comments: true
   ---
   ```

3. Write your content in Markdown below the front matter

4. Save and the local server will automatically rebuild

### Adding a New Page

1. Create a new file in the root directory:
   ```bash
   touch my-page.md
   ```

2. Add YAML front matter:
   ```yaml
   ---
   layout: page
   title: My Page
   ---
   ```

3. Add content in Markdown

4. Optionally add to navigation in `_config.yml`

### Working with Drafts

1. Create a draft in `_drafts/`:
   ```bash
   mkdir -p _drafts
   touch _drafts/my-draft.md
   ```

2. Drafts don't need dates in the filename

3. View drafts with `--drafts` flag:
   ```bash
   bundle exec jekyll serve --drafts
   ```

## Customizing the Theme

### Modifying Styles

1. Custom CSS files go in `assets/css/`
2. Add them to page front matter:
   ```yaml
   css: ["/assets/css/custom.css"]
   ```

### Modifying Layouts

1. Layouts are in `_layouts/`
2. Common layouts:
   - `default.html` - Base template
   - `page.html` - Standard pages
   - `post.html` - Blog posts
   - `home.html` - Homepage

### Adding JavaScript

1. Place JS files in `assets/js/`
2. Reference in page front matter:
   ```yaml
   js: ["/assets/js/custom.js"]
   ```

## Troubleshooting

### Common Issues

#### Bundler Errors

```bash
bundle update
bundle install
```

#### Port Already in Use

```bash
bundle exec jekyll serve --port 4001
```

#### Permission Denied (macOS/Linux)

```bash
sudo bundle exec jekyll serve
```

#### Changes Not Reflecting

1. Stop the server (Ctrl+C)
2. Clear the cache:
   ```bash
   bundle exec jekyll clean
   ```
3. Restart the server

### Dependency Issues

If you encounter gem dependency issues:

```bash
rm Gemfile.lock
bundle install
```

## Deployment

### GitHub Pages Deployment

The site automatically deploys when you push to the `master` branch:

```bash
git add .
git commit -m "Your commit message"
git push origin master
```

GitHub Pages will build and deploy the site within a few minutes.

### Manual Deploy

If needed, you can build and deploy manually:

```bash
# Build the site
bundle exec jekyll build

# The _site directory contains the generated site
# Upload contents to your web server
```

## Testing

### Link Checking

Install html-proofer:

```bash
gem install html-proofer
```

Test your site:

```bash
bundle exec jekyll build
htmlproofer ./_site
```

### Accessibility Testing

Use browser developer tools or online services:
- [WAVE Web Accessibility Tool](https://wave.webaim.org/)
- Chrome Lighthouse
- Firefox Accessibility Inspector

## Performance Optimization

### Image Optimization

- Use appropriate image formats (WebP, JPEG, PNG)
- Compress images before uploading
- Use responsive images with `srcset`

### Caching

- Jekyll automatically minifies HTML
- Enable caching in hosting configuration

### Analytics

Monitor site performance with:
- Google Analytics (configured in `_config.yml`)
- Google Search Console
- PageSpeed Insights

## Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Beautiful Jekyll Theme](https://beautifuljekyll.com/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)

## Getting Help

If you encounter issues:

1. Check the [Jekyll Troubleshooting](https://jekyllrb.com/docs/troubleshooting/) guide
2. Search [Jekyll Talk forum](https://talk.jekyllrb.com/)
3. Review the [Beautiful Jekyll documentation](https://beautifuljekyll.com/)
4. Open an issue on GitHub

---

Happy coding! 🚀
