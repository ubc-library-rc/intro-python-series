# Intro to Python: 5-Part Workshop Series
### UBC Library Research Commons

:heavy_exclamation_mark: This workshop is in development and not yet complete. :heavy_exclamation_mark:

Description: This set of 5 workshops is an introduction to Python programming, with a focus on skills that would be relevant to students and researchers who are working with data, particularly tabular data.

The 5 workshops have the following goals:
1. To understand the basics of Python syntax, variables, and data types.
2. To learn how to work with tabular data in Python, including reading, manipulating, and visualizing data.
3. To learn how to automate tasks in Python, including working with multiple files.
4. To learn to use logic and modularity to make Python code flexible and reusable.
5. To develop good habits for programming for research in Python, including handling errors, debugging, and writing reliable code.

These workshops can count towards the [Canadian Certificate in Digital Humanities](https://ccdhhn.ca/).

Participants need to sign up for each workshop individually.
It is not necessary to sign up for the first workshop in order to do the second (and so on), but note that each workshop will build on the topics covered in previous workshops in this series.

# Setup Instructions
In these workshops, we will write Python code in a text editor called Visual Studio Code (VS Code).

NOTE: Feel free to use you own preferred text editor or Jupyter Notebooks to write code in these workshops, but keep in mind that some aspects may be unpredictably different from the way things appear on my screen. For example, I will frequently use the Python Debugger in VS Code, and other text editors may have an entirely different mechanisms for debugging, and you may have to figure that out on your own. If you want to follow what I'm doing exactly, you should install VS Code and the extensions that I list below.

### Please follow the following steps/links to complete the setup for this workshop series.
1. Install a [**Python Interpreter**](https://code.visualstudio.com/docs/python/python-tutorial#_install-a-python-interpreter)
2. Install [**Visual Studio Code**](https://code.visualstudio.com/Download)
3. Install the [**Python extension for VS Code**](https://marketplace.visualstudio.com/items?itemName=ms-python.python). If you want more info on installing extensions for VS Code, see [this page on their "Extension Marketplace"](https://code.visualstudio.com/docs/configure/extensions/extension-marketplace)
4. Install this [**Python Debugger extension for VS Code**](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy)


Link to workshop: https://ubc-library-rc.github.io/your_workshop_repository_name/

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.


## Data information

### Data from The Canadian Library Challenges Database

File: `2026-01_canadian-library-challenges-database_SUBSET.csv`

#### Search parameters

- Year: 2015-2025 inclusive
- Form of complaint: Direct
- Object Category: Collection

#### Attribution

The Canadian Library Challenges Database. (n.d.). Centre for Free Expression. Retrieved February 17, 2026, from https://cfe.torontomu.ca/databases/canadian-library-challenges-database


#### Data from Google Trends

Files:
- Search 1 - top 8 books: `2026-02-18_google-trends-search-1.csv`
- Search 2 - second-to-top 8 books: `2026-02-18_google-trends-search-2.csv`

#### Search parameters

- Location: Canada
- Time: Past 5 years
- Type: Web search

#### Data manipulation and preprocessing

- The data was transposed (switched rows and columns) to match the data format in the Python workshop.
- The column label "Time" (turned into a row label) was deleted
- The data for search 1 was multiplied by 16/100 to make the two datasets have the same scale. Here's why and how I did this:
  - In the timeline chart of Google Trends, the max value for each search is 100 because all the values are normalized by the highest-searched item included in the search.
  - Therefore, separate searches will be normalized differently.
  - To address this, [I searched the item from each search that reached 100](https://trends.google.com/explore?q=%2Fm%2F07gyh9%2C%2Fg%2F11hz_gm9qv&date=today%205-y&geo=CA), and searched for them together; the results were as follows:
    - "Irreversible damage" (top item in search 1): 16
    - "If I ran the zoo" (top item in search 2): 100
  - Therefore, I normalized the data for search 1 so that the max value would be 16.

#### Information about the variable "Interest over time"

"Search interest over a specific time period, displayed on a relative scale from 0 to 100, where 100 signifies the peak interest for the time period of the chart. A value of 50 indicates half the popularity of the peak, and 0 suggests insufficient data." Google Trends (https://www.google.com/trends)

#### How the books were chosen

These were the top 16 most-challenged collection items in the dataset above (see the section "Data from The Canadian Library Challenges Database"). The number 16 was chosen because Google Trends allows you to search for 8 items at a time, and we wanted more than one data file.

#### Attribution

Data source: Google Trends (https://www.google.com/trends).

##### Search 1: items 0 - 7 (top 8 items)

Explore—Google Trends. (n.d.). Retrieved February 18, 2026, from https://trends.google.com/explore?q=%2Fg%2F11hz_gm9qv%2C%2Fg%2F11cm5t1r8x%2C%2Fm%2F06bc_tf%2C%2Fg%2F11fhkd2xsf%2C%2Fg%2F11fpgh5btl%2C%2Fg%2F11k0nr3vkf%2C%2Fg%2F11mh_xnf0v%2C%2Fg%2F11c52jc9ts&date=today%205-y&geo=CA

##### Search 2: items 8 - 15 (second-to-top 8 items)

Explore—Google Trends. (n.d.). Retrieved February 18, 2026, from ttps://trends.google.com/explore?q=%2Fm%2F04z1z%2C%2Fm%2F07gyh9%2C%2Fg%2F11qmbfjbc1%2C%2Fm%2F04t2rjn%2C%2Fm%2F0gt2b%2C%2Fg%2F11c707_d0x%2C%2Fg%2F11g1lvjqp2%2C%2Fg%2F11xcmp1fbp&date=today%205-y&geo=CA