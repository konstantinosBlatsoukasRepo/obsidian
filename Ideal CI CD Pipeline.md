Source -> 
Build -> 
Test Environemnt -> 
Prod Environment (1 box) 10% of traffic -> 
Prod Environment


Source: require reviewers
Build: compile, run unit tests, check coverage
Test Environment: run integration tests
Prod Environment: 

1) Alarms on Errors, Latency, Key Bussiness Metrics
2) Bake Period (error counts 9 latency breaches)
3) Canary




All infra specific to developer (isolated)
Dev environment (local) has it's own database (local to developer)

Test environment has it's own database

Prod environment has it's own database
