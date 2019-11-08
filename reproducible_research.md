# Reproducible research

To guarantee that all research is reproducible, code must be organized as a package. 
[Here](http://rmflight.github.io/posts/2014/07/analyses_as_packages.html) is the briefest explanation why it's a good idea.
More comprehensive explanations can be found by "research compendium" keyword ([rrrpkg](https://github.com/ropensci/rrrpkg) has a 
good description).

## Good practices

The very least one can do to preserve proper folder structure to store your data and results. Article 
["Stop the working directory insanity"](https://gist.github.com/jennybc/362f52446fe1ebc4c49f) has a detailed explanation of the
problem. To solve this problem without any overhead I propose [dataorganizer](https://github.com/khodosevichlab/dataorganizer)
package.

## Resources

- [Reproducible Researchwith R and RStudio](https://englianhu.files.wordpress.com/2016/01/reproducible-research-with-r-and-studio-2nd-edition.pdf):
  book is a bit out of date, but still is the best source of basic concepts I'm aware of (@vpetukhov)
- [Research Compendium](https://research-compendium.science/): collection of information on reproducible research
- [R Packages](http://r-pkgs.had.co.nz/) online book from Hadley Wickham
- [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/). All you need to know about R Markdown.
