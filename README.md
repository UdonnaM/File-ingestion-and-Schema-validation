# File-ingestion-and-Schema-validation

**Objective:**
The project involved testing various methods for reading a large dataset, performing data validation, and saving the data in a specified format.

**Methods of Reading Files:**
Pandas: The file was read in 47 seconds, demonstrating a relatively fast performance.
Dask: The file took 1 minute and 4 seconds to read. The slower performance compared to Pandas may be attributed to the overhead involved in Dask's parallel processing for this specific dataset size and configuration.
Modin and Ray: Both methods encountered errors and were unable to process the file due to the large size of the dataset and compatibility issues.

**Basic Validation on Data Columns:**
Column Name Cleaning: Column names were cleaned by removing any whitespace and special characters. The validation ensured that the dataset had consistent and appropriate column names.

YAML Schema:
File Created: schema.yml

Validation: Column validation against the YAML schema was successful, confirming that the dataset conforms to the expected schema.

File Writing:

Format: The dataset was saved in a pipe-separated format (|).

Compression: The file was compressed using gzip to reduce its size.

**File Summary:**
Total Number of Rows: 10,000,000
Total Number of Columns: 10
File Size: 2 GB

Conclusion:
Pandas provided the fastest read time among the methods tested. Dask, while slower, was still able to process the file, while Modin and Ray faced challenges with the dataset's size and other issues. The dataset was successfully validated, schema-defined, and saved in the required format.
