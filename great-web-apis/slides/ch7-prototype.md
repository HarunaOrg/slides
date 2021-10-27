# Prototype

!SLIDE

# Define

[OpenAPIv3](https://swagger.io/specification/)

Formerly "Swagger"

> The OpenAPI Specification (OAS) defines a standard, language-agnostic interface to RESTful APIs which allows both humans and computers to discover and understand the capabilities of the service without access to source code, documentation, or through network traffic inspection.

!SLIDE

# OpenAPI

> An OpenAPI document that conforms to the OpenAPI Specification is itself a JSON object, which may be represented either in JSON or YAML format.

!SLIDE

# OpenAPI

```yaml
title: Sample Pet Store App
description: This is a sample server for a pet store.
termsOfService: http://example.com/terms/
contact:
  name: API Support
  url: http://www.example.com/support
  email: support@example.com
license:
  name: Apache 2.0
  url: https://www.apache.org/licenses/LICENSE-2.0.html
version: 1.0.1
```

!SLIDE

# OpenAPI

```yaml
components:
  schemas:    # input and output shortcuts
  parameters: # inputs
  responses:  # outputs
paths: # API endpoints
  /some_path:
    get:
    
```

!SLIDE

# OpenAPI Paths: API endpoints

```yaml
paths:
  /some_path: # endpoint
    get: # HTTP method
      description: some_path description
      responses:
        '200': # success response code
          description: some_path success description
          content:
            application/json: # JSON response schema
```

!SLIDE

# OpenAPI Response Content

```yaml
content:
  application/json:
    schema:
      type: array
      items:
        $ref: '#/components/schemas/pet'
```

