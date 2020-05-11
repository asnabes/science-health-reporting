# Documentation for cleaning data exercise
1.	The data was split up over three pages of the PDF of a document titled ["Inventory of U.S. Greenhouse Gas Emissions and Sinks: 1990-2018."](https://www.epa.gov/sites/production/files/2020-04/documents/us-ghg-inventory-2020-main-text.pdf) Using Adobe Acrobat, I converted each page to an Excel spreadsheet. I copied and pasted the data from the second spreadsheet into the first one and the data from the third spreadsheet into the first one.
2.	I bolded the second row, because it contains the labels of each column.
3.	There were two columns that contained no data, because the table in the PDF had a grey line separating 1990 and 2005 and a grey line separating 2005 and 2014. I deleted the two empty columns.
4.	I relabeled the words in the “Gas/Source” column so that each category says the source followed by the gas emitted by that source. I did this because some of the categories apply to several gases, such as petroleum systems, and I want to make it clear which gas was emitted from that source we’re talking about. I did not put the gas name in parentheses at the end of a few of the categories, because for those categories, it’s obvious which gas is involved. An example is “N2O from Product Uses.” Some of the categories had letters at the end such as “a” or “b,” which refer to footnotes at the end of the table in the PDF. I deleted these letters. 
5.	I changed the column title “Gas/Source” to “Source and Gas” because in my table, the source is usually listed before the gas. 
6.	The table in the PDF lists “0.0” as a value or values in the “Magnesium Production and Processing” category in the HFCs section and in the “Substitution of Ozone Depleting Substances” category in the PFCs section. It’s not clear whether “0.0” refers to 0 or a value less than 0.1. I deleted these two rows, as they include ambiguous data points. The other data points in the rows are small values, so I think it’s okay to delete them.
7.	Row 46 was empty, so I deleted it. 
8.	I deleted all categories that had “+”s for all or most of their years. The “+”s are values less than 0.05 MMT CO2 Eq. Since we don’t know the values, these rows do not need to be in a data table. Also, as I have learned from my coursework for this class, if you wanted to find the average of a column, the “+” would interfere with the average function. I decided to not delete the rows with only one “+” because most of the values in the rows are real values.<br/>
These are the categories I deleted:<br/>
Abandoned Oil and Gas Wells (CO2)<br/>
Magnesium Production and Processing (CO2)<br/>
Ferroalloy Production (CH4)<br/>
Carbide Production and Consumption (CH4)<br/>
Iron and Steel Production & Metallurgical Coke Production (CH4)<br/>
Incineration of Waste (CH4)<br/>
Petroleum Systems (N2O)<br/>
Natural Gas Systems (N2O)<br/>
Electronics Industry (NF3)<br/>
Total Unspecified Mix of HFCs, PFCs, SF6 and NF3<br/>
Electronics Industry (Unspecified Mix of HFCs, PFCs, SF6 and NF3)<br/>
