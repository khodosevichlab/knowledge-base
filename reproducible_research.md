# Reproducible research

To guarantee that all research is reproducible, code must be organized as a package. 
[Here](http://rmflight.github.io/posts/2014/07/analyses_as_packages.html) is the briefest explanation why it's a good idea.
More comprehensive explanations can be found by "research compendium" keyword ([rrrpkg](https://github.com/ropensci/rrrpkg) has a 
good description).

## Good practices

The very least one can do to preserve proper folder structure to store your data and results. Article 
["Stop the working directory insanity"](https://gist.github.com/jennybc/362f52446fe1ebc4c49f) has a detailed explanation of the
problem. To solve this problem without any overhead I propose [dataorganizer](https://github.com/khodosevichlab/dataorganizer)
package. [Here](https://devtools.r-lib.org/) is a brief guide on how to develop packages in RStudio.

### Package structure

- All functions are stored in .R files inside "R/" folder maybe with **rare** exception of single-use functions
- All analysis is performed in .Rmd files in either "vignette" or "analysis" folders, grouped by subfolders with meaningful names
- If you re-use (e.g. copy-paste) the same code more than twice, move it to a function
- If your chunk takes longer than 10 lines, create a function with a proper name to understand what's going on (except chunks with data loading)
- After you get important result, commit all changes in "R/" and in your current .Rmd notebook **right away**.
- Avoid writing functions longer than 50 lines and with nesting level > 3. If it's the case, consider extracting sub-functions.
- Try to organize your code and data hierarchically: use subfolders for both notebooks and data files
- Though clean code is nice, don't be ashamed to store dirty code in your private repository: it's much better than not to store at all
- Please document your functions for an R package, both for yourself in the future and for sharing work with others. This is done via [roxygen2](https://github.com/r-lib/roxygen2). Trust me, you'll thank yourself later.

### Code style

In our packages I suggest the following code style (*it's fine to have different in your analysis, as far as it's consistent for the whole project*):
1. All functions are [lowerCamelCase](https://en.wikipedia.org/wiki/Camel_case). See [here](https://style.tidyverse.org/syntax.html#object-names) why naming functions with dots is a bed idea (tldr: R uses dots for S3 functions)
2. All variables are lower case with dot as a separator (e.g. "n.pcs" or "count.matrix")
3. All files are named in a [snake case](https://en.wikipedia.org/wiki/Snake_case) with capital R as the extension (e.g. utility_functions.R)
4. Spaces around matrix operations, but not around function parameters (e.g. "x + 2 / 3" or "f(x=1, y=(2 / 3))")
5. Parentheses are required everywhere except one-line "return" or "stop" statements or short messages (i.e. "message" or "cat")

Indeed, there are many style guides for R. One of the most popular is the [Hadley Wickham's](http://adv-r.had.co.nz/Style.html). But these guides are constantly changed, so there is no "best" option.

## Resources

- [Reproducible Research with R and RStudio](https://englianhu.files.wordpress.com/2016/01/reproducible-research-with-r-and-studio-2nd-edition.pdf):
  book is a bit out of date, but still is the best source of basic concepts I'm aware of (@vpetukhov)
- [Research Compendium](https://research-compendium.science/): collection of information on reproducible research
- [R Packages](http://r-pkgs.had.co.nz/) online book from Hadley Wickham
- [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/). All you need to know about R Markdown.
- [devtools](https://devtools.r-lib.org/): developing packages in RStudio
- [roxygen2](https://github.com/r-lib/roxygen2): documenting functions for other users in R packages. 
