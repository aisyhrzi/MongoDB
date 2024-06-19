# README for MongoDB Export and FastAPI Project
#For any questions or further help, please contact:
# - Name: Nur Aisyah Fatihah Binti Mohamed Rozi
# - Email:nur.aisyah.fatihah@graduate.utm.my
## Overview

This README file explains what is included in this submission for the MongoDB Export and FastAPI Project. It includes the exported MongoDB collections in JSON format, the FastAPI application code, and the MongoDB schema structure in JSON format.

## Deliverables

1. **MongoDB_caseB_json.txt**
   - This file shows the MongoDB schema structure in JSON format. It includes the structure of `protein_info`, `protein_interaction`, and `organism_info` collections.

2. **MongoDB_store.ipynb**
   - This explains how the CSV data was stored in MongoDB. The provided Python scripts read the CSV files and stored the data in MongoDB collections.
   - **Script to store CSV data in MongoDB**

3. **protein_info.json**
   - This file has the data from the `protein_info` collection in the `Assignment_B` MongoDB database.
   - Comes from Protein_Information.csv
   - Command used to export:
     ```
     mongoexport -d Assignment_B -c protein_info -o protein_info.json
     ```

4. **protein_interaction.json**
   - This file has the data from the `protein_interaction` collection in the `Assignment_B` MongoDB database.
   - Comes from Interaction_Data.csv
   - Command used to export:
     ```
     mongoexport -d Assignment_B -c protein_interaction -o protein_interaction.json
     ```

5. **organism_info.json**
   - This file has the data from the `organism_info` collection in the `Assignment_B` MongoDB database.
   - Comes from Organism_Information.csv
   - Command used to export:
     ```
     mongoexport -d Assignment_B -c organism_info -o organism_info.json
     ```

6. **caseB_fastApi.py**
   - This file has the FastAPI application code. The app has endpoints to get protein details, interactions, and proteins and interactions for a specific organism.
   - Main endpoints:
     - `/protein/{protein_id}`: Get details of a specific protein.
     - `/protein/{protein_id}/interactions`: Get all interactions for a specific protein.
     - `/organism/{organism_id}/proteins`: Get all proteins and their interactions for a specific organism.


## Instructions for Running FastAPI Application

1. **Set up the environment**:
   - Install the required packages:
     ```
     pip install fastapi
     ```

2. **Run the FastAPI application**:
   - Before run the fastapi make sure the python file in the correct path
   - Use this command to run the application:
     ```
     fastapi dev caseB_fastApi.py
     ```

3. **Access the API**:
   - You can find the API documentation at `http://127.0.0.1:8000/docs#/`.




