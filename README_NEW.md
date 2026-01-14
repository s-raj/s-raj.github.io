# Sharat Raj's Personal Website

[![Website](https://img.shields.io/website?url=https%3A%2F%2Fs-raj.github.io)](https://s-raj.github.io)
[![GitHub](https://img.shields.io/github/license/s-raj/s-raj.github.io)](LICENSE)

Welcome to the repository for my personal website and blog, hosted at [s-raj.github.io](https://s-raj.github.io). This site serves as my digital presence, showcasing my work, thoughts, and projects.

## About

This is a personal website built with [Jekyll](https://jekyllrb.com/) and the [Beautiful Jekyll](https://beautifuljekyll.com/) theme. The site is hosted on GitHub Pages and automatically deployed when changes are pushed to the repository.

**Website Owner:** Sharat Raj  
**Location:** Ponnani, Kerala (Arabian Sea coast)  
**Profession:** Engineer in the Automotive sector, contributing to autonomous commercial vehicles

## Website Structure

### Main Pages

- **Home** (`index.html`) - Landing page with blog posts feed
- **About Me** (`aboutme.md`) - Personal introduction and background
- **Calendar** (`calendar.md`) - Personal calendar integration
- **Tags** (`tags.html`) - Blog posts organized by tags

### Blog Posts

Blog posts are located in the `_posts` directory and follow Jekyll's naming convention: `YYYY-MM-DD-title.md`. Current posts include:

- Corona Days series documenting experiences during the pandemic

### Configuration

The site is configured through `_config.yml` with the following key settings:

- **Site Title:** My Home
- **Description:** Welcome to my Digital Wall
- **Author:** Sharat Raj
- **Domain:** s-raj.in
- **Google Analytics:** UA-167045605-1

### Navigation Links

The site includes links to:

- Slack channel for communication
- Grafana Dashboard for monitoring
- Personal projects:
  - Personalised News Email
  - Twitter Bot
- Personal blog at blog.s-raj.in

## Technology Stack

- **Static Site Generator:** Jekyll
- **Theme:** Beautiful Jekyll
- **Hosting:** GitHub Pages
- **Domain:** Custom domain (s-raj.in)
- **Analytics:** Google Analytics
- **Frontend:** Bootstrap 4, HTML5, CSS3, JavaScript

## Directory Structure

```
.
├── _config.yml           # Site configuration
├── _data/                # Data files for Jekyll
├── _includes/            # Reusable HTML components
├── _layouts/             # Page layouts
├── _posts/               # Blog posts
├── assets/               # Static assets (CSS, JS, images)
│   ├── css/
│   ├── img/
│   └── js/
├── docs/                 # Documentation
├── aboutme.md            # About page
├── calendar.md           # Calendar page
├── index.html            # Home page
├── tags.html             # Tags index
└── README.md             # This file
```

## Local Development

### Prerequisites

- Ruby (version 2.5 or higher)
- RubyGems
- GCC and Make

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/s-raj/s-raj.github.io.git
   cd s-raj.github.io
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Run the local server:
   ```bash
   bundle exec jekyll serve
   ```

4. Visit `http://localhost:4000` in your browser

### Development Tips

- Blog posts must include YAML front matter
- Follow the naming convention `YYYY-MM-DD-title.md` for posts
- Images should be placed in `assets/img/`
- Test locally before pushing changes

## Adding Content

### Creating a New Blog Post

1. Create a new file in `_posts/` with the format `YYYY-MM-DD-post-title.md`
2. Add YAML front matter at the top:
   ```yaml
   ---
   layout: post
   title: Your Post Title
   subtitle: Optional subtitle
   tags: [tag1, tag2]
   comments: true
   ---
   ```
3. Write your content in Markdown
4. Commit and push to deploy

### Adding a New Page

1. Create a new `.md` or `.html` file in the root directory
2. Add YAML front matter:
   ```yaml
   ---
   layout: page
   title: Page Title
   ---
   ```
3. Add the page to navigation in `_config.yml` if desired

## Deployment

The site is automatically deployed to GitHub Pages when changes are pushed to the `master` branch. GitHub Actions handles the build process.

**Live Site:** [https://s-raj.github.io](https://s-raj.github.io)  
**Custom Domain:** [https://s-raj.in](https://s-raj.in)

## Customization

To customize the site appearance and behavior, edit `_config.yml`. Key customizable features:

- Site colors and theme
- Navigation links
- Social media links
- Avatar image
- Google Analytics
- Comments (Disqus, Utterances, etc.)

For more detailed theme customization options, see [docs/THEME.md](docs/THEME.md).

## Contributing

While this is a personal website, suggestions and bug reports are welcome! Please feel free to:

1. Open an issue for bugs or suggestions
2. Submit a pull request for fixes

See [CONTRIBUTING.md](CONTRIBUTING.md) for more details.

## License

The website theme (Beautiful Jekyll) is licensed under the MIT License - see [LICENSE](LICENSE) for details.

The content (blog posts, personal information, images) is copyrighted by Sharat Raj.

## Contact

- **Email:** jartarahs@gmail.com
- **GitHub:** [@s-raj](https://github.com/s-raj)
- **LinkedIn:** [sharatraj](https://www.linkedin.com/in/sharatraj)
- **Website:** [s-raj.in](https://s-raj.in)
- **Blog:** [blog.s-raj.in](https://blog.s-raj.in)

## Acknowledgments

- Theme by [Dean Attali](https://deanattali.com) - [Beautiful Jekyll](https://beautifuljekyll.com/)
- Hosted on [GitHub Pages](https://pages.github.com/)
- Built with [Jekyll](https://jekyllrb.com/)
