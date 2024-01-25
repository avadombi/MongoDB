# CRUD operations

## 1. Create: Insert documents

```
db.my_collection.insertOne(document);

db.my_collection.insertMany([document, document, ...]);

document = {field: value, ...}
```

## 2. Read: Find documents

```
// find all documents
db.my_collection.find({}, projection);

// find documents that matches the specified conditions
db.my_collection.find(filters, projection);
filters = {
    field_1: {operator_1: value, ...},
    ...
}

// allow to specify fields you want to display. It is facultative
projection = {field_1: true, field_2: false, ...}

// projection is equivalent to:
SELECT field_1, ... FROM my_table;
```

## 3. Update: Modify documents

```
// update the first document that matches the specified filters
db.my_collection.updateOne(filters, [operators]);

// update all documents that match the specified filters
db.my_collection.updateMany(filters, [operators]);

filters = {...}  // apply update on data matching filters
operators = {
  update_operator: { field1: value1, ... },
  update_operator: { field2: value2, ... },
  ...
}  // update to apply
```

### Update operators

#### Behavior

![behavior](image.png)

#### Operators for Fields

![fields](image-1.png)

#### Operators for Arrays

* Operators
![arrays](image-2.png)

* Modifiers
![modify](image-3.png)

#### Bitwise
![bitwise](image-4.png)
