Build the application
```
./mvnw package
```

Create a MySQL service instance with the name `mysql`
```
cf create-service cleardb spark mysql
```

Push the application to CF
```
cf push
```

Call the REST API to create one or more items.
```
curl --request GET \
  --url https://trace-explorer-demo-impressive-impala.cfapps.io/items
```

Call the REST API to fetch the available items.
```
curl --request POST \
  --url https://trace-explorer-demo-impressive-impala.cfapps.io/items
```

Open the PCF-Metrics UI for the application in a browser and search for the "Retrieve all items" log entry.
Open the Trace-Explorer for the entry with the little icon on the left and view all logs related to the specific Trace-ID.