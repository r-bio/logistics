I have developed a series of scripts that takes museum data and builds niche models. 
The trick is that we use the collection dates in order to extract the climate data at the time of collection (year in our case). This seems to improve the results of the MaxEnt niche models. My goal is to take those scripts and wrap them in an R package. 
My first goal is to understand and decide what exactly is appropriate for a package. How many steps should I include ? How to divide them up ? 
The second step might be the lengthy one: gatherin all scripts, cleaning them up and making sure there are no bugs. Some scripts are written in R, some in Perl, and some steps were just done in house, on Excel or Text Wrangler. 
The last goal is to make the actual package. 


