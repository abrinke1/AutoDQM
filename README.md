# AutoDQM
AutoDQM parses DQM histograms and identifies outliers by various statistical tests for further analysis by the user. Its output can be easily parsed by eye on an AutoPlotter-based html page which is automatically generated when you submit a query from the AutoDQM GUI.

Example Page: http://uaf-7.t2.ucsd.edu/~jguiang/AutoDQM<br>
AutoPlotter: http://github.com/jkguiang/AutoPlotter

## Features

###### AutoDQM.py
- [x] Outputs histograms that clearly highlight outliers
- [x] Creates a .txt file along with each .pdf with relevant information on it
- [x] Allows user to easily change input
- [x] Seeks and accurately finds outliers

###### index.php
- [x] Previews input in a readable way
- [x] Gives a clear indication of the status of a user's query 

###### search.php
- [x] Allows user to quickly search data set names
- [x] Allows user to quickly search file name from selected data set name
- [x] Allows user to submit a retrieve query to index

###### database.php
- [x] Automatically generates a list of DQM files currently stored in a local database
- [ ] Allows user to manually refresh DQM file list
- [x] Allows user to submit a retrieve query to index

###### plots.php
- [x] Dynamically displays text files below AutoPlotter toolbar
- [x] Unique url's for sharing plots pages with the data and reference data set names

## Using AutoDQM

###### Setup:
Clone this repository and move its contents to a public html directory.

###### Main Page:
1. Select sample name
    - Currently supported samples: SingleMuon, Cosmics
2. Enter data and reference information
3. Click submit.
    - After process is complete, you will be automatically redirected to the "plots" page

###### Search Page:
1. Enter a data set name into the search bar
    - Supported regex expressions: Wildcards `*`
2. Click the search button
3. Select a data or reference data set
    - If applicable, choose a run from the file list generated by clicking the "Get File List" button
4. Repeat for other data set if necessary
5. Click the "Submit" button
    - The submission form can be toggled by using the "toggle submit form" checkbox

###### Database Page:
1. Select one of the automatically updated data sets
2. Use the radio menu to channel selection into either the data or reference form
3. Click the "Submit" button