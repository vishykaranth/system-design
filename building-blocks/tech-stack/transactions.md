## Isolation Level 1
- Both non-repeatable and phantom reads have to do with data modification operations from a different transaction, which were committed after your transaction began, and then read by your transaction.
- Non-repeatable reads are when your transaction reads committed UPDATES from another transaction. The same row now has different values than it did when your transaction began.
- Phantom reads are similar but when reading from committed INSERTS and/or DELETES from another transaction. There are new rows or rows that have disappeared since you began the transaction.
- Dirty reads are similar to non-repeatable and phantom reads, but relate to reading UNCOMMITTED data, and occur when an UPDATE, INSERT, or DELETE from another transaction is read, and the other transaction has NOT yet committed the data. It is reading "in progress" data, which may not be complete, and may never actually be committed.

## Isolation Level 2
- READ_UNCOMMITTED prevents nothing. It's the zero isolation level
- READ_COMMITTED prevents just one, i.e. Dirty reads
- REPEATABLE_READ prevents two anomalies: Dirty reads and Non-repeatable reads
- SERIALIZABLE prevents all three anomalies: Dirty reads, Non-repeatable reads and Phantom reads
- In fact transaction time consumption is in the following rate:
    - SERIALIZABLE > REPEATABLE_READ > READ_COMMITTED > READ_UNCOMMITTED
    
## References 
- https://stackoverflow.com/questions/11043712/what-is-the-difference-between-non-repeatable-read-and-phantom-read    