```java

@Entity

public class Project {

 @Id
 @GeneratedValue(strategy=GenerationType.AUTO)
 private long projectId;

 @OneToMany(mappedBy="theProject")
 private List<Employee> employees;

}

```

  

```java

@Entity

public class Employee {

 @Id
 @GeneratedValue(strategy=GenerationType.AUTO)
 private long employeeId;


 @ManyToOne
 @JoinColumn(name="project_id")
 private Project theProject;

```