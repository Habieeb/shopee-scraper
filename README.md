# Web Scraping Python Code

This Python code is a web scraper that extracts sales, available stock, price, and name of each individual product from a product page.

## Prerequisites

To run this code, you need to have the following:

- Python 3.x installed on your machine
- Python libraries: pandas, requests

You can install the required libraries using pip:

```bash
pip install pandas requests

# Usage
Clone the repository or download the code files to your local machine.

Open the command line or terminal and navigate to the directory where the code files are located.

Run the code using the following command: python web_scraper.py

You will be prompted to enter the seller ID. Please provide the ID and press enter. 409068735

The code will start scraping the product page and extracting the desired information.

Once the scraping is complete, a CSV file will be generated in the specified directory. The file will contain columns for "Ad ID", "Title", "Stock", "Price", "Sales", "Rating", "Likes", "Views", and "Date".

You can find the CSV file in the specified directory with the filename formatted as "YYYY-MM-DD.csv", representing the date the scraping was performed.

## Additional Notes
The code follows ethical web scraping practices and respects the terms of service and usage policies of the target website.

The code includes a delay of 1 second between each request to avoid overwhelming the server.

Ensure that you have the necessary permissions to write to the specified directory for saving the CSV file.

Modify the code as needed to adapt it to your specific requirements.

## Original Code

The original code for this project was developed by [paulodarosa](https://github.com/paulodarosa/shopee-scraper). This repository includes updates and modifications made by [Habieeb](https://github.com/Habieeb/shopee-scraper).

For the original code and more information, please refer to the [paulodarosa](https://github.com/paulodarosa/shopee-scraper).

## Update and Modifications

1.	Introduced pandas library: The updated code imports the pandas library to facilitate working with data in the form of a DataFrame.
2.	Created a results list: The updated code initializes an empty list called results to store the extracted data from each ad.
3.	Appended data to the results list: Within the loop, the code appends the extracted ad information as a sublist to the results list.
4.	Created a DataFrame: After extracting all the data, the code creates a pandas DataFrame (df) from the results list. The column names are specified as ["Ad ID", "Title", "Stock", "Price", "Sales", "Rating", "Likes", "Views"].
5.	Saved DataFrame to a CSV file: The code uses the to_csv method of the DataFrame to save the data to a CSV file. The index=False argument is passed to exclude the index column in the CSV file.
6.	Added date column: The updated code extracts the current date using the date.today() function and creates a new column named "Date" in the DataFrame. The extracted date is assigned to this column for each row in the DataFrame.
7.	Extracted date from the CSV file name: The code uses the os.path.basename() and os.path.splitext() functions from the os module to extract the file name and extension from the CSV file path. It then uses the pd.to_datetime() function to convert the date string to a datetime object and extracts the date part using .date().
8.	Assigned extracted date to the "Date" column: The code assigns the extracted date to the "Date" column in the DataFrame.
9.	These changes allow you to store the extracted data in the form of a pandas DataFrame, add a separate "Date" column to the DataFrame, and save the data to a CSV file with the updated format.
