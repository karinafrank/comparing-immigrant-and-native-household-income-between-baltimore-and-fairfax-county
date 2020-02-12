How Do Immigrant Status and Location Affect Household Income?
======
## An analysis of the correlations between immigrant status, census tract, and household income.

This analysis was conducted by using open data from the [Opportunity Atlas](https://www.opportunityatlas.org/). The data used consisted of [immigrant household income](https://github.com/karinafrank/comparing-immigrant-and-native-household-income-between-baltimore-and-fairfax-county/blob/master/Household_Immigrant.xlsx) across all subgroups and [native household income]() across all subgroups. Similar data was also included for [immigrant]() and [native] individual income() for deeper inspection, but was not used in this analysis.

### Data Analysis

Four different data sets downloaded from the Opportunity Atlas were consolidated into a single Excel file and analyzed using the following steps.
1. Data from the original Immigrant Individual Income data sheet was copied into a [new Excel file] (https://github.com/karinafrank/comparing-immigrant-and-native-household-income-between-baltimore-and-fairfax-county/blob/master/Data%20Analysis.xlsx) to prevent alterations to the original sheet. 
2. The data was filtered via census tract name to only include the rows with data from Baltimore City and Fairfax County.
3. As data was not analyzed across gender, all data columns containing "_gM_" or "_gF_" were deleted, leaving only columns with "_gP_" indicating data for all genders. 
   * The remaining data within the Immigrant Individual Income sheet varied across race, denoted "_rX_", and income percentile, denoted "_pX_". 
4. Three columns were added between all the remaining columns to create space for imported data from the three remaining data sheets.
5. VLOOKUP was used to import appropriate data from the remaining data sheets (Immigrant Household Income, Native Individual Income, and Native Household Income) correlating to different races and income percentiles. 
   * Immigrant Household Income was not available in any sections containing "_rNA_*, as those denoted data for Native Americans.
6. Rows were created using IF statements separating data into the four categories that were analyzed: Baltimore City (Immigrant), Baltimore City (Native), Fairfax County (Immigrant), and Fairfax County (Native).
   * For example:
```
=IF(ISNUMBER(SEARCH("imm",C1)),C132,0)
```
7. A pivot table was created using census tract and immigrant status as the x-axis, or "categories", and income values for different percentiles as the y-axis, or "values."
   * A stacked bar chart was created from the pivot table to show the relative distribution and location of various income percentiles across the four categories. 
8. A pivot table was created with groupings of income by race broken down by census tract and immigrant status.
   * A clustered column chart was created from the pivot table to show trends in income by race in each of locations/ situations as well as trends in income for these different races across these situations.
9. Chart and axis titles were added to the charts to make them more readable by an audience. 

### Results

#### Income Breakdown across Census Tract and Immigrant Status 

![Image description](https://github.com/karinafrank/comparing-immigrant-and-native-household-income-between-baltimore-and-fairfax-county/blob/master/Graph%201.JPG)

The chart shows that in both locations, Baltimore City and Fairfax County, immigrants are more likely to have higher incomes than people native to the United States. Addtionally, people who live in Fairfax County are more likely to have higher incomes than their counterparts in Baltimore City. A possible explanation for this correlation is that Fairfax County is a suburb of Washington, D.c., and that many people who live there have government jobs. 

#### Average Income for Different Races across Census Tract and Immigrant Status

![Image description](https://github.com/karinafrank/comparing-immigrant-and-native-household-income-between-baltimore-and-fairfax-county/blob/master/Graph%202.JPG)

The chart shows that across location and immigrant status, except for immigrants in Fairfax County, Whites have a higher average household income, followed by Asians, Hispanics, and Blacks. Native Americans were found to have income rates similar to Blacks. This chart also shows that within race, average income tended to be higher in Faifax County than in Baltimore City, and that in most cases immigrants had higher household incomes than natives. 


### Conclusions

In both sets of analysis, people in Fairfax County tended to have higher household incomes than those in Baltimore City. Additionally, in each of these locations, people in immigrant families tended to have higher household incomes than people in families native to the United States. However, as this data was collected for households and not individuals, conclusions may not be made regarding social mobility opportunities in circumstances. Higher household incomes could be attributed to having more individuals contributing to the overall income. Additionally, the data collected may not accurately reflect the populations, as immigrants may be less willing to self-identify and to provide income information.

While the results from this analysis are not conclusive, they may inform what types of social mobility programs and interventions would or would not be helpful in these areas. There could be an instinct to enact programs that aid immigrants in an area, but the data shows that natives are more likley to have lower household incomes, and therefore may require more focus from aid programs. 

