you can define

propagation type [[transaction_propagation]]
isolation level
timeout: amount of time that wrapped transaction timedout
readOnly: indicates that the trasaction is for read only op (any modification op will be executed normaly, it is just an indicaiton)

Rollback: for an exception
example:
```java
@Transactional(rollbackFor = { SQLException.class })
```


