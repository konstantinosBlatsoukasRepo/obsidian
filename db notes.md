
1. connect as root
```mysql
.\mysql.exe -uroot  (password empty)
```

2. 
```mysql
use nexushub
```

3.
```mysql
GRANT ALL ON *.* TO 'nexus'@'localhost' IDENTIFIED BY '';
```