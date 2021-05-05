# ETL-Pipeline-for-Web-Scarping-and-Text-Analysis

Process of the code was as follows:

STEP-1: Loop through the excel file. 

STEP-2: In every iteration, URL's data was fetched from the SECFNAME column into the panda's data frame.

STEP-3: In every iteration, data from the HTML webpage is read through the URL Link.

STEP-4: After reading the data from the HTML page, HTML components are removed from it to get clean text data.

STEP-5: Once the data is ready using the above operations, then we start fetching specific sections of data using the function fetching_data().

STEP-6: The sections information is brought utilizing a straightforward methodology. For instance: if we want to extract the "RISK FACTORS" section data, this sections data would be present in the Table of Contents and the main section. We would be seeking the number of occurrences of "RISK FACTORS" in the fetched data and look particularly for the upper case because of the part where actual data is present starts with the "RISK FACTORS". So after finding the occurrence of RISK FACTORS in my data, data is sliced to start it from that position. To know where to end the search is decided by the "ITEM". If RISK FACTORS corresponds to ITEM 2, its next should be ITEM 3, which would be the endpoint. 

STEP-7: After all the three sections data has been fetched, all calculations are performed on it using various functions.

STEP-8: The output data frame is converted to an output excel file.
