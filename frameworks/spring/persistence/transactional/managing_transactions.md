[[transactional]]

ACID (atomicity consistency isolation durability) -> all or nothing


@Transactional

important properties that you can set in the transactional annotation to 
change/customize the transaciton

- propagation 

- readOnly
  
This just serves as a hint for the actual transaction subsystem; it will _not necessarily_ cause failure of write access attempts. A transaction manager which cannot interpret the read-only hint will _not_ throw an exception when asked for a read-only transaction but rather silently ignore the hint.

https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/transaction/annotation/Transactional.html#readOnly--

- rollbcackFor
- noRollbackFor
