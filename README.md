# MDS: Import CSV-Fitbit data in InfluxDB

This Python script is designed to import Fitbit data stored in CSV files into InfluxDB. It utilizes the pandas library to read CSV files and manipulate timestamps, and the influxdb_client library to connect to and write data to InfluxDB. This example uses Fitbitdata from the first month of a crowdsourcing project by Furberg, R., Brinton, J., Keating, M., & Ortiz, A. (https://doi.org/10.5281/zenodo.53894).

# Requirements
Python 3.x
pandas
influxdb_client
Installation

# Installation
1. Install Python dependencies:
pip install pandas influxdb_client

3. Set up InfluxDB:
Install and configure InfluxDB OSS (https://www.influxdata.com/products/influxdb/). Make sure it is running and accessible via HTTP.

# Usage
1. Clone this repository or download the script fitbit_data_import.py.
2. Modify the script with your InfluxDB credentials and CSV file paths.
3. Run the script:
   python fitbit_data_import.py
   Monitor the console for progress and error messages.

# Configuration
- Update the InfluxDB connection details (token, org, bucket, url) in the script to match your setup.
- Ensure that the CSV files (heartrate_seconds_new.csv, hourlysteps_new.csv, etc.) are in the same directory as the script or update the paths accordingly.

# Script Details
Files Processed:
- heartrate_seconds_new.csv: Heart rate data
- hourlysteps_new.csv: Steps data
- minutesleep_new.csv: Sleep data
- hourlycalories_new.csv: Calories data
- hourlyintensities_new.csv: Intensities data
- weightloginfo_new.csv: Weight log data

# Timestamp Handling
Timestamps in the CSV files are converted to RFC 3339 format before being written to InfluxDB.

# InfluxDB Client
The script uses influxdb_client to establish a connection to InfluxDB and write data synchronously.

# Data Writing
Data from each CSV file is processed and written to InfluxDB using a common function write_data(), which handles data formatting and error checking.

# Contributing
Feel free to contribute to this script by submitting issues or pull requests.

# License
This project is licensed under the MIT License - see the LICENSE file for details.
