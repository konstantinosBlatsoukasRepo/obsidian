[[transactional]]

- required (default one, join an active trx or open a new one)
- supports (join an trx if one exists)
- mandatory (a transaction must  exists or  an exception is trown)
- never (throws an exception if gets called in the context of an active trx)
- not supported (suspends an active transaction)
- requires new (always starts a new trx for this method)