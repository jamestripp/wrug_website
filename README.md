# Warwick R User Group Website

Warwick R User Group website, created using [`Distill`](https://pkgs.rstudio.com/distill/index.html)

## Installation

1. Clone this repo: `git clone git@github.com:WarwickRUG/wrug_website.git`
2. Install `renv` if not already installed (instructions [here](https://rstudio.github.io/renv/index.html)).
2. Run `renv::restore()` to restore the state of your project from `renv.lock`.

## Updating packages

1. Install packages as usual.
2. Run `renv::snapshot()` to update `renv.lock`.
3. Create a commit with `renv.lock` changes and push it to the repo.


## Troubleshooting

If facing issues installing packages from Windows, run this command. (more info [in `renv` documentation](https://rstudio.github.io/renv/articles/renv.html#downloads-1) and [in this discussion](https://community.rstudio.com/t/cant-install-packages-with-renv/96696/6))

```R
Sys.setenv(RENV_DOWNLOAD_METHOD = "libcurl")
```
