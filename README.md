# REST Client

A lightweight Java REST client focusing on flexibility, extensibility and resiliency.

## Rationale

TODO

## Features

* Standards compliance
  * [JAX-RS Client](https://docs.oracle.com/javaee/7/api/javax/ws/rs/client/package-summary.html)
  * [JSON-B](http://json-b.net/)
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
