[![standard-libraries-now](assets/banner.svg)](https://github.com/watanabe3tipapa/standard-libraries-now)

<!-- badges -->
[![Deployment](https://img.shields.io/github/deployments/watanabe3tipapa/standard-libraries-now/github-pages)](https://github.com/watanabe3tipapa/standard-libraries-now/deployments)

[English](README.md) | [日本語](README_ja.md)

# standard-libraries-now

A daily-updated index of standard libraries for Node.js, Python, Rust, Go, and Tauri. The data is crawled automatically every morning and published as a static site.

Live site: https://watanabe3tipapa.github.io/standard-libraries-now/

## Table of contents

- About
- Features
- Live preview
- Repository structure
- Installation
- Usage
- Contributing
- Development & maintenance
- License
- Contact

## About

standard-libraries-now provides a consolidated, daily-refreshed listing of standard libraries across multiple languages. The project publishes the collected data as a static website.

## Features

- Daily crawling — GitHub Actions runs at 5:00 JST and refreshes the library data automatically
- Contains entries for 5 languages (Node.js / Python / Rust / Go / Tauri) and around 670 modules
- Single-page drill-down UI — expand language → category → module, implemented using native HTML `<details>` / `<summary>` (no JavaScript)
- Neo Brutalism design — flat cards, thick black borders, and neon accents

## Live preview

![Screenshot](assets/IMGSS.jpg)

Visit the live site: https://watanabe3tipapa.github.io/standard-libraries-now/

## Repository structure (selected)

The repository includes the following top-level items (selection):

- assets/ — images and static assets used by the site
- crawler/ — code and dependencies used to crawl and collect library data
- site/ — static site source and build files
- data/ — generated data used by the site
- package.json — project scripts (see Installation / Usage)

## Installation

Clone the repository and install dependencies for the crawler and site:

```bash
# Clone the repository
git clone https://github.com/watanabe3tipapa/standard-libraries-now.git

# Install crawler dependencies
cd crawler
npm install

# Install site dependencies
cd ../site
npm install
```

## Usage

The top-level package.json provides three scripts that coordinate the pipeline:

```bash
# Run the full pipeline (crawl + build)
npm run run

# Crawl all languages only
npm run crawl

# Build the static site only
npm run build
```

(The above scripts invoke commands in the crawler/ and site/ subfolders.)

## Contributing

Contributions are welcome. A suggested flow:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Development & maintenance

- The repository is not archived.
- The site data is updated automatically on a daily schedule (GitHub Actions run at 5:00 JST as noted in project documentation).
- The project publishes a static site; deployment status is visible via the repository deployment badge.

## License

License not yet specified.

## Contact

Repository: https://github.com/watanabe3tipapa/standard-libraries-now

Homepage: https://watanabe3tipapa.github.io/standard-libraries-now/
