# BigQuery

To run against the database, provide the following environment variables:

- GOOGLE_APPLICATION_CREDENTIALS
- PROJECT_ID
- DATASET_ID
- LOCATION

`GOOGLE_APPLICATION_CREDENTIALS` should refer to an service account key file (this can be set by an appliation rather than locally).

`PROJECT_ID` is the id (not number) of the project and `DATASET_ID` is the name of the dataset that is used by default.

`LOCATION` is an (optional) datacenter location id where the query is being executed.
