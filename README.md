# Install homebrew
```{r, engine = 'bash', eval = FALSE}
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

# Seascape_genomics_packages
Useful software and programs to perform seascape genomics analyses

## Make sure you will have all Xcode packages updated and available in your machine
```{r, engine = 'bash', eval = FALSE}
brew update
brew upgrade
xcode-select --install
brew install libgit2
pip3 install pygit2
brew install libxml2
brew install gsl 
brew install gcc
brew install gdal
brew install oracle-jdk --cask
brew install pkg-config
brew install libgd
```

## Install [CMAKE] https://cmake.org/download/

## Install [VCFTOOLS](http://vcftools.sourceforge.net/)
VCFtools is a program package designed for working with VCF files, such as those generated by [STACKS](http://catchenlab.life.illinois.edu/stacks/).
```{r, engine = 'bash', eval = FALSE}
brew install vcftools
```

## Install [PLINK](http://zzz.bwh.harvard.edu/plink/download.shtml)
PLINK is a free, open-source whole genome association analysis toolset, designed to perform with tfam and tped files that are easily converted from vcftools via the ***plink-tped*** following command:
```{r, engine = 'bash', eval = FALSE}
vcftools --vcf nameofyourfile.vcf --plink-tped --out nameofyourfile
done
```

## Install JAVA
```{r, engine = 'bash', eval = FALSE}
brew install java
brew info java
```

## Install [PGDSpider](http://www.cmpg.unibe.ch/software/PGDSpider/)
PGDSpider is a data conversion tool for population genetic and genomics programs. 
It support a vast range of data types with the ability of parsing 33 and writing 36 different file formats

### Install Miniconda

```{r, engine = 'bash', eval = FALSE}
mkdir -p ~/miniconda3
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh -o ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```

## Install [ADMIXTURE](http://software.genetics.ucla.edu/admixture/)
ADMIXTURE is a software tool for maximum likelihood estimation of individual ancestries from multilocus SNP genotype datasets. It uses the same statistical model as STRUCTURE but calculates estimates much more rapidly using a fast numerical optimization algorithm.
```{r, engine = 'bash', eval = FALSE}
conda install bioconda::admixture
```

## Install [R studio](https://www.rstudio.com/products/rstudio/download/)
R studio has developped an integrated development environment for R, with a console that supports direct code execution.

```{r, engine = 'bash', eval = FALSE}
brew install xquartz
brew install r
brew install --appdir=/Applications rstudio
```

## Install [BayeScan](http://cmpg.unibe.ch/software/BayeScan/download.html) 
Bayescan is a command line based open source software that aim to detect natural selection from population based genetic data.

## Install [SamBada](https://www.epfl.ch/labs/lasig/page-101934-en-html/sambada/)
Samβada is an integrated software for landscape genomic analysis of large datasets.

## LOG IN to the cloud 
All explanations on how to log in to the cloud are indicated in this [link](https://speciationgenomics.github.io/logging_on/).

All softwares (except R and the PR packages required for the class) will be available on the cloud.

## R software: install R packages 
First install devtools package that allows you to directly download R package available in github.
```{r}
install.packages("devtools")
```

Then, a variety of useful package for performing relevant analyses in a context of seascape genomic class are avaible in R: population genomics index, filtering SNPs, hierarchical analyses, multivariate analysis etc.

### For lecture 1 to 5

```{r}
install.packages("ggmap")
install.packages("ggplot2")
install.packages("raster")
install.packages("ggsn")
install.packages("rnaturalearth")
install.packages("rnaturalearthdata")
install.packages("seqinr")
install.packages("visreg")
install.packages("qvalue")
install.packages("data.table")
install.packages("gdistance")
install.packages("dismo")
install.packages("vegan")
install.packages("reshape2")
install.packages("dplyr")
install.packages("adespatial")
install.packages("ade4")
install.packages("spdep")
install.packages("codep")
install.packages("adegraphics")
install.packages("ape")
install.packages("car")
install.packages("sp")
install.packages("marmap")
install.packages("viridis") 
install.packages('terra', configure.args = '--with-gdal-config=/opt/homebrew/bin/gdal-config --with-geos-config=/opt/homebrew/Cellar/geos/3.11.0/bin/geos-config --with-proj-include=/opt/homebrew/Cellar/proj/9.1.0/include --with-proj-lib=/opt/homebrew/Cellar/proj/9.1.0/lib', configure.vars = 'GDAL_DATA=/opt/homebrew/opt/gdal/share/gdal/')
install.packages('sf', configure.args = '--with-gdal-config=/opt/homebrew/bin/gdal-config --with-geos-config=/opt/homebrew/Cellar/geos/3.11.0/bin/geos-config --with-proj-include=/opt/homebrew/Cellar/proj/9.1.0/include --with-proj-lib=/opt/homebrew/Cellar/proj/9.1.0/lib', configure.vars = 'GDAL_DATA=/opt/homebrew/opt/gdal/share/gdal/')
```

### For lecture 6 to 8
```{r}
if (!require("devtools")) install.packages("devtools")
devtools::install_github("thierrygosselin/radiator")
install.packages(c("ggplot2","gridExtra","gtable","label.switching","tidyr","devtools"),dependencies=T)
devtools::install_github('royfrancis/pophelper')
install.packages("poppr")
install.packages("adegenet")
install.packages("assigner")
install.packages("pcadapt")
install.packages("vcfR")
install.packages("plyr")
```

Verify that package gdsfmt was installed and that you have package SeqArray version >= 1.28.1.
```{r}
devtools::package_info(pkgs = "SeqArray")
```

Some packages are best downloaded using github:
```{r}
library("devtools")
install_github("jdstorey/qvalue")
devtools::install_github("whitlock/OutFLANK")
```
