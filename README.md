# Spark-MongoDB
 
Data - 
FireData.csv and ClimateData.csv -

These data files contain input data in CSV form.
FireData contains details about when Fires have occured in Victorian Cities
ClimateData contains the weather conditions measured at different weather stations.

PythonSocketProgram -
Reads data from both files using python csv library and sends it as separate streams into different sockets 

Spark Streaming Application - 

1. Reads events of from the client program and processes the rdds for both streams.
2. Gets the required fields from each rdd using Map transformation
3. Joins the two rdds using spark join 
4. Calls the action ForeachRdd to trigger the DAG
5. For each partition, process the streams and write to MongoDB

