CRAN Task View: Archaeological Science
---------------------------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><strong>Maintainer:</strong>
Ben Marwick</td>
<td align="left"><strong>Contact:</strong>
benmarwick at gmail.com</td>
<td align="left"><strong>Version:</strong>
2015-04-18</td>
</tr>
</tbody>
</table>

This CRAN Task View contains a list of packages useful for scientific work in Archaeology, grouped by topic. Note that this is not an official CRAN Task View, just one I have prepared for my own convenience, so it includes some packages only on GitHub and other non-CRAN resources I find useful. 

Besides these packages, a very wide variety of functions suitable for scientific work in Archaeology is provided by both the basic R system (and its set of recommended core packages), and a number of other packages on the Comprehensive R Archive Network (CRAN) and [GitHub](http://www.rdocumentation.org/packages?type=github). Consequently, several of the other CRAN Task Views may contain suitable packages, in particular the [Social Sciences](http://cran.rstudio.com/web/views/SocialSciences.html), [Spatial](http://cran.rstudio.com/web/views/Spatial.html),  [Spatio-temporal](http://cran.rstudio.com/web/views/SpatioTemporal.html), [Cluster analysis](http://cran.r-project.org/web/views/Cluster.html), [Multivariate Statistics](http://cran.r-project.org/web/views/Multivariate.html), [Bayesian inference](http://cran.r-project.org/web/views/Bayesian.html), [Visualization](http://cran.r-project.org/web/views/Graphics.html), and [Reproducible research](http://cran.r-project.org/web/views/ReproducibleResearch.html) Task Views. 

Contributions to this Task View are always welcome, and encouraged. The source file for this particular task view file resides in a GitHub repository (see below), and pull requests are the preferred method for contributions. 

**Data acquisition**

-  To read Microsoft Excel files into R there are a number of packages: [readxl]( https://github.com/hadley/readxl) (requires Rcpp, which in turn requires Rtools for Windows or XCode for OSX), [gdata](http://cran.rstudio.com/web/packages/gdata/index.html) (requires Perl), [openxlsx](http://cran.rstudio.com/web/packages/openxlsx/index.html) (requires Rcpp, which in turn requires Rtools for Windows or XCode for OSX), [XLConnect](http://cran.rstudio.com/web/packages/XLConnect/index.html) (requires [rJava](http://cran.rstudio.com/web/packages/rJava/index.html) and Java), [xlsx](http://cran.rstudio.com/web/packages/xlsx/index.html) (also requires rJava and Java). OpenDocument Spreadsheet files can be read into R using [readODS](http://cran.rstudio.com/web/packages/readODS/index.html). However, the preferred method is to export your spreadsheets from Excel as CSVs (comma-separated-values, a simple, non-proprietary plain-text-based format that is very transparent, being human-readable, easily machine-processable and suitable for archival storage) and read them into R using the base function `read.csv()`. Data in other types of plain text files can be read in with `read.table()`. Text data (as in sentences and paragraphs) can be read in and analysed with the [tm](http://cran.rstudio.com/web/packages/tm/index.html) package. 
-   For quickly reading in a very large number of CSV files, or very large CSV files, use `fread()` from the [data.table](http://cran.rstudio.com/web/packages/data.table/index.html) package or functions in the [readr](https://github.com/hadley/readr) package.
-	  [RODBC](http://cran.rstudio.com/web/packages/RODBC/index.html), [RMySQL](http://cran.rstudio.com/web/packages/RMySQL/index.html), [RPostgreSQL](http://cran.rstudio.com/web/packages/RPostgreSQL/index.html), [RSQLite](http://cran.rstudio.com/web/packages/RSQLite/index.html) for connecting R to SQL databases. [RODBC](http://cran.rstudio.com/web/packages/RODBC/index.html) can connect to Microsoft Access databases. 
-	  The [haven](https://github.com/hadley/haven) and [foreign](http://cran.rstudio.com/web/packages/foreign/index.html) packages can be used for reading and writing files from certain versions of Minitab, S, SAS, SPSS, Stata, Systat and Weka. 
-   ESRI shapefiles can be read using [rgdal](http://cran.rstudio.com/web/packages/rgdal/index.html) or [maptools](http://cran.rstudio.com/web/packages/maptools/index.html)
- R can receive data directly from the web using [httr](http://cran.rstudio.com/web/packages/httr/index.html), [XML](http://cran.rstudio.com/web/packages/XML/index.html), [jsonlite](http://cran.rstudio.com/web/packages/jsonlite/index.html), [rvest](http://cran.rstudio.com/web/packages/rvest/index.html), [RSelenium](http://cran.r-project.org/web/packages/RSelenium/index.html) (requires Selenium 2.0 Remote WebDriver). R can be programmed to be a web-scraper using rvest and/or rselenium. The [Web Technologies](http://cran.r-project.org/web/views/WebTechnologies.html) task view gives more details.
- Google spreadsheets can be read into R using the [googlesheet](https://github.com/jennybc/googlesheet) package
- Datasets from the Open Context repository can be browsed and read into R using the [opencontext](https://github.com/ropensci/opencontext) package

**Data manipulation**

-   [dplyr](http://cran.rstudio.com/web/packages/dplyr/index.html) and [data.table](http://cran.rstudio.com/web/packages/data.table/index.html) for splitting the data up by groups, applying some common or custom functions, and combining the output back into a convenient form (ie. typical aggregation, splitting and summarising operations). Both packages are fast on very large datasets. 
-	[reshape2](http://cran.rstudio.com/web/packages/reshape2/index.html) and [tidyr](http://cran.rstudio.com/web/packages/tidyr/index.html) for rearranging the data from long to wide forms, and more complex reshaping. 
-     [sqldf](http://cran.rstudio.com/web/packages/sqldf/index.html) can manipulate data directly in R using SQL queries

**Visualising data**

-     [ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html) produces a very wide variety of attractive plots with a highly flexible and logical syntax. 
-    Extensions include [ggbiplot](https://github.com/vqv/ggbiplot) (PCA biplots with ellipses), [GGally](http://cran.r-project.org/web/packages/GGally/index.html) (plot matrices), [ggtern](http://www.ggtern.com/) (ternary plots), [gridExtra](http://cran.rstudio.com/web/packages/gridExtra/index.html)  (arranging multiple plots, see also [wq](http://cran.rstudio.com/web/packages/wq/index.html)), and [ggfortify](https://github.com/sinhrks/ggfortify) (many methods for plotting PCA, clustering, linear model output, etc., using ggplot2) 
-   [plotrix](http://cran.rstudio.com/web/packages/plotrix/index.html) has the function `battleship.plot()` to make Ford's battleship diagrams. 
-   [ggmaps](http://cran.rstudio.com/web/packages/ggmaps/index.html) combines the spatial information of static maps from Google Maps, OpenStreetMap, Stamen Maps or CloudMade Maps with the layered grammar of graphics implementation of ggplot2
-	   Stratigraphic data plots can be drawn using `Stratiplot()` function in [analogue](http://cran.rstudio.com/web/packages/analogue/index.html) and functions `strat.plot()` and strat.plot.simple in the [rioja](http://cran.rstudio.com/web/packages/rioja/index.html) package. The rioja package also includes `chclust()` for stratigraphically constrained clustering, and related dendrogram plotting methods.
-	   [rgl](http://cran.rstudio.com/web/packages/rgl/index.html) for interactive 3D plots, [scatterplot3d](http://cran.rstudio.com/web/packages/scatterplot3d/index.html) also draws 3D point clouds.
-   [tabplot](https://github.com/mtennekes/tabplot/) for exploratory data visualisation of tables
-   For schematic diagrams such as Harris matrices, [DiagrammeR](https://github.com/rich-iannone/DiagrammeR) is useful.
-   For colour schemes in plots: [RColorBrewer](http://cran.r-project.org/web/packages/RColorBrewer/index.html), [wesanderson](http://cran.r-project.org/web/packages/wesanderson/index.html), [munsell](http://cran.r-project.org/web/packages/munsell/index.html)  for exploring and using the Munsell colour system, and for some extra themes for ggplot2, including some Tufte-inspired themes, see [ggthemes](http://cran.r-project.org/web/packages/ggthemes/index.html). 
-   [rCharts](https://github.com/ramnathv/rCharts) allows the interactive visualization of R data using javascript libraries, and [ggvis](http://cran.r-project.org/web/packages/ggvis/index.html) produces interactive web graphics using vega.

**Analysis in general**

-    Base R, especially the stats package, has a lot of functionality useful for analysing archaeological data. For example, `chisq.test()`, `prop.test()`, `binom.test()`, `t.test()`, `wilcox.test()`, `kruskal.test()`, `mcnemar.test()`, `cor.test()`, `power.t.test()`, `power.prop.test()`, `power.anova.test()` among many others. [Hmisc](http://cran.r-project.org/web/packages/Hmisc/index.html) includes bootstrapping, setting confidence intervals, and power analysis functions, see also [psych](http://cran.r-project.org/web/packages/psych/index.html) for useful descriptive statistics and visualizations.
-    Bayesian and resampling variants of these also exist, for example in the [MCMCpack](http://cran.r-project.org/web/packages/MCMCpack/index.html), [BEST](http://cran.r-project.org/web/packages/BEST/index.html) (requires JAGS), [Bayesian First Aid](https://github.com/rasmusab/bayesian_first_aid) (also requires JAGS) packages (see the [Bayesian](http://cran.r-project.org/web/views/Bayesian.html) task view for more) and the [coin](http://cran.rstudio.com/web/packages/coin/index.html), [boot](http://cran.r-project.org/web/packages/boot/index.html), and [bootstrap](http://cran.r-project.org/web/packages/bootstrap/index.html) packages (see also [msm](http://cran.r-project.org/web/packages/msm/index.html)).
-    For analysing change over time, [bcp](http://cran.r-project.org/web/packages/bcp/index.html), [changepoint](http://cran.r-project.org/web/packages/changepoint/index.html), [ecp](http://cran.r-project.org/web/packages/ecp/index.html), [AnomalyDetection](https://github.com/twitter/AnomalyDetection) and [BreakoutDetection](https://github.com/twitter/BreakoutDetection) provide functions for detecting distributional changes within time-ordered observations.
-    [abc](http://cran.r-project.org/web/packages/abc/index.html) provides functions for parameter estimation, model selection, and goodness-of-fit.

**Analysis of categorical and count data**

-	The `table()` function in the base package and the `xtabs()` and `ftable()` functions in the stats package construct contingency tables.
-	The `chisq.test()` and `fisher.test()` functions in the stats package may be used to test for independence in two-way contingency tables    

**Linear, generalized linear models, and non-linear models**

-  Linear models can be fitted (via OLS) with `lm()` (from stats).
-  The `nls()` function (from stats) as well as the package [minpack.lm](http://cran.rstudio.com/web/packages/minpack.lm/index.html) allow the solution of nonlinear least squares problems.
- Correlated and/or unequal variances can be modeled using the `gnls()` function of the [nlme](http://cran.rstudio.com/web/packages/nlme/index.html) package and by [nlreg](http://cran.rstudio.com/web/packages/nlreg/index.html). The nlme package is supported by Pinheiro & Bates (2000) Mixed-effects Models in S and S-PLUS, Springer, New York. 
-  The generic `anova()` function in the [stats](http://cran.rstudio.com/web/packages/stats/index.html) package constructs sequential analysis of variance and analysis of deviance tables, and can compute F and likelihood-ratio tests for nested models. (It is typical for other classes of statistical models in R to have anova methods as well.) The generic anova function in the [car](http://cran.rstudio.com/web/packages/car/index.html) package (associated with Fox, An R and S-PLUS Companion to Applied Regression, Sage, 2002) constructs so-called "Type-II" and "Type-III" tests for linear and generalized linear models.

**Multivariate statistics**

-   The [Cluster task view](http://cran.r-project.org/web/views/Cluster.html) provides a more detailed discussion of available cluster analysis methods and appropriate R functions and packages.
-	 [caret](http://cran.rstudio.com/web/packages/caret/index.html) and [FactoMiner](http://cran.rstudio.com/web/packages/FactoMiner/index.html) are popular packages with a suite of multivariate methods
-	[aplpack](http://cran.rstudio.com/web/packages/aplpack/index.html) provides `bagplots()`
-	`lda()` and `qda()` within [MASS](http://cran.rstudio.com/web/packages/MASS/index.html) provide linear and quadratic discrimination respectively.

Model Testing and Validation

- [caret](http://cran.rstudio.com/web/packages/caret/index.html) provides many functions for model training, testing, and validation. There is also Max Kuhn's excellent companion book called "Applied Predictive Modeling" (Springer, also available as an ebook). The [mlr](http://cran.r-project.org/web/packages/mlr/index.html) package also provides classification, regression, and machine learning methods. 
-  Other packages that enable tuning and evaluation of models include bootstrap and [Hmisc](http://cran.rstudio.com/web/packages/Hmisc/index.html)
- The [CVtools](http://cran.rstudio.com/web/packages/CVtools/index.html) and [DAAG](http://cran.rstudio.com/web/packages/DAAD/index.html) packages include cross-validation functions for evaluating the optimality of tuning parameters such as sample sizes or number of predictors etc., in statistical models 

Hierarchical cluster analysis

-    The package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) provides functions for cluster analysis following the methods described in Kaufman and Rousseeuw (1990) Finding Groups in data: an introduction to cluster analysis, Wiley, New York
-    There are also `hclust()` in the stats package and `hcluster()` in [amap](http://cran.rstudio.com/web/packages/amap/index.html)
-    [pvclust](http://cran.rstudio.com/web/packages/pvclust/index.html) is a package for assessing the uncertainty in hierarchical cluster analysis. It provides approximately unbiased p-values as well as bootstrap p-values.

Other partitioning methods

-   `kmeans()` in stats provides k-means clustering and cmeans() in [e1071](http://cran.rstudio.com/web/packages/e1071/index.html) implements a fuzzy version of the k-means algorithm. The recommended package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) also provides functions for various partitioning methodologies.
-    To compute the optimum number of clusters there is the `pamk()` function in the [fpc](http://cran.rstudio.com/web/packages/fpc/index.html) package, `cascadeKM()` in [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), `Mclust()` in [mclust](http://cran.rstudio.com/web/packages/mclust/index.html), `apcluster()` in [apcluster](http://cran.rstudio.com/web/packages/apcluster/index.html)

Mixture models and model-based cluster analysis

-    [mclust](http://cran.rstudio.com/web/packages/mclust/index.html) and [flexmix](http://cran.rstudio.com/web/packages/flexmix/index.html) provide implementations of model-based cluster analysis.

Principle components and other projection, scaling, and ordination methods

-	 Principal Components (PCA) is available via the `prcomp()` function (based on svd),  `rda()` (in package [vegan](http://cran.rstudio.com/web/packages/vegan/index.html)), `pca()` (in package [labdsv](http://cran.rstudio.com/web/packages/labdsc/index.html)) and `dudi.pca()` (in package [ade4](http://cran.rstudio.com/web/packages/ade4/index.html)), provide more ecologically-orientated implementations. Plotting of PCA output is available in [ggbiplot](https://github.com/vqv/ggbiplot) and [ggfortify](https://github.com/sinhrks/ggfortify). 
-   Redundancy Analysis (RDA) is available via `rda()` in vegan and `pcaiv()` in ade4. 
-   Canonical Correspondence Analysis (CCA) is implemented in `cca()` in both vegan and ade4. 
-   Detrended Correspondence Analysis (DCA) is implemented in `decorana()` in vegan. 
-   Principal coordinates analysis (PCO) is implemented in `dudi.pco()` in ade4, `pco()` in labdsv, `pco()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html), and `cmdscale()` in package [MASS](http://cran.rstudio.com/web/packages/MASS/index.html).
-    Non-Metric multi-Dimensional Scaling (NMDS) is provided by `isoMDS()` in package MASS and `nmds()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html). `nmds()`, a wrapper function for `isoMDS()`, is also provided by package [labdsv](http://cran.rstudio.com/web/packages/labdsv/index.html). vegan provides helper function `metaMDS()` for `isoMDS()`, implementing random starts of the algorithm and standardised scaling of the NMDS results. The approach adopted by vegan with `metaMDS()` is the recommended approach for ecological data.
-	`corresp()` and `mca()` in MASS provide simple and multiple correspondence analysis respectively. [ca](http://cran.rstudio.com/web/packages/ca/index.html) also provides single, multiple and joint correspondence analysis. `ca()` and `mca()` in ade4 provide correspondence and multiple correspondence analysis respectively, as well as adding homogeneous table analysis with `hta()`. Further functionality is also available within vegan co-correspondence is available from cocorresp. [FactoMineR](http://cran.rstudio.com/web/packages/FactoMineR/index.html) provides `CA()` and `MCA()` which also enable simple and multiple correspondence analysis as well as associated graphical routines. [CAinterprTools](https://github.com/gianmarcoalberti/CAinterprTools) has functions for correspondence analysis and diagnostics. 
-    Seriation methods are available in [seriation](http://cran.rstudio.com/web/packages/seriation/index.html), which includes `bertinplot()` for producing battleship plots, and [CAseriation](https://github.com/gianmarcoalberti/CAseriation) which also has a battleship plotting function. 

Dissimilarity coefficients

- `dist()` in standard package stats, `daisy()` in recommended package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html), `vegdist()` in [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), `dsvdis()` in [labdsv](http://cran.rstudio.com/web/packages/labdsv/index.html), `Dist()` in [amap](http://cran.rstudio.com/web/packages/amap/index.html), `distance()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html), a suite of functions in [ade4](http://cran.rstudio.com/web/packages/ade4/index.html)
- [simba](http://cran.rstudio.com/web/packages/simba/index.html) provides functions for the calculation of similarity and multiple plot similarity measures with binary data (for instance presence/absence data)
- `distance()` in the [analogue](http://cran.rstudio.com/web/packages/analogue/index.html) package can be used to calculate dissimilarity between samples of one matrix and those of a second matrix. The same function can be used to produce pair-wise dissimilarity matrices, though the other functions listed above are faster. `distance()` can also be used to generate matrices based on Gower's coefficient for mixed data (mixtures of binary, ordinal/nominal and continuous variables). Function `daisy()` in package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) provides a faster implementation of Gower's coefficient for mixed-mode data than `distance()` if a standard dissimilarity matrix is required. Function `gowdis()` in package [FD](http://cran.rstudio.com/web/packages/FD/index.html) also computes Gower's coefficient and implements extensions to ordinal variables.
- [DistatisR](http://cran.rstudio.com/web/packages/DistatisR/index.html) provides functions for three-way multidimensional scaling for the analysis of multiple distance/covariance matrices collected on the same set of observations.
- Simple and partial Mantel tests to compute the Mantel statistic as a matrix correlation between two dissimilarity matrices are available in [vegan](http://cran.rstudio.com/web/packages/vegan/index.html) and [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html)

**Making maps and using R as a Geographical Information System**

-	Making maps: [maps](http://cran.rstudio.com/web/packages/maps/index.html), [mapdata](http://cran.rstudio.com/web/packages/mapdata/index.html), [maptools](http://cran.rstudio.com/web/packages/maptools/index.html), [mapproj](http://cran.rstudio.com/web/packages/mapproj/index.html), [ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html), [ggmap](http://cran.rstudio.com/web/packages/ggmap/index.html), [RgoogleMaps](http://cran.rstudio.com/web/packages/RgoogleMaps/index.html), [RColorBrewer](http://cran.rstudio.com/web/packages/RColorBrewer/index.html) 
-   R has many packages that enable it to be used as a GIS for spatial analysis: [sp](http://cran.rstudio.com/web/packages/sp/index.html), [raster](http://cran.rstudio.com/web/packages/raster/index.html), [rasterVis](http://cran.rstudio.com/web/packages/rasterVis/index.html), [shapefiles](http://cran.rstudio.com/web/packages/shapefiles/index.html), [spatial](http://cran.rstudio.com/web/packages/spatial/index.html), [spatstat](http://cran.rstudio.com/web/packages/spatstat/index.html), [splancs](http://cran.rstudio.com/web/packages/splancs/index.html), [ipdw](http://cran.rstudio.com/web/packages/ipdw/index.html), [geoR](http://cran.rstudio.com/web/packages/geoR/index.html), [argosfilter](http://cran.rstudio.com/web/packages/argosfilter/index.html), [ads](http://cran.rstudio.com/web/packages/ads/index.html), [spdep](http://cran.rstudio.com/web/packages/spdep/index.html), [gstat](http://cran.rstudio.com/web/packages/gstat/index.html), as well as [spgrass6](http://cran.rstudio.com/web/packages/spgrass6/index.html) and [rgrass7](http://cran.rstudio.com/web/packages/rgrass7/index.html) which provides facilities for using all [GRASS](http://grass.osgeo.org/) geographical information system commands from the R command line.
-   [rgdal](http://cran.rstudio.com/web/packages/rgdal/index.html) uses the GDAL (Geospatial Data Abstraction Library) (raster) and OGR (vector) data I/O library, as well as PROJ.4 for CRS (coordinate reference systems) (re)projections
-   [rgeos](http://cran.rstudio.com/web/packages/rgeos/index.html) uses the GEOS (Geometry Open Source) library, which powers PostGIS: does the 'usual' geometry operations for features
-   The [Spatial](http://cran.r-project.org/web/views/Spatial.html) and [Spatio Temporal](http://cran.r-project.org/web/views/SpatioTemporal.html) task views have more details. 

**Environmental & geological analysis**

-	   Transfer function models including weighted averaging (WA), modern analogue technique (MAT), Locally-weighted WA, & maximum likelihood (aka Gaussian logistic) regression (GLR) are provided by [analogue](http://cran.rstudio.com/web/packages/analogue/index.html), [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), and [rioja](http://cran.rstudio.com/web/packages/rioja/index.html) for stratigraphic analyses
-	  [G2Sd](http://cran.rstudio.com/web/packages/G2Sd/index.html) gives full descriptive statistics and a physical description of sediments based on grain-size distributions, [soiltexture](http://cran.rstudio.com/web/packages/soiltexture/index.html) and [ggtern](http://cran.rstudio.com/web/packages/ggtern/index.html) for ternary plots of soil texture
-	   Constrained clustering of stratigraphic data is provided by function `chclust()` in the form of constrained hierarchical clustering in [rioja](http://cran.rstudio.com/web/packages/rioja/index.html).
-	   Stratigraphic columns can be plotted and analysed with the the [SDAR](http://run.unl.pt/bitstream/10362/14554/1/TGEO0128.pdf) package. 
-    Radiocarbon dates can be calibrated using [Bchron](http://cran.rstudio.com/web/packages/Bchron/index.html) with various calibration curves (including user generated ones); also does Age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models; and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM).
-    Various R functions for Luminescence Dating data analysis are in the [Luminescence](http://cran.rstudio.com/web/packages/Luminescence/index.html) package.
-    Functions for tree ring analysis can be found in [dplR](http://cran.rstudio.com/web/packages/dplR/index.html)
-    The [siar](http://cran.rstudio.com/web/packages/siar/index.html) package takes data on organism isotopes and fits a Bayesian model to their dietary habits based upon a Gaussian likelihood with a mixture dirichlet-distributed prior on the mean
-    The [zooaRch](http://cran.r-project.org/web/packages/zooaRch/) package has functions for survival analysis of zooarchaeological datasets
- See the [Environmetrics](http://cran.r-project.org/web/views/Environmetrics.html) task view for more. 

**Phylogenetics, morphometrics, evolution and shape analysis**

-  The [Phylogenetics task view](http://cran.r-project.org/web/views/Phylogenetics.html) provides more detailed coverage of the subject area and related functions within R. 
-  Packages specifically tailored for the analysis of phylogenetic and evolutionary data include: [ape](http://cran.rstudio.com/web/packages/ape/index.html), [phytools](http://cran.rstudio.com/web/packages/phytools/index.html), [phangorn](http://cran.rstudio.com/web/packages/phangorn/index.html), [Rphylip](http://cran.rstudio.com/web/packages/Rphylip/index.html) (requires PHYLIP), [ouch](http://cran.rstudio.com/web/packages/ouch/index.html), and [pegas](http://cran.rstudio.com/web/packages/pegas/index.html). 
-  For plotting trees most of these packages include their own modifications of the base `plot()` function, and there are also [ggtree](http://cran.rstudio.com/web/packages/ggtree/index.html), [ggdendro](http://cran.rstudio.com/web/packages/ggdendro/index.html), [dendextend](http://cran.rstudio.com/web/packages/dendextend/index.html), and [ggphylo](http://cran.rstudio.com/web/packages/ggphylo/index.html)
-  Morphometric and shape analysis methods are provided by [shapes](http://cran.rstudio.com/web/packages/shapes/index.html) and [Momocs](http://cran.rstudio.com/web/packages/Momocs/index.html). Related packages include [shapeR](https://github.com/lisalibungan/shapeR) [Anthropometry](http://cran.rstudio.com/web/packages/Anthropometry/index.html) and [Morpho](http://cran.rstudio.com/web/packages/Morpho/index.html).

**Image analysis**

-   [pixmap](http://cran.rstudio.com/web/packages/pixmap/index.html) provides methods for creating, plotting and converting bitmapped images in three different formats: RGB, grey and indexed pixmaps. Similarly, [jpeg](http://cran.rstudio.com/web/packages/jpeg/index.html) provides an easy and simple way to read, write and display bitmap images stored in the JPEG format.
-   [EBImage](http://www.bioconductor.org/packages/release/bioc/html/EBImage.html) (requires ImageMagick) provides general purpose functionality for the reading, writing, processing and analysis of images (and is very well documented). Various functions for image processing and analysis can also be found in [ripa](http://cran.rstudio.com/web/packages/ripa/index.html)

**Simulations**

- [RNetLogo](http://cran.rstudio.com/web/packages/RNetLogo/index.html) links R and NetLogo
-  [simecol](http://cran.rstudio.com/web/packages/simecol/index.html)  for simulating ecological (and other) dynamic systems. It can be used for differential equations, individual-based (or agent-based) and other models as well.
-  One-dimensional cellular automata are also possible to model with the package [CellularAutomaton](http://cran.rstudio.com/web/packages/CellularAutomaton/index.html).

**Network analysis**

-    The two major packages are [igraph](http://cran.rstudio.com/web/packages/igraph/index.html), which is a generic network analysis and visualisation package, and [sna](http://cran.rstudio.com/web/packages/sna/index.html), which performs social analysis of networks.
-    Other packages include [statnet](http://cran.rstudio.com/web/packages/statnet/index.html), [intergraph](http://cran.rstudio.com/web/packages/intergraph/index.html), [network](http://cran.rstudio.com/web/packages/network/index.html) (manipulates and displays network objects), [ergm](http://cran.rstudio.com/web/packages/ergm/index.html) (a set of tools to analyze and simulate networks based on exponential random graph models exponential random graph models), [hergm](http://cran.rstudio.com/web/packages/hergm/index.html) (implements hierarchical exponential random graph models), and [RSiena](http://cran.rstudio.com/web/packages/RSiena/index.html) (allows the analyses of the evolution of social networks using dynamic actor-oriented models)


**Reproducible research**

-	  [knitr](http://cran.rstudio.com/web/packages/knitr/index.html) enables R code and text with formatting instructions (eg. markdown or LaTeX) to be combined in a single document and executed to produce a document that contains rendered plots, analysed data and formatted text. The [remake](https://github.com/richfitz/remake) package has functions that enable declarative workflows so that each time an analysis is run, it updates only the parts of the workflow that have changed. [rlp](https://github.com/yihui/rlp) is a package that lets you write an analysis as a Rmd file and then converts it into a package. [manuscriptPackage](https://github.com/jhollist/manuscriptPackage), [template](https://github.com/cboettig/template), and [template](https://github.com/Pakillo/template) (yes, that's two slightly different packages with the same name) are packages that give templates for organising an analysis as an R package (eg. where the manuscript is the package vignette, or similarly bundled with the package) 
-   The [rmarkdown](http://cran.rstudio.com/web/packages/rmarkdown/index.html) package implements the simple markdown document formatting language with some minor customizations to recognize R code blocks and inline code. Complementary packages include [captioner](https://github.com/adletaw/captioner) and [kfigr](https://github.com/mkoohafkan/kfigr) for figure and table captions and cross-referencing. 
-   [pandoc](http://johnmacfarlane.net/pandoc/) is a universal document format converter (not an R package), in this context it is used to convert rmarkdown or LaTeX to PDF, MS Word or HTML files. It is included with RStudio but can also be used stand-alone from the command line. 
-   [packrat](http://cran.rstudio.com/web/packages/packrat/index.html) supports the development of isolated, stand-alone projects that include all the packages used and their dependencies. [miniCRAN](http://cran.rstudio.com/web/packages/miniCRAN/index.html) has functions to create a local repository to install packages (and their dependancies) from without internet access (related: [rbundler](http://cran.rstudio.com/web/packages/rbundler/index.html) for package development which manages dependencies listed in a package's DESCRIPTION file by storing them in a local project-specific library for installation). 
-   [checkpoint](http://cran.rstudio.com/web/packages/checkpoint/index.html) allows you to install R packages from a specific snapshot date in the past, ensuring that you use the same package version that you started with, not a more recent one (related: [gRAN](https://github.com/rgmbecker/gRAN) can retrieve and build sources for any version of any non-base package that has ever been released on CRAN or BioConductor).
-   [rocker](https://github.com/rocker-org/rocker) is a project that provides Docker containers to run R in a lightweight virtual environment, the hadleyverse container includes dplyr, ggplot2, etc., as well as RStudio server and LaTeX. The package [harbor](https://github.com/wch/harbor) provides functions for controlling docker containers on local and remote hosts. The [analogsea](https://github.com/sckott/analogsea) package has functions for deploying R and RStudio quickly & easily on DigitalOcean clusters using Docker images for cloud computing. The [dockertest](https://github.com/richfitz/dockertest) package contains functions for generating Dockerfiles from R packages and other R projects, and building Docker containers that contains all the package dependencies.

**Developing R code and packages**

-	  [devtools](http://cran.rstudio.com/web/packages/devtools/index.html) (requires Rtools for Windows or Xcode for OSX) for easily creating R packages. Includes `use_travis()` and related functions for easily adding continuous integration for automated building and testing during package development. 
-   [roxygen2](http://cran.rstudio.com/web/packages/roxygen2/index.html) for simplifying the creation of documentation for packages,
-   [testthat](http://cran.rstudio.com/web/packages/testthat/index.html) for developing tests of functions in packages
-   [Rcpp](http://cran.rstudio.com/web/packages/Rcpp/index.html) enables the use of C++ code in R packages for high performance computing, requires Rtools for Windows or Xcode for OSX
-   [RStudio](http://www.rstudio.com/) is an integrated development environment that simplfies developing R code with numerous built-in conveniences, including vim keyboard shortcuts.  
-   [Emacs](http://www.gnu.org/software/emacs/) is a highly flexible text editor, which when used with the [Emacs Speaks Statistics](http://ess.r-project.org/) package, is a comprehensive R development environment. [Org-mode](http://orgmode.org/) provides a literate programming environment in Emacs similar to knitr. 
-   [Style guide for writing R code](http://adv-r.had.co.nz/Style.html) by Hadley Wickham, and the package [formatR](http://cran.rstudio.com/web/packages/formatR/index.html) which is designed to reformat R code to improve readability. The [lintr](http://cran.r-project.org/web/packages/lintr/) package analyses code to check that it conforms to Hadley Wickham's style guide. 
-   Idioms of R are discussed in the [vignette](http://cran.r-project.org/web/packages/rockchalk/vignettes/Rchaeology.pdf) of the [rockchalk](http://cran.rstudio.com/web/packages/rockchalk/index.html) package and Pat Burn's essay [the R Inferno](http://www.burns-stat.com/documents/books/the-r-inferno/).

**Datasets**

-   [archdata](http://cran.rstudio.com/web/packages/archdata/index.html) contains eleven archaeological datasets from around the world reported in published studies. These represent typical forms of archaeological data (and so are useful for teaching)
-  [chemometrics](http://cran.rstudio.com/web/packages/chemometrics/index.html) contains a dataset of elemental concentrations for 180 archaeological glass vessels excavated from 15th - 17th century contexts in Antwerp.
-  [BSDA](http://cran.rstudio.com/web/packages/BSDA/index.html) contains a dataset of 60 radiocarbon ages of observations taken from an archaeological site with four phases of occupation.
-  [zooaRch](http://cran.r-project.org/web/packages/zooaRch/) contains two zooarchaeological datasets.
-  [cawd](https://github.com/sfsheath/cawd) contains 15 datasets of ancient Greek, Roman and Persian maps and digital atlas data 

**Places to go for help**

-	`?` function, eg. `?mean` to get built-in help on the mean function
-	`sos::findFn("rose diagram")` searches all installed packages for the search term, using the [sos](http://cran.rstudio.com/web/packages/sos/index.html) package
-   Most major packages come with vignettes that narrate typical uses of the package's core functions. Vignettes can be accessed with the command `vignette(packagename)`.
-	Google searches in the form: [r help [search terms]](https://www.google.com/?gws_rd=ssl#q=r+help+)
-   A custom search engine of R resources: http://www.rseek.org/
-   [Graphical output from the examples in the documentation for all CRAN packages](http://rgm3.lab.nig.ac.jp/RGM)
-   All R package documentation (including CRAN, GitHub and Bioconductor packages) is online in an easy-to-ready format at http://www.rdocumentation.org/
-   Cheatsheets to print for handy reference: [short one on base](http://cran.r-project.org/doc/contrib/Short-refcard.pdf), [longer one on base](http://cran.r-project.org/doc/contrib/Baggott-refcard-v2.pdf), [ggplot2, dplyr, tidyr, rmarkdown, making packages](http://www.rstudio.com/resources/cheatsheets/), [data.table](https://s3.amazonaws.com/assets.datacamp.com/img/blog/data+table+cheat+sheet.pdf), [using colours](https://www.nceas.ucsb.edu/~frazier/RSpatialGuides/colorPaletteCheatsheet.pdf), [colours](http://research.stowers-institute.org/efg/R/Color/Chart/ColorChart.pdf), [numerous others](http://devcheatsheet.com/tag/r/)
-  [stackoverflow](http://stackoverflow.com/questions/tagged/r) is an online Q&A point-scoring website where questions and answers can be voted on to indicate their quality. Many highly skilled R programmers are active participants. [Cross Validated](http://stats.stackexchange.com/) is a similar Q&A site for questions about statistics
-   You could send a message to the official [r-help email list](https://stat.ethz.ch/mailman/listinfo/r-help), but do be sure to read, follow and cite the [posting guide](http://www.r-project.org/posting-guide.html). The list is also [searchable](https://www.google.com/?gws_rd=ssl#q=site:stat.ethz.ch+pipermail+archaeology).


### Related links:

-   CRAN Task View: [SocialSciences](http://cran.rstudio.com/web/views/SocialSciences.html)
-   CRAN Task View: [Spatial](http://cran.rstudio.com/web/views/Spatial.html)
-   CRAN Task View: [Spatio-temporal](http://cran.rstudio.com/web/views/spatioTemporal.html)
-   CRAN Task View: [Cluster analysis](http://cran.r-project.org/web/views/Cluster.html)
-   CRAN Task View: [Multivariate Statistics](http://cran.r-project.org/web/views/Multivariate.html) 
-   CRAN Task View: [Bayesian inference](http://cran.r-project.org/web/views/Bayesian.html)
-   CRAN Task View: [Phylogenetics](http://cran.r-project.org/web/views/Phylogenetics.html)
-   CRAN Task View: [Robust](http://cran.r-project.org/web/views/Robust.html)
-   CRAN Task View: [Visualization](http://cran.r-project.org/web/views/Graphics.html)
-   CRAN Task View: [Reproducible research](http://cran.r-project.org/web/views/ReproducibleResearch.html) 
-   [David L. Carlson's guides on using R for 'Quantifying Archaeology' by Stephen Shennan 'Statistics for Archaeologists' by Robert Drennan]( http://people.tamu.edu/~dcarlson/quant/index.html)
-   [Matt Peeples' scripts for archaeological statistics]( http://www.mattpeeples.net/resources.html)
-   [Gianmarco Alberti's pages on Correspondence Analysis in Archaeology](http://cainarchaeology.weebly.com/)
-   [Quantitative Archaeology Wiki](http://wiki.iosa.it/doku.php), including [some code for battleship plots](http://wiki.iosa.it/dokuwiki/doku.php?id=contingency_tables)
-   [GitHub repository for this Task View](https://github.com/benmarwick/ctv-archaeology)

#### Publications that include R code

Contreras, Daniel A. and John Meadows. (2014) “Summed radiocarbon calibrations as a population proxy: a critical evaluation using a realistic simulation approach.” Journal of Archaeological Science 52:591-608. [doi:10.1016/j.jas.2014.05.030] (http://www.sciencedirect.com/science/article/pii/S0305440314002088)

Crema, E.R., K. Edinborough, T. Kerig, S.J. Shennan (2014) An Approximate Bayesian Computation approach for inferring patterns of cultural evolutionary change, Journal of Archaeological Science, Volume 50 Pages 160-170 [http://dx.doi.org/10.1016/j.jas.2014.07.014](http://www.sciencedirect.com/science/article/pii/S0305440314002593)

Drake BL, Wills WH, Hamilton MI, Dorshow W (2014) Strontium Isotopes and the Reconstruction of the Chaco Regional System: Evaluating Uncertainty with Bayesian Mixing Models. PLoS ONE 9(5): e95580. [doi:10.1371/journal.pone.0095580](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0095580)

Drake, Brandon L., David T. Hanson, James L. Boone (2012) The use of radiocarbon-derived Δ13C as a paleoclimate indicator: applications in the Lower Alentejo of Portugal, Journal of Archaeological Science, Volume 39, Issue 9, September 2012, Pages 2888-2896, [http://dx.doi.org/10.1016/j.jas.2012.04.027](http://www.sciencedirect.com/science/article/pii/S0305440312001471)

Drake, Brandon L., (2012) The influence of climatic change on the Late Bronze Age Collapse and the Greek Dark Ages, Journal of Archaeological Science, Volume 39, Issue 6, June 2012, Pages 1862-1870 [http://dx.doi.org/10.1016/j.jas.2012.01.029](http://www.sciencedirect.com/science/article/pii/S0305440312000416)

Drake, Brandon L., WH Wills, and Erik B Erhardt (2012) The 5.1 ka aridization event, expansion of piñon-juniper woodlands, and the introduction of maize (Zea mays) in the American Southwest The Holocene December 2012 22: 1353-1360, first published on July 9, 2012 [doi:10.1177/0959683612449758](http://hol.sagepub.com/content/22/12/1353.short)

Dye, Thomas S. (2011). “A Model-based Age Estimate for Polynesian Colonization of Hawai‘i”. Archaeology in Oceania 46, pp. 130–138 [https://github.com/tsdye/hawaii-colonization](https://github.com/tsdye/hawaii-colonization)

Lowe, K., Wallis, L., Pardoe, C., Marwick, B., Clarkson, C., Manne, T., Smith, M. and R. Fullagar 2014 Ground-penetrating radar and burial practices in western Arnhem Land, Australia. Archaeology in Oceania  49(3): 148–157 [http://onlinelibrary.wiley.com/doi/10.1002/arco.5039/abstract](http://onlinelibrary.wiley.com/doi/10.1002/arco.5039/abstract)

Mackay A, Sumner A, Jacobs Z, Marwick B, Bluff K and Shaw M 2014. Putslaagte 1 (PL1), the Doring River, and the later Middle Stone Age in southern Africa's Winter Rainfall Zone. Quaternary International. [http://dx.doi.org/10.1016/j.quaint.2014.05.007](http://dx.doi.org/10.1016/j.quaint.2014.05.007)

Marwick, B., 2013. Multiple Optima in Hoabinhian flaked stone artefact palaeoeconomics and palaeoecology at two archaeological sites in Northwest Thailand. Journal of Anthropological Archaeology 32, 553-564.  [http://dx.doi.org/10.1016/j.jaa.2013.08.004](http://dx.doi.org/10.1016/j.jaa.2013.08.004)

Marwick, B. 2013. Discovery of Emergent Issues and Controversies in Anthropology Using Text Mining, Topic Modeling, and Social Network Analysis of Microblog Content. In Yanchang Zhao, Yonghua Cen (eds) Data Mining Applications with R. Elsevier. p. 63-93 [https://github.com/benmarwick/AAA2011-Tweets](https://github.com/benmarwick/AAA2011-Tweets)

Shennan, SJ, Enrico R. Crema, Tim Kerig, (2014) Isolation-by-distance, homophily, and 'core' vs. 'package' cultural evolution models in Neolithic Europe, Evolution and Human Behavior, Available online 2 October 2014,  [http://dx.doi.org/10.1016/j.evolhumbehav.2014.09.006](http://www.sciencedirect.com/science/article/pii/S1090513814001251)

#### Contributors

Ben Marwick, Agustin Diez Castillo, Allar Haav, Sebastian Heath, Phil Riris, Tom Brughmans, Lee Drake, Stefano Costa, Enrico Crema, Domenico Giusti, Matt Peeples, Mark Madsen, Daniel Contreras
