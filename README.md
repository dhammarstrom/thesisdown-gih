# thesisdowngih

This is a fork from the [thesisdown](https://github.com/ismayc/thesisdown) project. Modification has been made to meet requirements of doctoral theses presented at the [Swedish School of Sport and Health Sciences (GIH)](http://www.gih.se).

The pdf is functional. The thesis can also be compiled to a gitbook without any apperent problems.

The thesisdown documentation may be to your assitance! Please read over the documentation available in the `gitbook` template at https://thesisdown.netlify.com/.  This is also available below at http://ismayc.github.io/thesisdown_book.

Authoring is done in [markdown](http://rmarkdown.rstudio.com/authoring_basics.html) syntax, and **R** code and its output can be seamlessly included using [rmarkdown](http://rmarkdown.rstudio.com).


### Using [thesisdown](https://github.com/ismayc/thesisdown)

The following instructions apply to the thesisdowngih version also.

Using **thesisdown** has some prerequisites which are described below. To compile PDF documents using **R**, you are going to need to have LaTeX installed.  It can be downloaded for Windows at <http://http://miktex.org/download> and for Mac at <http://tug.org/mactex/mactex-download.html>.  Follow the instructions to install the necessary packages after downloading the (somewhat large) installer files.  You may need to install a few extra LaTeX packages on your first attempt to knit as well.

To use **thesisdown** from RStudio:

1) Install the latest [RStudio](http://www.rstudio.com/products/rstudio/download/).
Only the version as of Oct 2017 has a recent enough Pandoc included so you may need to upgrade this
separately or install a newer RStudio.

    ```r
    rmarkdown::pandoc_available("1.2")
    #> [1] TRUE
    ```

2) Install the **bookdown** and **thesisdowngih** packages: 

```
install.packages("devtools")
devtools::install_github("rstudio/bookdown")
devtools::install_github("dhammarstrom/thesisdowngih")
```

3) Use the **New R Markdown** dialog to select **Thesis**:

    Note that this will currently only **Knit** if you name the directory `index` as shown above.

4) After choosing which type of output you'd like in the YAML at the top of index.Rmd, **Knit** the `index.Rmd` file to get the book in PDF or HTML formats.
5) Edit the individual chapter R Markdown files as you wish and then re-run step (4) again.
