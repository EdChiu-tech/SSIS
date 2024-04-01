# SSIS Solution for Kore Assignment

The goal of this SSIS Package is to import the data in the provided CSV file and migrate them to the production table. Below is a step-by-step description of the data flow of the SSIS package.

Step 1. Retrieve the CSV file in the Import CSV to Staging Table Data Flow Task.
			- CSV Import is the location of the CSV file as string values.
	 			- potential error where input is longer than 255 characters.  Log to error table.
		 	- Replace "null" and "" as NULL transformation and stored in new columns.
			- Data Type Conversion.  Using the new columns from previous transformation and converting the data types of each column to their respective SQL data types.
	 			- potential invalid data in a column such as a string in a numeric column. Log to error table.
		 	- Staging Table to Users where the appropriate data and typing is stored into the Staging Table for further transformations.

Step 2. Removing invalid UserID
			- As UserID should be unique and represents a client, rows that do not have a valid UserID should not be considered.

Step 3. 
			-
