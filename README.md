# Phone-Number-Normalizer

![PHONE-NUMBER-NORMALIZER](PNN.png)

This workflow is an automated data cleaning and standardization pipeline designed to normalize customer phone numbers within a Google Sheets dataset. It ensures that inconsistent, manually entered phone numbers are transformed into a uniform international format and written back to the same data source for consistency.

It begins with a **Manual Trigger**, which allows the workflow to be executed on demand. This provides flexibility for running the process whenever new data is added or when updates are required, without needing full automation.

Next, the **Google Sheets (Read) node** fetches customer records from the spreadsheet. At this stage, the dataset contains raw phone numbers in inconsistent formats, including variations in prefixes, spacing, and symbols. This step serves as the data ingestion layer, bringing unstructured input into the workflow.

The workflow then moves to the **Code Node** (Normalize Phones), where JavaScript is used to clean and standardize phone numbers into an international format (e.g., +2547XXXXXXXX). It removes unwanted characters, converts local formats to international, and ensures consistent structure—improving data quality for use in APIs, CRMs, and communication systems.