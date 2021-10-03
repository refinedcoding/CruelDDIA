231 - 238
## Errors handling
The transaction can be abort when an error happens and retry
The database should follow ACID principle so when a dangerous action happens, it will abort it.
## Weak isolation
When two transactions are independent, not write/read the same data, they could run parallel
Real applications need to afford many users at the same time, transaction isolation is needed to prevent concurrency happen
Serializable isolation works but the cost are high. That’s why to use weak (non-serializable) isolation
## Read Committed
Means read and write with only committed data. It prevents dirty reads and writes
### Implementing read committed 
By using row locks
## Snapshot Isolation and Repeatable Read 
Nonrepeatable read/ read skew
A transaction should read through a consistent snapshot of the database. It guarantees it read the committed data and changes are made based on this committed data
