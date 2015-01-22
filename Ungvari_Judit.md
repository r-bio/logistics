The goals of my project is to summarize 22 months of bird capture data spread over 4 years of fieldwork. I have data from 40 sampling sites of individual birds that were captured, marked, measured and released. I am interested in comparing capture rates, species accumulation curves in habitat types (2 types of habitats were sampled), species turnover between habitat types, area effects, edge effects, and basic community ecology metrics (detrended correspondence analysis, non-metric multidimensional scaling). 

The data is organized in a .csv file with individuals in rows. Sampling site information and geographic locality information is also recorded for each capture in addition to lots of other morphological and demographic variables. I want to test whether there is any nestedness or turnover between habitat types, and how area (size of a patch) affects the number of species captured. I predict that smaller patches will not have habitat specialist species.

The data needs to be standardized to capture effort (500 net hours line), there were some sites that were sampled repeatedly, while some sites were only sampled once. Otherwise it should be ready for analysis.

The R packages that I plan on using are: reshape, vegan, gdata, car, betapart, maps, mapdataknitr.
