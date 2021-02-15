# CFIA Food Recall Web Scrapping Using Selenium and BeautifulSoup
Extracting Food Recalls & Alerts from the Government of Canada's Website

## Context

In the food industry, HACCP (Hazard Analysis and Critical Control Points) is a systematic approach to the identification, evaluation, and control of food safety hazards. A hazard is any biological, chemical or physical agent that is likely to cause illness or injury in the absence of its control. 

For example, a biological hazard can be Salmonella. A chemical hazard can be an additive that causes allergies such as sulphites. A physical hazard can be plastic, metal or hair. 

The process of hazard identification usually involves a brainstorming session with individuals who have specific knowledge and expertise appropriate to the product and process. This is called the HACCP team. The team is multidisciplinary and includes individuals from engineering, production, sanitation, quality assurance, and food microbiology.

In addition, hazard identification also involves looking at historical food safety recalls. This data is usually available by government agencies in charge of food safety. In Canada, this data is collected by the CFIA (Canadian Food Inspection Agency) and can be found on the following [website](https://healthycanadians.gc.ca/recall-alert-rappel-avis/search-recherche/simple/en?s=&plain_text=&f_mc=1&js_en=&page=50&per_page=). However, the data lacks a download link to be further analyzed to inform our HACCP plan accurately.

## Objective

The objective of this project is to scrap the data from the CFIA website and export it into a .csv file for further analysis using Excel, Tableau or Python.


## Approach

**1. Selenium and BeautifulSoup**
* Selenium and BeautifulSoup allows to access specific tag elements in the HTML source code.
* The website source code is accessed using the developer tools in Chrome.

**2. Extracting Recall Hyperlinks and Titles**
* BeautifulSoup is used to access each tag element where our data of interest is located.
* The text of each tag element is extracted and appended to a list using dictionaries.

**3. Extracting Recall Details**
* The initial page does not contain important information such as date of recall, hazard type, brand name, company, etc. This information is available when you click on each hyperlink. Therefore, every link is accessed to extract the data of interest.

**4. Extracting Recalled Products**
* Each recall or row in our dataset can have more than one product affected. We can extract ALL of the products affected into a single list by accessing the hyperlink of each recall.


## Results
This project extracted close to 100% of the food recalls listed in the Government of Canada's website.

## Next Steps
The extracted data needs to be explored, cleaned and visualized to draw insights that can inform our HACCP plan.
