# Data Analysis/Visualization of Covid-19 in WHO Regions Tool

## Description

The Data Analysis/Visualization of Covid-19 in WHO Regions Tool aims to provide analytical data frames and visual reprsentations of the most important statistics regarding the Covid-19 Pandemic on a global level. The format of the tool is that it is an ".ipynb" file that can be uploaded to Google Drive and Opened through Google Colab or downloaded to local system and opened through any IDE such as VSCode with Jupyter Notebook installed. The tool allows users to input any data regarding the pandemic and potentially any disease in the format of the example CSV file and perform various data analysis operations. Following that, the user is given the opportunity to perform various data anlaysis operations to generate DataFrames for specific data points such as Top 10 countries and WHO regions with active, recovered and death cases, and active, recovered and death stats over time in 2020. Finally, the tool allows the users to visually represent their DataFrames using Seaborn and Matplotlib. 

## Necessary Packages
**Google Colab Users:** <br>
1) Download the "Data_Analysis_Visualization_of_Covid_19_in_WHO_Regions.ipynb" from the repository.
2) Upload the file to your Google Drive.
3) Open the file using Google Colab and follow the instructions on the file. 
4) No other packages need to be installed as Google Colab comes iwth pre-installed Python libraries

**Local System Users:** <br>
1) Download and install a terminal such as Miniforge and the latest version of Python. <br>

2) Using Miniforge install Pandas, Seaborn, Matplotlib as follows: <br>
*   pip install pandas
*   pip install seaborn
*   pip install matplotlib

## Features
Feature 1: The tool reads in data from a CSV file based on covid-19 data. I impoted pandas and used “pd.read_csv” to correctly complete it. 

Feature 2: Using pandas, I will performed cleaning on the data. Performed multiple metrics collections using ".isna().sum", ".info()", and ".describe()". I dropped a few columns that I deemed as not necessary for the tool using ".drop". Finally, I used ".groupby" to create DataFrames for the data analysis operations.

Feature 3: I used the ".sum()" function coupled with ".groupby()" to acquire data for specific data points such as  the sum of active cases in each country in the entire data set as the original dataset presents the cases on a daily basis for each country. The preceding required me to search the columns for any mention of the specific key word whose values needed to be summed. In this situation, I searched the columns for each specific "country" and summed the active cases vales for them. Furthemore, I used sort_values for the active, death, and recovered cases columns to compute the top 10 countries that lead in each category and listed them in a table using “head(10).” I repeated the preceding process for the WHO regions and the covid-19 statistics over time in 2020. 

Feature 4: Using seaborn or matplotlib, I visualize plots as follows, but not limited to: Top 10 countries with most death cases, Top 10 countries with most active cases, active, recovered and death cases based on WHO region, and active, recovered and death stats over time. 

Feature 5: I interpreted data and plots using markdown cells and also discussed why I selected those specific plots. 

## Instructions
**Google Colab Users:** <br>
After following the instructions in the "Necessary Packages" section of this README file, follow the markdown cells on the loaded Google Colab file to fully utilize the tool. Run each cell in the order that they are presented while understanding the information from the markdown cells.

**Local System Users:** <br>
After following the instructions in the "Necessary Packages" section of this README file, load the file on your IDE such as Visual Studio and follow the markdown cells on the loaded file to fully utilize the tool. Run each cell in the order that they are presented while understanding the information from the markdown cells.

## Dataset used in the Tool
Worldmeter collects data from official reports, directly from Government's communication channels or indirectly, through local media sources when deemed reliable. They provide the source of each data update in the "Latest Updates" (News) section. Using this [source](https://www.worldometers.info/coronavirus/), I acquired data from the year of 2020.
