# Process that calls a REST service

Note! This example can be designed only with the Desktop version of the Camunda Modeler. Refer to the [setup-connector](../setup-connectors.md) file to configure the Desktop Modeler before starting.

Before starting with this example it is required to:
- configure the  Desktop Modeler to enable the connectors (see [setup-connector](../setup-connectors.md) for the steps). Note! This example can be designed only with the Desktop version of the Camunda Modeler or with the SaaS - Web Modeler.
- run the [bookstore](https://github.com/ISGroup-Polimi/rest-examples/tree/main/bookstore) example 

The following steps must be executed:
- load the [call-rest-service](./call-rest-service.bpmn) process with Camunda Modeler
- check the *REST activity* properties. The server IP address in `URL` must be updated with the IP address of the machine where the bookstore REST service is running. Note! Putting *localhost* does not work as Camunda is running in containers and *localhost* means the container.
- deploy the process
- open the tasklist application http://localhost:8082 and run the process
- again on tasklist claim and execute the form to select the book

For more information about the REST API calls, refer to https://docs.camunda.io/docs/guides/orchestrate-apis/, https://marketplace.camunda.com/en-US/apps/415933/rest-connector