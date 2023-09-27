# Documentation Site for AIROU
This is a wiki where the documentation for the AIROU Lab lives. The intention is for this site to be a living document, where project information, setup, and past instructions can live.

This is built using [mdBook](https://rust-lang.github.io/mdBook/index.html), a Rust-based 

Link to Documentation:
https://airou-lab.github.io/air-lab-documentation/

## Starter Guide
This documentation is configured to auto-deploy when commits are made to the `main` branch. This is done via GitHub Actions.

To edit the site, just edit the `.md` files within the `src` directory. The site will automatically render the Markdown files and structure the website according to the structure of the `src` folder.

If you want to just edit the site within the GitHub web interface, you can edit the Markdown files and view a preview. Then just commit your changes and the website will be updated.

Each page is written using Markdown files, so you can embed images, add sections etc. like a normal markdown file. [The mdBook docs has instructions for editing MD](https://rust-lang.github.io/mdBook/format/markdown.html).
