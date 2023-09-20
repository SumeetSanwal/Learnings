## Schema Evolution

### Introduction
* Schema evolution is the process of modifying the structure of a database schema over time as new requirements and data models emerge. 
* It involves changing the schema to accommodate new data elements or changes to existing ones while preserving the integrity and consistency of the data.
* 

### Working 
* Different Type of schema evolution changes : 
  * Add – add a new column to the table or to a nested struct
  * Drop – remove an existing column from the table or a nested struct
  * Rename – rename an existing column or field in a nested struct
  * Update – widen the type of a column, struct field, map key, map value, or list element
  * Reorder – change the order of columns or fields in a nested struct

* Schema evolution should happen in a way to allow backward and forward compatibility.

* AVRO is quite matured at schema evolution but parquet just supports at the end i.e In parquet you can only delete and add new column from the end.

### Links 
* [Schema Evolution](https://stackoverflow.com/questions/37644664/schema-evolution-in-parquet-format)
