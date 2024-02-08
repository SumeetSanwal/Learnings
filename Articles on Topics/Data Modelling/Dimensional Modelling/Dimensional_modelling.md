### Dimensional Modelling

- Dimensional modeling is a popular technique used to model data for analytics. At it's core, dimensional modeling revolves around organizing data into two types of datasets: fact tables and dimension tables. 
- Facts are usually comprised of numerical values that can be aggregated while dimensions hold descriptive attributes of entities/objects. 
- A key tradeoff the dimensional model makes is it denormalizes data (increases data redundancy) in order to speed up queries.

### Types of Design Pattern in dimensional Modelling
- Within dimensional modeling there are a few different schema design patterns: star schema (recommended in most cases), snowflake schema, and galaxy schema.

### Dimensional Modeling Advantages
- Intuitive to understand.
- Good query performance for analytics.
- Keeps track of historical changes easily.

### Dimensional Modeling Disadvantages
- Can be complicated to query sometimes.