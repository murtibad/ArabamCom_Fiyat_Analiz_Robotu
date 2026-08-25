# Arabam.com Price and Mileage Analyzer (RPA)

An automated Robotic Process Automation (RPA) workflow developed with UiPath Studio. This project scrapes used car listings from Arabam.com, processes the data, and generates a structured Excel report containing price categorization and average mileage per production year.

## Features
* **Dynamic Input:** Prompts the user for target car model, category, and the number of listings to scrape.
* **Web Scraping & UI Filtering:** Extracts listing data while filtering out sponsored advertisements using UI Selectors.
* **Data Cleansing:** Removes currency strings ("TL") and thousand separators, converting scraped string values into numeric types (Double/Integer).
* **Conditional Logic:** Categorizes vehicles into two separate DataTables based on an 800,000 TL threshold.
* **Data Aggregation:** Groups scraped vehicles by production year and calculates the average mileage for each year.
* **Excel Reporting:** Exports the categorized lists and calculated averages into a pre-formatted Excel template.

## Project Structure
The workflow is modularized using the `Invoke Workflow File` activity:
* `VeriCekme.xaml`: Handles user inputs and web scraping sequences.
* `VeriAnalizi.xaml`: Manages data cleansing, type conversions, and mathematical logic.
* `Raporlama.xaml`: Writes the final DataTables to the Excel report.

## Technologies Used
* UiPath Studio
* VB.NET
