
- health endpoint, health check
check if the app os working

	GET localhost:8080/actuator/health

aggregation of several health checks
you can add custom health checks

how much memory app is using

	GET localhost:8080/actuator/metrics/jvm.memory.used

check config props

	GET localhost:8080/actuator/configprops

metrics

	GET localhost:8080/actuator/health


monitor interact or control 

exposes all the endpoints
	management.endpoints.web.exposure.include=*

loggers endpoint


securing actuator endpoints:

enabling != exposing

enabling: creating
exposing: controls consumption http or jms

enabling and disabling endpoints:

	management.endpoints.enabled-by-default = false
	maangement.endpoint.name.enabled = true
	
exposing endpoints (http or jmx)
	management.endpoint.<PROTOCOL>.expose.include=(endpoint id)
	beans,metrics,info,healt....


HealthIndocator
InfoContributor





