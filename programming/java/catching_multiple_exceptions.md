This feature introduced in java 7

```java
try {
    // execute code that may throw 1 of the 3 exceptions below.
} catch(SQLException | IOException e**) {
    logger.log(e);

} catch(Exception e) {
    logger.severe(e);
}
```