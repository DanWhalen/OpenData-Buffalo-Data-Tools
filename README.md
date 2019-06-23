# OpenData Buffalo Data Tools

# Background
The Open Data Buffalo portal (data.buffalony.gov) is an online repository of downloadable data files regarding the demographics and municipal administration of Buffalo, NY (my hometown!). 

The website is maintained by the city government, is open to the public, and does not require sign-ups or accounts to use.

Some datasets available for download from Open Data Buffalo are actually created by the city of Buffalo itself, but most come from Federal and New York State sources.  Over 600 different datasets are accessible through Open Data Buffalo.

# Situation
Each dataset has its own distinct URL/landing page, where documentation/notes relevant to that particular dataset are posted.  

This set up is sufficient for researching specific datasets, one-by-one.  However, it can be a cumbersome and confusing set up for trying to research multiple datasets as a group (looking for common fields across datasets, finding potential join keys, understanding update schedules, how datasets may relate to each other, etc.).
 
I have developed these Python scripts (ODB Data Dictionary.py and ODB Data Map.py) to read the datasets' landing pages, and make simplified documentation files for them.  This makes exploring Open Data Buffalo quick and clear.

# How To Use
ODB Data Dictionary.py
User enters any number of URLs (each corresponding to a different Open Data Buffalo dataset the user is interested in) into a Python list.  The list is called 'target_urls', and it appears at the very start of the ODB Data Dictionary.py script.  Then the user runs ODB Data Dictionary.py.

ODB Data Dictionary.py outputs a series of html files, one for each URL the user entered into the 'target_urls' list.  Each of the html files contains a clean and simple data dictionary document corresponding one of the datasets.  

It also creates one large html file called "MASTER.html", which compiles those data dictionaries together into one document.

This provides the user with files which are ctrl+f searchable, formatted for easy printing, centralized, and devoid of extraneous information, media or formatting.  These documents make it easy for users to familiarize themselves with what data is available through Open Data Buffalo, and how it can and should be used.

ODB Data Map.py
User enters any number of URLs (each corresponding to a different Open Data Buffalo dataset the user is interested in) into a Python list.  The list is called 'target_urls', and it appears at the very start of the ODB Data Dictionary.py script.  Then the user runs ODB Data Map.py.

ODB Data Map.py outputs a .csv file.  Each row represents a data field name, and each column represents a dataset from the list the user provided.  A '1' at the intersection of a data field name (row) and a dataset name (column) indicates the data field appears in that dataset.

By sorting and filtering the .csv, the user can easily explore and identify datafields that are common across multiple datasets.  This enables quick and clear views of how Open Data Buffalo datasets relate to each other, and makes it much easier to discover opportunities for joining/merging datasets.
