# Daniel B. Data Engineer Task Solutions

This Repository contains Data engineer projects/task solution created by Daniel Beach. For those who don't know him - He's a preety cool Snr Data Engineer.

These solutions would be broken down into exercises, with each exercise focusing on a particular task handled by Data Engineers ranging from Easy to Hard. Including:

- Python data processing.
- csv, flat-file, parquet, json, etc.
- SQL database table design.
- Python + Postgres, data ingestion and retrieval.
- PySpark
- Data cleansing / dirty data.

If you're also looking to jump on the challenge [click here](https://github.com/danielbeach/data-engineering-practice)

## Exercises

### Exercise-1: Downloading files

The [first exercise](./Exercise-1/) tests one ability to download a number of files from an `HTTP` source and unzip them, storing them locally with `Python` using `various methods` and approach.

### Exercise-2: Web Scraping + Downloading + Pandas

The [second exercise](./Exercise-2/) tests one ability to perform `web scraping`, `build uris`, `download files`, and use `Pandas` to do some simple cumulative actions.

### Exercise-3: Boto3 AWS + s3 + Python

The [third exercise](./Exercise-3/) tests a few skills. This time we  will be using a popular `aws` SDK package called `boto3` to try to perform a multi-step actions to download some open source `s3` data files.

### Exercise 4 - Convert JSON to CSV + Ragged Directories

The [fourth exercise](./Exercise-4/) focuses more file types `json` and `csv`, and working with them in `Python`.
You will have to traverse a ragged directory structure, finding any `json` files
and converting them to `csv`.

### Exercise 5 - Data Modeling for Postgres + Python

The [fifth exercise](./Exercise-5/) is going to be a little different than the rest. In this problem you will be given a number of `csv` files. You must create a data model / schema to hold these data sets, including indexes,
then create all the tables inside `Postgres` by connecting to the database with `Python`.

#### Exercise 6 - Ingestion and Aggregation with PySpark

The [sixth exercise](./Exercise-6/) Is going to step it up a little and move onto more popular tools. In this exercise we are going to load some files using `PySpark` and then be asked to do some basic aggregation.
