# Statistical analyses and visualization in R

## Introduction
The data was analyzed by creating combined data from Gapminder (Ref. 1). The data was downloaded in the form of CSV files for the population, Human Development Index (HDI), Income per person (Income), Life Expectancy (LifeExp), The Sustainable Development Index (SDI), Region and Income Group of various countries. These parameters are defined as follows:

**Population**: Data for the population was downloaded from Gapminder population data (Ref. 2).  
**Human Development Index (HDI)**: HDI is used to rank various countries by the level of human development and includes level of health, education and living standard (Ref. 3).  
**Income per person (Income)**: This is calculated as gross domestic product per person adjusted for inflation and is converted to dollars (from 2017) using power parity rates (Ref. 4).  
**Life Expectancy (LifeExp)**: It is the average number of years a newborn child would live, considering the current mortality patterns (Ref. 5).  
**The Sustainable Development Index (SDI)**: This index assesses the ecological efficiency of nations in delivering human development considering “development index” and “ecological impact index” (Ref. 6).  
**GDP per capita (GDPPC)**: is calculated as GDP divided by midyear population, data is in constant of dollars (from 2010) (Ref. 7).  
**Metadata**: Income group and Region in the data were taken from the classification for The World Bank GNI (Ref. 8).  
**Note**: Rmarkdown for the report is attached at the end of the document as Appendix.  

## Data cleaning
All data imported from CSV were read into R and cleaned (i.e., values in K, M, B etc. were converted to e3, e6, e9 respectively. The data is converted to tidy format using tidyverse (Ref. 9). Since, after combining all the data it became too large (>2.5 Gb) and therefore it was filtered only for few selected years (i.e., 1990, 1995, 2000, 2005, 2015, 2019). Missing data (i.e., NA) were removed.

## Analysis done 
1. Data visualization - Histogram, Bar plot, Box plot, Plot of means, Effect plot
2. Measures of cental tendency across various parameters
3. Anova (One-way, Two-way)
4. Tukey post-hoc
5. Fisher’s Exact Test 

## Dependencies
* library(tidyverse)
* library(gt)
* library(pracma) # for mode
* library(ggpubr) # for ggarrange
* library(memisc) # mtable 
* library(multcomp) # for Tukey post-hoc test
* library(Rmisc) # for summarySE
* library(phia) # for testInteractions
* library(effects) # for effect
* library(knitr) # for kable
* library(broom) # for tidy glht
* library(jtools) # for summ

## References
1.	Gapminder: https://www.gapminder.org/data
2.	Population: http://gapm.io/dpop
3.	HDI: https://hdr.undp.org/en
4.	Income: http://gapm.io/dgdppc
5.	LifeExp: http://gapm.io/ilex
6.	SDI: http://gapm.io/dsdi
7.	GDPPC: https://data.worldbank.org/indicator/NY.GDP.PCAP.KD
8.	Metadata: https://data.worldbank.org/indicator/NY.GNP.MKTP.PP.CD
9.	Wickham H, Averick M, Bryan J, Chang W, McGowan LD, François R, Grolemund G, Hayes A, Henry L, Hester J, Kuhn M. Welcome to the Tidyverse. Journal of open source software. 2019 Nov 21;4(43):1686.
