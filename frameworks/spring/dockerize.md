
1. create a Dockerfile
```
 FROM openjdk:11-jre-slim

WORKDIR application

COPY ../../../target/xxx.jar ./

ENTRYPOINT ["java", "-jar", "xxx.jar"]
```

2.
docker build -f ./dirToDockerFile -t kbe-rest
docker run -p 8080 


dockerize

1. create a jar file (fat?)
2. create a docker image (Dockerfile)

```
FROM openjdk11
LABEL
ADD myJar.jar myJar.jar
ENTRYPOINT ["java", "-jar", "myJar.jar"]
```

4. from terminal, build the image
```
docker build -t nexus:1 .
```

5. run docker image in container
```
docker run -p 8080:8080 nexus
```


dockerize (docker channel)

unit of deployment -> the jar file (war, ear)

why docker

- repeatable and versioned
- cloud envs

1. build spring boot app
```
mvnw package
```
my code -> fat jar


## Dockerfile

FROM openjdk:17
COPY JAR
ENTRYPOINT["java", "-jar", "/app.jar"]


## Build image

```
docker build -t nexus:1 .
```

## run docker image in container

```
docker run -p 8080:8080 nexus:1
```

## spring config

- passed as arguments when app starts
```
docker run -p 8080:8080 nexus:1 --server.port=3000
```
- can passed as Docker run args

# Everything inside Dockerfile (too many layers)

```
FROM openjdk:11
WORKDIR /app

COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src src

RUN ./mvnw package
COPY target/*jar app.jar
ENTRYPOINT ["java", "-jar", "myJar.jar"]

```


## Multistage builds

```
# create the jar
FROM openjdk:11 as buildstage
WORKDIR /app

COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src src

RUN ./mvnw package
COPY target/*jar app.jar

# run the jar
FROM openjdk:11
COPY --from=buildstage /app/app.jar
ENTRYPOINT ["java", "-jar", "myJar.jar"]
```


palantir gradle plugin
jib plugin