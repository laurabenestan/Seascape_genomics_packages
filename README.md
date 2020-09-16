# Seascape_genomics_packages
Useful software and programs to perform seascape genomics analyses

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
brew cask install java
brew cask info java
```

## Install [PGDSpider](http://www.cmpg.unibe.ch/software/PGDSpider/)
PGDSpider is a data conversion tool for population genetic and genomics programs. 
It support a vast range of data types with the ability of parsing 33 and writing 36 different file formats


## Install [ADMIXTURE](http://software.genetics.ucla.edu/admixture/)
ADMIXTURE is a software tool for maximum likelihood estimation of individual ancestries from multilocus SNP genotype datasets. It uses the same statistical model as STRUCTURE but calculates estimates much more rapidly using a fast numerical optimization algorithm.
To use ADMIXTURE, you need to transfor your file vcf file into a bed format via plink by typing the ***make-bed*** command available in PLINK:
```{r, engine = 'bash', eval = FALSE}
plink --tfam nameofyourfile.tfam --tped nameofyourfile.tped --make-bed --out nameofyourfile
done
```

## Install [R studio](https://www.rstudio.com/products/rstudio/download/)
R studio has developped an integrated development environment for R, with a console that supports direct code execution.

```{r, engine = 'bash', eval = FALSE}
brew cask install xquartz
brew cask install r
brew cask install --appdir=/Applications rstudio
```

## Install [BayeScan](http://cmpg.unibe.ch/software/BayeScan/download.html) 
Bayescan is a command line based open source software that aim to detect natural selection from population based genetic data.

## R software: install R packages 
First install devtools package that allows you to directly download R package available in github.
```{r}
install.packages("devtools")
```

Then, a variety of useful package for performing relevant analyses in a context of seascape genomic class are avaible in R: population genomics index, filtering SNPs, hierarchical analyses, multivariate analysis etc.

### For lecture 4: Characterize seascape configuration: spatial distribution and ocean transports you will need:

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
install.packages("rgdal")
install.packages("maptools")
install.packages("gdistance")
install.packages("dismo")
install.packages("vegan")
install.packages("reshape2")
install.packages("dplyr")
install.packages("SoDA")
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
```

### For lecture 6: Genomic data preparation + preliminary analyses
```{r}
if (!require("devtools")) install.packages("devtools")
devtools::install_github("thierrygosselin/radiator")
install.packages(c("ggplot2","gridExtra","gtable","label.switching","tidyr","devtools"),dependencies=T)
devtools::install_github('royfrancis/pophelper')
install.packages("poppr")
install.packages("adegenet")
install.packages("assigner")
```

Verify that package gdsfmt was installed and that you have package SeqArray version >= 1.28.1.
```{r}
devtools::package_info(pkgs = "SeqArray")
```

### For lecture 7: Outlier detection
```{r}
install.packages("pcadapt")
install.packages("pcadapt") 
install.packages("vcfR")
install.packages("plyr")
install.packages('qvalue')
```
