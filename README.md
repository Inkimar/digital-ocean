# digital-ocean
an effort to create a docker-project with multiple service like rstudio,dmail,chat and soforth

## rstudio for naturalist-migration
This project  facilitates the running of R-scripts for migrating media-files and data from naturforskaren.se (source) to a mediaserver (target).

### pre-req.
you need to have installed Docker CE (Community Edition) on your system.
https://docs.docker.com/engine/installation/


### Running RStudio in your local browser.
This project pulls down an image from dockerhub ( https://hub.docker.com/r/raquamaps/mirroreum/ ) that makes it possible for you to run rstudio (https://www.rstudio.com/) in your webbrowser.
The benefit comparing to your local installation of RStudio is that you do not have to install all the dependencies ( packages and sometimes system-libraries that may be neccisary)

### how to start RStudio
```
$ make 
```

(The makefile pulls down the 'raquamaps/mirroreum:v0' from dockerhub and runs it)


### login to RStudio (http://localhost:8787/)
```
$ make start-ui 
```

starts a browser (credentials are are found in the Makefile)
After you login,  RStudio will open, on the left-hand side you will see the RStudio-console
The below is the 'greeting message' from the RStudio-console

```
R version 3.4.0 (2017-04-21) -- "You Stupid Darkness"
Copyright (C) 2017 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.
```

**Enter** the following 2 lines of instructions 'library(devtools)' and 'install_github("dina-web/dinar", ref="dev")'

```
> library(devtools)
> install_github("dina-web/dinar", ref="dev")
```

## examine the script and edit
https://github.com/DINA-Web/dinar/blob/dev/exec/media_migrate_examples.R


