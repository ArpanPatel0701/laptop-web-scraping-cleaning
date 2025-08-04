## This project scrapes laptop data from Flipkart using Python and performs thorough data cleaning

- Scrapes multiple pages of laptop listings from Flipkart.
- Extracts key attributes: name, image URL, ratings, processor, RAM, OS, display size, warranty, price and discount.
- Cleans messy fields and fills missing values using regex and logic.
- Converts text fields into clean numeric values for analysis.
- Final data exported to `laptop.csv`.

- `Data Analysis Process.ipynb`: Full code for scraping + cleaning
- `laptop.csv`: csv file
- `laptop_analysis_datset` : clean csv file
- `README.md`: This file

#### Libraries Used
- `requests`
- `BeautifulSoup`
- `pandas`
- `numpy`
- `re`

#### Clearning 
- Extracted brand names from the name column by taking the first word.
- Extracted numerical values from the rating and review columns and converted them to appropriate numeric data types.
- Extracted processor brand names from the processor column, corrected inconsistent values, removed incorrect entries by setting them to NaN, and filled missing processor values by extracting them from the name column.
- Added new columns for brand and processor generation extracted from the processor columns respectively.
- Shifted misplaced display-related values from the ram column to the display column. Filled missing RAM values by extracting them from the name column, extracted the numeric RAM size, and created a new column for ram_type.
- Replaced inconsistent values in the operating_system column and removed incorrect entries by setting them to NaN.
- Removed display-related values from the rom column by setting them to NaN, and extracted the numeric storage values using pattern matching. Filled some missing values by extracting relevant information from the name column.
- Removed incorrect values from the display column by setting them to NaN, extracted display size in centimeters using pattern matching, and converted the data type to numeric.
- Extracted the number of warranty years from the warranty column.
- Removed the ₹ symbol and commas from the actual_price and discount_price columns.
- Removed the % off text from the discount column and extracted only the numeric discount value.


#### Final data cleaning file : laptop_analysis_datset.csv

