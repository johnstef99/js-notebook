# JS-Notebook

[website](https://notebook.johnstef.com)

## Requirements

- [R](https://www.r-project.org/)
  - [rmarkdown](https://cran.r-project.org/web/packages/rmarkdown/index.html)
  - (optional)
    [rsconnect](https://cran.r-project.org/web/packages/rsconnect/index.html)
    for publishing website to Rstudio Connect
  - (optional) [colorout](https://github.com/jalvesaq/colorout) colorizes
    R output when running in a Unix
- [pandoc](https://pandoc.org/)

## Usage

Run `R` in your terminal inside this folder, that should source the local
`.Rprofile` that loads necessary libraries. In `R` type:

```{r}
rmarkdown::render_site()
```
website is stored inside the `_site` folder

## My Workflow

1) Run tmux and create a pane runs
   [browser-sync](https://github.com/BrowserSync/browser-sync) `cd _site &&
   browser-sync --watch`, that will refresh automatically every time I render
   the site
2) I use vim as my texteditor and automatically runs `render_site()` on file
   saving
3) Publish website to my own Rstudio Connect server using
   `rmarkdown::publish_site()`

### Vim Setup
Plugins:
```
Plug 'jalvesaq/Nvim-R'
Plug 'vim-pandoc/vim-pandoc'
Plug 'vim-pandoc/vim-pandoc-syntax'
```

### How to setup your RsConnect Server

[Guide](https://docs.rstudio.com/rsc/installation/)
