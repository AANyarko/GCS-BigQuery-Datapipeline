
1. Introduction and Overview
Purpose: This project automates the process of transforming data from a .xls format to .csv, reformatting a time column, storing the file in Google Cloud Storage (GCS), uploading the data to BigQuery, and visualizing it using Data Studio.

The pipeline is set to run daily via a cron job, ensuring up-to-date data processing and visualization.

2. Setup Process
Environment Setup:
Ensure Python (version 3.10 or above) is installed.
Required libraries: pandas, google-cloud-storage, google-cloud-bigquery.
IDE/Tools: Recommended to use VS code for development.

Google Cloud Setup:
Create a GCP account and enable APIs for BigQuery and GCS.
Set up a service account with appropriate permissions and download the JSON key file.

3. Script Usage
Data Transformation Script (data_transformation.py):
Purpose: Reads traffic_spreadsheet.xls, converts it to .csv, reformats the time column.
Usage: python scripts/data_transformation.py.
Parameters: Update input_file and output_file paths in the script.

GCS Upload Script (upload_to_gcs.py):
Purpose: Uploads the transformed .csv file to GCS.
Usage: python scripts/upload_to_gcs.py.
Data Format: Ensure .csv file is in the correct format.

BigQuery Loading Script (load_data_gcs_bigquery.py):
Purpose: Loads data from GCS to BigQuery.
Usage: python scripts/load_data_gcs_bigquery.py.
Configuration: Update bucket name, blob name, dataset, and table ID in the script.

4. Terraform Configurations
Resource Definitions:
Document each Terraform resource (GCS bucket, BigQuery dataset, table).
Describe purpose and settings of each resource.

Execution Instructions:
Run terraform init, terraform plan, terraform apply, terraform destroy.
Address common issues and errors.

