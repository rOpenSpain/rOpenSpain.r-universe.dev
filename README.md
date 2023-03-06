# rOpenSpain setup for the r-universe

This repository holds a `packages.json` files
with the packages to be included in the dedicated universe 
[ropenspain.r-universe.dev/](https://ropenspain.r-universe.dev)


Source universe for ropenspain: <https://github.com/r-universe/ropenspain>

Last deployment: <https://ropenspain.r-universe.dev>

## Adding a new package to the r-universe

Just commit to [packages.json](https://github.com/rOpenSpain/universe/blob/master/packages.json) with the following information:

```json

[
  ...
  },

  {
    "package": "name_of_the_package",
    "url": "https://url_of_the_repo",
    "branch" : "optional: name_of_the_branch e.g main",
    "subdir": "optional: name_of_the_subdir"
  },
  
  ...
  
   {
      "package":"opendataes",
      "url":"https://github.com/rOpenSpain/opendataes"
   }
]
```

In a few minutes it would be available on 
<https://ropenspain.r-universe.dev>.  

## Usage

```r

# Enable this universe
options(repos = c(
  ropengov = "https://ropenspain.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))

# Install some packages
install.packages("rostemplate")

# Alternatively a single line
install.packages("rostemplate", repos = c("https://ropenspain.r-universe.dev", "https://cloud.r-project.org"))


```
