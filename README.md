# mongoDBLab

Download MongoDB from https://www.mongodb.com/

1. Commands
  use DatabaseName                                           // Set current database or create new database
  db                                                         // Get the name of the current database
  show dbs                                                   // Get the list of all databases
  db.CollectionName.inseart({"A":"a", "B":"b", "C":"c"})     // Add Document to the database at CollectionName 
  db.CollectionName.inseart([{"A":"a"}, {"A":"b"}])          // Add Documents to the database at CollectionName
  db.dropDababase()                                          // Delete current database
  db.createCollection(name,*{option1: val1, option2: val2}*) // Create Collection
                                                             // Options
                                                             //   1. capped: true (or flase) // If the collection exceeds the maximum memmory, delete the oldest data.
                                                             //   **YOU MUST SET size IF CAPPED IS TRUE**
                                                             //   2. size: number // Set the maximum memory of the collection. (number bytes)
                                                             //   3. autoIndex: true (or false) // Add "_id" field automatically. 
                                                             //   4. max: number // Set maximum number of documents in the collection.
  show collections                                           // Print collection list in the current database.
  db.CollectionName.drop()                                   // Delete collection CollectionName in the current database.
  db.CollectionName.find()*.pretty()*                        // Print CollectionName's documents.
  db.CollectionName.remove(criteria, *justOne: bool*)        // remove all documents from CollectionName that has criteria. If JustOne is true, delete the first one.
  
  2. Comparison Operation
  
    $eq   // Equal // db.find({"A":{$eq:"a"}})
    $gt   // Greater than // db.find({"A":{$gt:1}})
    $gte  // Greater than or eqaul 
    $lt   // Less than // db.find({"A":{$gt:1, $lt:5}})
    $lte  // Less than or equal
    $ne   // Not equal
    $in   // In // db.find({"A":{$in:["a", "b"]}})
    $nin  // Not in
    
  3. Logical Operation
  
    $and // db.find({$and: [{"A": "a"}, {"B": "b"}]})
    $not
    $nor
    $or
  
