# Avro (in go)
Pros:
- using schema: clear structure, type and meaning (through documentation) of the data
- encode more efficiently
- smaller size: metadata such as the field names don’t have to be explicitly encoded in the data (because the schema is provided at decoding time)

Cons:
- Doesn't have offical avro library for go
- Inconvenient to work with multiple consumers (compare with json), because we need to attach schema along with avro data (it means we need to provide them a way to get schema)
- A lot of extra work to control schema version (Schema Evolution)

There are 2 most popular libraries for go and avro
https://github.com/linkedin/goavro : generates a class file corresponding to the schema
- Need to generate go files based on schema files
- Easy to deserialize /unserialize
- Can use struct directly


https://github.com/alanctgardner/gogen-avro : directly read the schema using parsers library.
- No need to generate anything, everything is on the fly
- Can't use struct directly, unserialize data is map of interfaces (or I can't find it out with their poor document)

Json
Pros:
- Easy to read/write: no need schema, no need to use new library
Cons:
- missing is contractfor data between the producers and the consumers: if an upstream team make changes to the data format, then it becomes very difficult to ensure that all downstream consumers will (continue to) be able to interpret the data.
- heavier




Reference:
* https://github.com/alanctgardner/gogen-avro/issues/31
* https://docs.confluent.io/current/avro.html#avro-backward-compatibility
* https://www.tutorialspoint.com/avro/avro_overview.htm
* http://avro.apache.org/docs/current/
* https://github.com/alanctgardner/gogen-avro
* https://github.com/linkedin/goavro
