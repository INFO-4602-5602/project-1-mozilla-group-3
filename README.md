# Group 3 README.md file
Trevor Buck, Clark Mousaw, Hannah Weber

## Team Roles:
The three of us in the group each created a visualization for the project. We did three visualizations so we each would have something to work on and so the work would be easily divided. We met twice outside of class to work on this project. 

## How to Run the Project:
We have three different HTML files to run the three visualizations. We will provide individual descriptions of our visualizations as well as information for how to run each file below.
    * feelings_knownterms_vis.html (Hannah)
    * Technical_knowledge_by_Country (Clark)
    * FeelingsbyCountry (Trevor)

## feelings_knownterms_vis.html (Hannah)
* This visualization compares the feelings that people expressed concerning an Internet-connected future (question 3) and how much they know about some basic internet terms (question 9). By visualizing this information we were curious if there was a correlation between people who are excited for the future and if they were more or less knowledgeable about some of its terms.
* Task abstraction of the visualization: This visualization allows the viewer to discover a trend between people’s feelings of a connected future and how knowledgeable people are of certain basic Internet terms. The tooltip provides a way to annotate the data so the viewer can hover over the bar and see the raw data. The design of the bar chart provides a clear way to look at the trends in the data.
* Before visualizing this data I did some basic data analysis in a Jupyter Notebook (feelings_knownterms_preprocessing.ipynb) to preprocess the data and get it into a format that would be easier to use with D3, given my limited experience with Javascript. This preprocessing stage involved 6 steps:
    1. Create a smaller dataframe that included only the answers to questions 3 and 9 which I planned on visualizing. 
    2. Remove all rows that didn’t have a response to question 3 and/or 9 because I wouldn’t be able to do a comparison with those responses.
    3. Remove all of the rows of data that answered that they didn’t k 555now any of the internet terms in question 9 because I wanted them to know at least one of them.
    4. Create two new columns: one that counts the number of null values in the question 9 answer columns, and one that converts that number to the number of terms that they knew.
    5. Run a groupby/aggregation function on question 3 and the number of terms the person knew.
    6. Convert this groupby/aggregation function dataframe into a csv file that can be easily visualized in D3. 
* Once the data was in a usable format I worked with it in D3. I used the code we worked on in class with the Shakespeare data and the D3 Worksheet, in addition to the code I wrote for the week 6 and 7 assignments. Since the data for question 3 is categorical, a bar chart was a good way to represent the data visually. The x-axis has the answer categories to question 3, and the y-axis has the aggregated average to how many terms were checked off for question 9. I choose to depict an aggregated average compared to each instance individually because I felt that a simple visual could better communicate the comparison. 
* How to run the file: The mozilla_df_infovis.csv file is in the repository so the feelings_knownterms_vis.html file should be able to run on its own.

## Technical_knowledge_by_Country  (Clark)
* This visualization utilizes two questions from the Mozilla survey data: the technical knowledge of each survey respondent (Question #1), and the country of origin of each respondent (Question 10). While the sample size probably doesn’t completely reflect the population of each country and their corresponding knowledge of computing technologies, we decided it would still be interesting to visualize these two survey questions.

* Task abstraction: The goal of this visualization is to show the viewer the average technical knowledge that survey respondents characterized themselves to have sorted by the countries of each respondent. 

* Question 1 of the Mozilla survey asked users if they consider themselves Ultra Nerds, Technically Savvy, Average Users, or Luddites in regards to their knowledge of technology. The visualization that displays this data was created in d3. I assigned numeric values to each response with Ultra Nerd being the highest at 4, and Luddite being the lowest at 1. Respondents that answered in the beta before this question was asked or that had unexpected data values in the spreadsheet were given scores of 2 (Average User). The number of responses for each country required to be included in the visualization was 750 responses.


## FeelingsbyCountry (Trevor)
* This visualization compares the feelings that people expressed concerning an Internet-connected future (question 3) and which country they are from.  This comparison would give us insight about the priorities and concerns of each individual country.  We thought it might be interesting to find out which demographics are more troubled with the takeover of the internet.
* Task abstraction: ...
* Process: In order to create this visualization, I needed to take a deeper look at question 3.  I started by assigning each response a number value corresponding to the level of concern.  For example, the answer: "Scared as Hell" was given the highest value of 5, whereas the answer, "Super excited!" was given the value of 1.  I then summed all of the value to create a score for each country.  To normalize the data, I divided the score by the number of responses given by each country.  This gave me a number on a scale from 1 to 5.  I then plotted these numbersdrawing heavily from the barchart example used in class.  After doing this, I realized that the visualization was way too complex.  There were too many countries/data points to fit on one graph.  So I filtered the data by only showing the countries with at least 500 responses. 
* How to run: The file can run remotely.  The only two files that need to be downloaded are the original csv file (*named here*) and feelingsByCountry.html

