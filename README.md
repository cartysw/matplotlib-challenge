# matplotlib-challenge

Hello!

This is a repo for the Matplotlib Challenge for the UofM Data Analytics Bootcamp course. The jupyter notebook script and data files are included for review. 

All credits for inital file formatting and initial sample code included in the file for use in the challenge go to whoever created the starter file/code through the bootcamp course.

References were used during the creation of this script, which you can find below. I hope the analysis found within proves useful!

I received help from the xpert learning assistant through the bootcamp website resources with printing: "array(['g989'], dtype=object)". There were a bunch of clarifications that had to be made but for reference my first prompt was:
im working with a dataset concerning mouse lab treatment results. i need to find info about a specific mouse id that repeats. i have: dupes = mouse_Data_Full['Mouse ID'].value_counts() print(dupes['g989']). This (correctly) prints out how many times the mouse id "g989" occurs, but the problem is that the output i'm trying to receive is: array(['g989'], dtype=object)

I referenced this site for info on how to drop rows containing specific values, specifically for the function to drop rows containing the mouse id "g989":
https://www.geeksforgeeks.org/how-to-drop-rows-in-pandas-dataframe-by-index-labels/

I referenced this for syntax on .sem() function, used for calcs in the summary statistics table:
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sem.html

I referenced code from an ai result off google to help write the "advanced summary" table that we were asked to write all on one line. Here's the query I entered on the google search that got me what i needed:
pandas generate statistics summary table using agg function

I got more help from xpert learning assistant with adding a "Tumor Volume (mm3)" header to the "advanced_Summary" stats table,
here's a snippet of the prompt i used:
i have something that gets almost what i need: advanced_Summary = mouse_Data_Clean.groupby(['Drug Regimen'])['Tumor Volume (mm3)'].agg(['mean', 'median', 'var', 'std', 'sem']) advanced_Summary. The only issue is that i would like it to also display Tumor Volume (mm3) above the "column" names in the resulting summary table

I referenced this stack overflow thread for formatting help, specifically for getting the pie charts to show a percentage inside the wedges:
https://stackoverflow.com/questions/6170246/how-do-i-use-matplotlib-autopct 

I performed a google search to figure out how to move a pie chart title to the middle of the left side on the chart using matplotlib.pyplot. The ai result told me i could pass "y=0.5" in the plt.title() function which worked for me, so here's the prompt i used:
matplotlib print pie chart title on middle left side of pie chart

I got syntax help from the xpert assistant with filtering final tumor volume results per regimen in the Quartiles, Outliers and Boxplots section.

I referenced this to create the code line that edits the outlier point colors on the box plot using the "flierprops" argument:
https://stackoverflow.com/questions/43342564/flier-colors-in-boxplot-with-matplotlib

I got more help from xpert assistant with writing the data gathering lines for the generation of the scatter plot, specifically the groupby and merging functions.

I referenced this to calculate the correlation coefficient for the final plot:
https://stackoverflow.com/questions/49350445/correlation-coefficient-of-two-columns-in-pandas-dataframe-with-corr

I referenced this to help write my lines that calculate the linear regression and then print the line onto the scatter plot:
https://geo.libretexts.org/Courses/Texas_AM/ATMO_321%3A_python_for_atmospheric_sciences/18%3A_Regression/18.02%3A_scipy.stats.linregress()
