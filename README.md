# Warwick R User Group Website
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-3-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Warwick R User Group website, created using [`Distill`](https://pkgs.rstudio.com/distill/index.html)

## Installation

1. Clone this repo: `git clone git@github.com:WarwickRUG/wrug_website.git`
2. Install `renv` if not already installed (instructions [here](https://rstudio.github.io/renv/index.html)).
2. Run `renv::restore()` to restore the state of your project from `renv.lock`.

## Updating packages

1. Install packages as usual.
2. Run `renv::snapshot()` to update `renv.lock`.
3. Create a commit with `renv.lock` changes and push it to the repo.

## Updating website

### Content creation

Add new blog posts

1. Create a new blog post by running `distill::create_post("<date_your title>", draft = TRUE)` where `<date_your title>` will be replaced with an actual date in yyy-mm-dd format and any meaningful title which will be the blog post's url.
2. Edit content as a regular Rmd file (refer to https://rstudio.github.io/distill/blog.html#creating-a-post for more information)
3. Once you are happy with the results:
  1. change `draft = TRUE` to `draft = FALSE` (or just comment the line) so the post can be displayed.
  2. knit the Rmd file: `knitr::knit(<your filename>)` or use RStudio's interface.
  
Edit an existing blog post

1. Edit the desired post within `_posts``folder
2. Save changes
3. Knit the file


### Rendering and deploying the website

1. run `rmarkdown::render_site()` to render a local copy of the website. (this will only deploy any rendered site)
2. website deployment will depend on what we decide in [this issue](https://github.com/WarwickRUG/wrug_website/issues/2)

## Troubleshooting

### Can't install a new package

If facing issues installing packages from Windows, run this command. (more info [in `renv` documentation](https://rstudio.github.io/renv/articles/renv.html#downloads-1) and [in this discussion](https://community.rstudio.com/t/cant-install-packages-with-renv/96696/6))

```R
Sys.setenv(RENV_DOWNLOAD_METHOD = "libcurl")
```

### I can't see my updated content

Make sure that you knit your content after editing your `.Rmd` file, otherwise, it will not show in the new site when rendering and deploying the site. The advantage of this approach is that older blog posts don't break if you update your R packages or dependencies and don't want to update the posts. If you don't fancy re-knitting every time you make a change, then you can write an ordinary markdown post

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://carloscamara.es/en"><img src="https://avatars.githubusercontent.com/u/706549?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Carlos Cámara</b></sub></a><br /><a href="https://github.com/WarwickRUG/wrug_website/commits?author=ccamara" title="Code">💻</a> <a href="#projectManagement-ccamara" title="Project Management">📆</a></td>
    <td align="center"><a href="https://www.heatherturner.net/"><img src="https://avatars.githubusercontent.com/u/3343008?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Heather Turner</b></sub></a><br /><a href="#question-hturner" title="Answering Questions">💬</a></td>
    <td align="center"><a href="https://selbydavid.com"><img src="https://avatars.githubusercontent.com/u/7850509?v=4?s=100" width="100px;" alt=""/><br /><sub><b>David Selby</b></sub></a><br /><a href="#question-Selbosh" title="Answering Questions">💬</a> <a href="#content-Selbosh" title="Content">🖋</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!