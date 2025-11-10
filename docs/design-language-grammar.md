# Design language Grammmar

## Create application
create application;
application.name=app1;

## Define applciation type
- console: application.type=console;
- http: application.type=http;
- web: application.type=web;
- mobile: application.type=mobile;

## Define programming language
application.language=js

## Define application entities
create entity;
entity.name=d1;
entity.schema={JSON schema}
application.entities.add=d1

## Define endpoints
- Console application
- http endpoint

### Endpoint specification
create endpoint;
endpoint.name=e1;
endpoint.description="prints hello world";
endpoint.type=POST;
endpoints.url=/abc/{abc}
endpoints.requestPayload=application.entities.d1
endpoints.responsePayload=application.entities.d2
application.endpoints.add=e1

## Define external services
External services can be defined as a plugin to Saral. The plugin will expose certain parameters that are required for it to interact with the external service. Plugin will also contain information about the APIs exposed by external service.
create externalService;
externalService.name=SaaS;
externalService.name=bookingConnector;
externalService.url=api.booking.com; // hardcoded in plugin unless tenant specific
externalService.authScheme=oauth-cc; // hardcoded in plugin unless multiple auth schemes are supported
externalService.clientId=w5tte454;
externalService.clientSecret=45435345;
externalService.scopes=default; // permissions allowed on SaaS
application.externalServices.add=externalService;

