# Data Engineering E2E Project

This is a project that involves the full data lifecyle from ingesting the data to presenting it as a useful information in a report.

## Architecture
<img src="architecture.jpg">

## Softwares used

- This project uses python as the engineering language. 
- Collab notebook for transformation 
- Mage.ai for orchestration of pipeline - https://www.mage.ai/
- Cloud Storage to hold the raw data
- Virtual Machine to hold the Orchestrator
- Big Query 
- Looker Studio as a reporting and visualization tool


## Data Used

Here is the dataset used in the video - https://github.com/Sakindeb/DataTaxiAnalysis/blob/main/data/uber_data.csv

More info about dataset can be found here:

Website - https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Data Dictionary - https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf

## Relationship Diagram from Data Modelling
<img src="data_model.jpeg">

## Ingestion
The data ingestion is from the nyc.gov site that contains multiple dataset that are currently saved as parquet. This is converted to csv and stored in a public cloud storage bucket for access.

## Processing
The data is then transformed and split into the defined fact table and dimensional table formed from data modelling. The tables are formatted and saved in a format that is ready for use.
A mage pipeline automates the ingestion process using the public bucket url and uses the transformations in python to prep the data

## Load
The pipeline then loads the data to BigQuery. A datawarehouse for easy analysis and querrying of the data. This is then easily linked to a looker studio sheet. Some modifications are made to prepare summaries of the figures and describe the data from a consolidated table.


## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Credit
This project was built with the guide of Darshil Parmar. [Video](https://youtu.be/WpQECq5Hx9g?si=U8v1ICT1Ohy8vzU4)

## License

[MIT](https://choosealicense.com/licenses/mit/)
