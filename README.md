# 🚖 NYC Taxi Trip Data Processing Project

This project involves processing and validating a 2+ GB CSV dataset of NYC yellow taxi trips using Python and modern data tools. The aim was to clean, validate, transform, and summarize the dataset for further use in analytics or ML workflows.

# 🗂️ Dataset
Source: NYC Yellow Taxi Trip Records (e.g., 2022 data)

Initial Size: Over 2 GB

Records: 11,908,509

Columns: 19

# ⚙️ Tools & Technologies Used

Google Colab (cloud environment)

Python Libraries:

pandas (primary processing)

dask (for performance comparisons)

pyyaml (for schema creation and validation)

os, gzip, io, and built-in modules

Output Format: Pipe-separated .txt.gz

Schema Format: YAML

# ✅ Key Steps Completed

Multiple File Readers Evaluated: Tested pandas and Dask for efficiency. Tried Modin, but session crashed after using all available RAM. This was probably because Modin with the Ray backend is optimized for parallel processing but requires significant shared memory to operate efficiently.

Column Validation & Cleanup: Removed special characters and trimmed whitespaces from column names.

YAML Schema Defined: Created a YAML file describing column names and file format (pipe-separated).

Validation: Ensured the column names and count matched the YAML schema.

File Output: Cleaned data saved in |-separated .txt.gz format.

# Summary Report Generated:

📄 Rows: 11,908,509

📊 Columns: 19

💾 File Size: ~206 MB

# 📁 Output Files
cleaned_data_output.txt.gz

schema.yaml
