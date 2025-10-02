---
title: Setup
---

::: instructor

- The main goal here is to help the learners be comfortable with the RStudio
  interface.
- Go very slowly in the "Getting set up" section. Make sure everyone is following
  along (remind learners to use the stickies). Plan with the helpers at this
  point to go around the room, and be available to help. It's important to make
  sure that learners are in the correct working directory, and that they create
  a `data` (all lowercase) subfolder.

::::::::::::

## Data Sets

<!--
FIXME: place any data you want learners to use in `episodes/data` and then use
       a relative link ( [data zip file](data/lesson-data.zip) ) to provide a
       link to it, replacing the example.com link.
-->
Download the [data zip file](https://example.com/FIXME) and unzip it to your Desktop

## Setup instructions

Coding exercises for this lesson can either be done 1) on your own computer using R and R studio, or 2) using a Jupyter Notebook with an R Kernel on the Du Bois Cloud.

Using Notebooks on the Du Bois cloud does not require any set up or installation. You can simply follow hyperlinks provided in this lesson that will open a Notebook in any web browser.

For those who want to do more data visualization and work with R beyond this lesson, we recommend using R and R studio. If you have not yet installed R and R studio, you can do so by following the instructions below. 

**R** and **RStudio** are separate downloads and installations. R is the
underlying statistical computing environment, but using R alone is no
fun. RStudio is a graphical integrated development environment (IDE) that makes
using R much easier and more interactive. You need to install R before you
install RStudio. Once installed, because RStudio is an IDE, RStudio will run R in
the background.  You do not need to run it separately.

After installing both programs,
you will need to install the **`tidyverse`** package from within RStudio. The
**`tidyverse`** package is a powerful collection of data science tools within **R**
see the [**`tidyverse`** website](https://tidyverse.tidyverse.org) for more details.
Follow the instructions below for your operating system, and then follow the
instructions to install **`tidyverse`**.

### Windows

#### If you already have R and RStudio installed

- Open RStudio, and click on "Help" > "Check for updates". If a new version is
  available, quit RStudio, and download the latest version for RStudio.
- To check which version of R you are using, start RStudio and the first thing
  that appears in the console indicates the version of R you are
  running. Alternatively, you can type `sessionInfo()`, which will also display
  which version of R you are running. Go on
  the [CRAN website](https://cran.r-project.org/bin/windows/base/) and check
  whether a more recent version is available. If so, you can update R using
  the `installr` package, by running:

```r
if( !("installr" %in% installed.packages()) ){install.packages("installr")}
installr::updateR(TRUE)
```

#### If you don't have R and RStudio installed

- Download R from
  the [CRAN website](http://cran.r-project.org/bin/windows/base/release.htm).
- Run the `.exe` file that was just downloaded.
- Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/).
- Under *Installers* select **RStudio x.yy.zzz - Windows.
  Vista/7/8/10** (where x, y, and z represent version numbers).
- Double click the file to install it.
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

### macOS

#### If you already have R and RStudio installed

- Open RStudio, and click on "Help" > "Check for updates". If a new version is
  available, quit RStudio, and download the latest version for RStudio.
- To check the version of R you are using, start RStudio and the first thing
  that appears on the terminal indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on
  the [CRAN website](https://cran.r-project.org/bin/macosx/) and check
  whether a more recent version is available. If so, please download and install
  it. In any case, make sure you have at least R 3.2.

#### If you don't have R and RStudio installed

- Download R from
  the [CRAN website](http://cran.r-project.org/bin/macosx/).
- Select the `.pkg` file for the latest R version.
- Double click on the downloaded file to install R.
- It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed
  by some packages).
- Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/).
- Under *Installers* select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)**
  (where x, y, and z represent version numbers).
- Double click the file to install RStudio.
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

### Linux

- Follow the instructions for your distribution
  from [CRAN](https://cloud.r-project.org/bin/linux), they provide information
  to get the most recent version of R for common distributions. For most
  distributions, you could use your package manager (e.g., for Debian/Ubuntu run
  `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
  don't recommend this approach as the versions provided by this approach are
  usually out of date. In any case, make sure you have at least R 3.2.
- Go to the
  [RStudio download page](https://posit.co/download/rstudio-desktop/).
- Under *Installers* select the version that matches your distribution, and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-x.yy.zzz-amd64.deb` at the terminal).
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.
- Before installing the `tidyverse` package, **Ubuntu** (and related) users may
  need to install the following dependencies: `libcurl4-openssl-dev libssl-dev libxml2-dev`
  (e.g. `sudo apt install libcurl4-openssl-dev libssl-dev libxml2-dev`).

### For everyone

**After installing R and RStudio, you need to install the `tidyverse` and `here` packages.**

- After starting RStudio, at the console type:
  `install.packages("tidyverse")` followed by the enter key. Once this has installed, type
  `install.packages("here")` followed by the enter key. Both packages should now be installed.

- For reference, the lesson uses `SAFI_clean.csv`. The direct download link for
  this file is: [https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI_clean.csv](https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI_clean.csv).
  This data is a slightly cleaned up version of the SAFI Survey Results available on
  [figshare](https://figshare.com/articles/dataset/SAFI_Survey_Results/6262019).
  Instructions for downloading the data with R are provided in the
  [Before we start episode](https://datacarpentry.org/r-socialsci/00-intro.html).

- The [json episode](https://datacarpentry.org/r-socialsci/07-json.html) uses
  `SAFI.json`. The file is available on GitHub
  [here](https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI.json).
