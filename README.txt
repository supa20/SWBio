SWBio: Determining if MLST data can be used for source attribution of Campylobacter jejuni isolates
Introduction
##Where to start 1)This code require Python3 and JupyterNotebook that can be accessed via the Anaconda Navigation Package 2) Download all the files within this GitHub repository into a single file directory which include the JupyterNotebook entitled 'SourceAttribbution.ipynb' and the csv entitled 'Australia_Campy_Data.csv' 3) In the JupyterNotebook install the libraries listed at the top of the page and read the csv file

##Data Filtering

The data frame was run so the data could be quickly inspected
Any blanks in the data frame were replaced with ‘NaN’
The columns disease was commonly blank so was removed. The ‘id’ column and ‘epidemiology’ column did not contain information that was necessary for this investigation so were removed as well.
The data points in the housekeeping genes columns were numbers but this is for cataloguing purposes as opposed to holding any numerical value so were converted to strings.
##Data Visualisation

A strip plot was used to visualise any possible correlation between the source of the isolates and the clonal_complex_MLST (MLST classification).
##Correlation

To test the correlation directly between the source of the isolate and the MLST classification a contingency program was utilised. A contingency table was generated, and chi squared, statistical value and degree of freedom were calculated

To avoid error from missing values in the contingency table this points were removed from the table. This step is not necessery if there is data in each cell of the contingency table

A more efficent method to test Chi Square on every combination of variables was then run. Within this code there is an option to omit results based on their expected frequency. It is currently set at 1 (4%) but this value you can be altered to control what combinations of variables are used based on the frequency of their data points

4.A heatmap was produced from the data generated from the Chi square test to visualise any possible trends.The code for this heat map as left in as on a different data set this may be a useful visualisation step.