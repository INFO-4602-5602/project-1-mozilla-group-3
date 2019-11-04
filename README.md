# Group 3 README.md file
Trevor Buck, Clark Mousaw, Hannah Weber

## Team Roles:
The three of us in the group each created a visualization for the project. We did three visualizations so we each would have something to work on and so the work would be easily divided. We met twice outside of class to work on this project. 

## How to Run the Project:
We have three different HTML files to run the three visualizations. We will provide individual descriptions of our visualizations as well as information for how to run each file below.
    * feelings_knownterms_vis.html (Hannah)
    * [ADD FILE NAME] (Clark)
    * [ADD FILE NAME] (Trevor)

## feelings_knownterms_vis.html (Hannah)
* This visualization compares the feelings that people expressed concerning an Internet-connected future (question 3) and how much they know about some basic internet terms (question 9). By visualizing this information we were curious if there was a correlation between people who are excited for the future and if they were more or less knowledgeable about some of its terms.
* Task abstraction of the visualization: This visualization allows the viewer to discover a trend between people’s feelings of a connected future and how knowledgeable people are of certain basic Internet terms. The tooltip provides a way to annotate the data so the viewer can hover over the bar and see the raw data. The design of the bar chart provides a clear way to look at the trends in the data.
* Before visualizing this data I did some basic data analysis in a Jupyter Notebook (feelings_knownterms_preprocessing.ipynb) to preprocess the data and get it into a format that would be easier to use with D3, given my limited experience with Javascript. This preprocessing stage involved 6 steps:
    1. Create a smaller dataframe that included only the answers to questions 3 and 9 which I planned on visualizing. 
    2. Remove all rows that didn’t have a response to question 3 and/or 9 because I wouldn’t be able to do a comparison with those responses.
    3. Remove all of the rows of data that answered that they didn’t know any of the internet terms in question 9 because I wanted them to know at least one of them.
    4. Create two new columns: one that counts the number of null values in the question 9 answer columns, and one that converts that number to the number of terms that they knew.
    5. Run a groupby/aggregation function on question 3 and the number of terms the person knew.
    6. Convert this groupby/aggregation function dataframe into a csv file that can be easily visualized in D3. 
* Once the data was in a usable format I worked with it in D3. I used the code we worked on in class with the Shakespeare data and the D3 Worksheet, in addition to the code I wrote for the week 6 and 7 assignments. Since the data for question 3 is categorical, a bar chart was a good way to represent the data visually. The x-axis has the answer categories to question 3, and the y-axis has the aggregated average to how many terms were checked off for question 9. I choose to depict an aggregated average compared to each instance individually because I felt that a simple visual could better communicate the comparison. 
* How to run the file: The mozilla_df_infovis.csv file is in the repository so the feelings_knownterms_vis.html file should be able to run on its own.

## [ADD FILE NAME] (Clark)


## [ADD FILE NAME] (Trevor)