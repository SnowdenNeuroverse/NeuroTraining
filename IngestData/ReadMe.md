# Ingest Data
This tutorial will show you how to setup an endpoint in neuroverse and capture any data sent to that endpoint in the datalake.
This tutorial will use an event hub as the endpoint which is well suited to large amounts of data coming from centralised data sources.
As opposed to an IOT Hub which is well suited to data coming from decentralised data sources (directly off devices).

### Content
1. Setup the event hub
2. Configure capture of the raw data being sent to that event hub
3. Send a test payload
4. Access the data landed in the DataLake using spark

#### TODO:
Show how to setup a scheduled spark job that transforms the raw data and stores it in sql or the datalake in a shape better suited for access (columnar format)
