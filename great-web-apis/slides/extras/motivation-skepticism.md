# Motivation and Skepticism

!SLIDE

# Web API Motivation

- Contemporary websites and apps
  - Dynamic javascript applications
- Robust tools and techniques
  - Web servers
  - Load balancers and high availability
  - Web-application frameworks
  - Security
- Third-party software, eg.
  - AWS, cloud-services APIs
  - InfluxDB: client-server interactions are over HTTP

!SLIDE

# Web API Skepticism

> "The Best Code is No Code At All"- [Jeff Atwood](https://blog.codinghorror.com/the-best-code-is-no-code-at-all/)

- Will a native client suffice? Eg. connecting directly to database or message queue.

- Is there something already written? OPenDAP, THREDDS, PostgREST, SDK, etc.

!SLIDE

# Web API Skepticism

> "Microservices: 'I wish my method calls had more latency'" - [Aaron Patterson](https://twitter.com/tenderlove/status/1337483916492488705)

- Dynamic, server-side HTML updates
  - Rails HTML Over The Wire (HOTWIRE)
  - Phoenix LiveView
