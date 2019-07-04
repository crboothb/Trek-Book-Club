TrekBookClub data visualization notes

All visualizations will be conducted in RStudio.
Finished visualizations will be available in an annotated .Rmd file, and available as .png images

Changes to initial spreadsheet:
* Converted to .csv for easier processing
* Column headings changed for easier processing
	* "Month/Year" --> "year_month"
	* "Selected or Vote" --> "Selection"
	* "D or lower" --> "D"
	* "Number of votes" --> "n_votes"
* In the selection column, notes on whether there was involvement from Patreons in the selection process were removed
* A new column titled "Patreon" was added indicating whether there was involvement from Patreons in the selection process. This variable is a binary "yes" or "no"
* Dates were changed from Excel's godawful automatic date settings to month-year "XX-XX" format. Note: Never open the .csv in Excel again or this change will revert :(
* All percentages were converted to decimals
* In the Series column, the series classification for novels that were unaffiliated with a particular television series were renamed "Unaffiliated." For example, "Titan: Taking Wing," cannot be comfortably affiliated with any particular television series because it includes characters from several series. I believe this larger group better reflects the fact that the series classification for all other novels connects them to particular television properties. Affected novels:
	* "Articles of the Federation"
	* "Titan: Taking Wing"
	* "Titan: The Red King"
* "Publication" column was added to record the first publication year of each novel because why not?
* "Pages" column was added to record the number of pages in each novel's first edition because why not?

All visualizations will be conducted in RStudio.
Finished visualizations will be available in an annotated .Rmd file, and available as .png images

Interesting basic facts:
* averaged scores of novels from different series --DONE
* Top 5 Novels with the highest average score --DONE
* Histogram of novels' publication dates --DONE
* Growth in the people who vote in the poll--as a proxy for the growth in #TrekBookClub's participants --DONE

Proposed visualizations:
* time-series plot of the number of votes cast in ranking the novels over time --DONE (a point plot with a linear best fit line?) --DONE
* plot of each of each novel's popularity by number of votes corrected against the general growth in the #TrekBookClub community (eh, not so sure this is necessary)
* stacked bar graphs of the proportion of each rating for the novels. This approach sees the vote for a letter grade as likert-scale data. --DONE
* stacked bar graphs of the proportion of each rating for the novels, all faceted by series. (that ordered, color-coded dotplot works better)
* plot of average score of each novel, when each vote for an A, B, C, or D, is counted as 3,2,1, and 0 respectively. Inclusion of some indication of the number of votes cast for normalization purposes--> Do these averages capture enough information about how the community felt about each novel? Reflect on whether there is info in the stacked bar, that doesn't show up in the averages. --DONE (It'll do, but how the average was generated will have to be explained in a caption. Maybe ask Rob what he thinks about using the average)
* plot of average score of novel against publication date. Is this a productive variable? --DONE, and no, it's not
* plot of average score of novel against number of pages. Is this a productive variable? --DONE, and no, it's not
* plots of average score and number of voters faceted by whether the novel was selected or voted for --DONE, no major differences at ALL in scores. Steeper slope for selected novels may well be due to outliers (The Way to the Stars (Fricking Una McCormack! XD ) at the high end, and the very first 2 novels back when the club was just starting on the low end)

Continuing issues:
* different novels have very different numbers of voters. This means they also could also have differences in the significance of the composite scores. (Need to reopen statistics notes :/ )
* Do novels with higher numbers of voters have a higher proportion of people giving As? NO! This is good! For each letter grade, the proportion of the grade is not not correlated with the number of votes! There's a very slight negative correlation with C, but I have to figure out how to decide how real the correlation is. 
