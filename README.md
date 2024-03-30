## Logstash Pipeline for Indexing JSON Documents into Elasticsearch

### Overview
This Logstash pipeline is designed to ingest JSON documents from a file and index them into Elasticsearch. It removes unnecessary fields and then sends the processed documents to Elasticsearch for indexing.

### Pipeline Components
1. **Input**: Reads JSON documents from a specified file.
2. **Filter**: Parses the JSON content, removes unnecessary fields, and prepares the documents for indexing.
3. **Output**: Sends the processed documents to Elasticsearch for indexing.

### Usage
1. **Input File**: Place your JSON documents in the `data/input.log` file.
2. **Start Logstash**: Ensure Logstash is installed and running.
3. **Configuration**: Copy the provided Logstash pipeline configuration into a `.conf` file, e.g., `testdb.conf`.
4. **Start Pipeline**: Run Logstash with the specified pipeline configuration file:
   ```bash
   bin/logstash -f testdb.conf

### Pipeline Details
1. **Input**: Reads JSON documents from the specified file (data/input.log).
2. **Filter**:Parses the JSON content from the message field, Removes unnecessary fields such as @version, @timestamp, host, log, and event and Prepares the documents for indexing.
3. **Output**: Sends the processed documents to Elasticsearch for indexing and Specifies the Elasticsearch index name (testdb) where the documents will be indexed
### Requirements
1. Logstash installed and configured.
2. Elasticsearch running and accessible at http://localhost:9200.
3. Input JSON documents formatted correctly and placed in the specified file path.
### Contributors
[Jawadoch]


