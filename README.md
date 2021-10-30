# Example of Extract, Transform, Load (ETL
This is an example of ETL. It is assumed that the data is located in a single source and stored using cloud storage. Data of different formats (csv, json, xml) are combined into a single file. The data undergoes a simple rounding transformation. Finally, the data is written into a csv format and stored in a seperate folder. The entire process can be done by calling a single function in a seperate helper file.

## Usefulness
This process can be made to be automated for continous processing of unstructured data. The process allows for processed data to be readily available for subsequent analysis. Feature transformations can be done at the beginning before Exploratory Data Analysis (EDA). The automated functions can be easily altered to accomadate any source and feature transformation. This process will save valuable time that can be spend on analysis. 

## Data
Motor vehicle data was provided by IBM:
https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0221EN-SkillsNetwork/labs/module%206/Lab%20-%20Extract%20Transform%20Load/data/datasource.zip

## Orientation of Important Folders in Repository
```
$ tree 
.
├── README_images
├── data_source_files
│   ├── used_car_prices1.csv
│   ├── used_car_prices1.json
│   ├── used_car_prices1.xml
│   ├── used_car_prices2.csv
│   ├── used_car_prices2.json
│   ├── used_car_prices2.xml
│   ├── used_car_prices3.csv
│   ├── used_car_prices3.json
│   └── used_car_prices3.xml
├── helper_files
│   └── etl_helper.py
├── transformed_data
│   └── dealership_transformed_data.csv
├── data_source_files   
│   └── data.zip
├── datasource.zip
├── dealership_logfile.txt
├── ETL Example.ipynb
├── ETL Test.ipynb
└── README.md
```

## Improvements
With continous data growth, having multiple copies of the dataset on file and in memory is inefficient. Additions should be made to delete files from the datalake. However, since errors are possible, a rollback system should be included with a second temporary storage prior to deletion. Also, visualizations to monitor characteristics and purity of the data. This can be taken a step further to include an alert system for data abnormalities.
