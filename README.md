# REST Client

A lightweight Java REST client focusing on flexibility, extensibility and resiliency.

## Rationale

## Features

* Standards compliance
  * JAX-RS
  * JAX-B
  * JSON-B
* Timeouts
  * Connect
  * Read
* Open tracing
* Fault tolerance
* Failure testing
* Heartbeats
* Real-time versus best-effort
  * Adaptive time-outs
  * Back-pressure
* Plugin architecture
  * All dependencies optional
  * Features enabled by the presence of optional dependencies
* Pluggable authentication
  * Basic authentication
  * OAuth2 authentication
* Asynchronous callbacks
* Alternate response marshaling

## Java SE (without CDI)

```(java)
RestClient client = RestClientBuilder
    .trace("blahdeeblah")
    .build();
```

## Java EE or Java SE (with CDI)

```(java)
@Inject
@Trace("blahdeeblah")
RestClient client;
```

## Resteasy client dependencies

``` (text)
edu.psu.swe.rest:rest-client:jar:1.0-SNAPSHOT
+- org.jboss.resteasy:resteasy-client:jar:3.5.1.Final:compile
|  +- org.jboss.spec.javax.ws.rs:jboss-jaxrs-api_2.1_spec:jar:1.0.0.Final:compile
|  +- org.jboss.resteasy:resteasy-jaxrs:jar:3.5.1.Final:compile
|  |  +- org.jboss.spec.javax.xml.bind:jboss-jaxb-api_2.3_spec:jar:1.0.0.Final:compile
|  |  +- org.reactivestreams:reactive-streams:jar:1.0.2:compile
|  |  +- javax.validation:validation-api:jar:1.1.0.Final:compile
|  |  +- org.jboss.spec.javax.annotation:jboss-annotations-api_1.2_spec:jar:1.0.0.Final:compile
|  |  +- javax.activation:activation:jar:1.1.1:compile
|  |  +- commons-io:commons-io:jar:2.5:compile
|  |  +- net.jcip:jcip-annotations:jar:1.0:compile
|  |  +- org.eclipse.microprofile.rest.client:microprofile-rest-client-api:jar:1.0:compile
|  |  \- org.eclipse.microprofile.config:microprofile-config-api:jar:1.1:compile
|  |     \- org.osgi:org.osgi.annotation.versioning:jar:1.0.0:compile
|  +- org.jboss.logging:jboss-logging:jar:3.3.1.Final:compile
|  \- org.apache.httpcomponents:httpclient:jar:4.5.4:compile
|     +- org.apache.httpcomponents:httpcore:jar:4.4.7:compile
|     +- commons-logging:commons-logging:jar:1.2:compile
|     \- commons-codec:commons-codec:jar:1.10:compile
+- org.eclipse:yasson:jar:1.0.1:compile
|  +- javax.json.bind:javax.json.bind-api:jar:1.0:compile
|  +- javax.json:javax.json-api:jar:1.1.2:compile
|  \- javax.enterprise:cdi-api:jar:2.0:compile
|     +- javax.el:javax.el-api:jar:3.0.0:compile
|     +- javax.interceptor:javax.interceptor-api:jar:1.2:compile
|     \- javax.inject:javax.inject:jar:1:compile
+- org.projectlombok:lombok:jar:1.16.20:compile
+- org.junit.jupiter:junit-jupiter-api:jar:5.2.0:test
|  +- org.apiguardian:apiguardian-api:jar:1.0.0:test
|  +- org.opentest4j:opentest4j:jar:1.1.0:test
|  \- org.junit.platform:junit-platform-commons:jar:1.2.0:test
+- org.junit.jupiter:junit-jupiter-params:jar:5.2.0:test
+- org.assertj:assertj-core:jar:3.10.0:test
\- org.mockito:mockito-core:jar:2.18.3:test
   +- net.bytebuddy:byte-buddy:jar:1.8.5:test
   +- net.bytebuddy:byte-buddy-agent:jar:1.8.5:test
   \- org.objenesis:objenesis:jar:2.6:test
```