# sensor_streaming_data_pipeline
Data Pipeline is being built with the help of Kafka on confluent platform which will take streaming data from the sensors(producers) and will store data in data storage (consumer) that can be database, s3 bucket. 

This repo help us to know how to publish and consume data to and from kafka confluent in json format.

Step1: Create  a conda environment
```
conda create -p venv python==3.8 -y
```
Step2:
```
conda activate venv/
```
Step3:
```
pip install -r requirements.txt
```
Cluster Environment Variable
```
API_KEY
API_SECRET_KEY
BOOTSTRAP_SERVER
```
Schema related Environment Variable
```
SCHEMA_REGISTRY_API_KEY
SCHEMA_REGISTRY_API_SECRET
ENDPOINT_SCHEMA_URL
```
Data base related Environment Variable
```
MONGO_DB_URL
```
Set the above environment variables .

Run the produce_main.py to produce the data into confluent kafka topic.

Run the consumer_main.py to consume the data in parallel from kafka topic.

Data get consumed row by row from kafka topic to the mongo db database collection and it can be monitored, how the data inflow happening to the mongo db.
