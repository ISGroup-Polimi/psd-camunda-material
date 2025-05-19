## Setting up camunda

Here some convient hints to allow you the definition of processes with REST calls and integration with external applications.


### How to add REST connectors to the Camunda Desktop Modeler

This setup is required to allow you 

Camunda connectors for REST services can be found here [https://github.com/camunda/connectors/tree/main/connectors/http/rest](https://github.com/camunda/connectors/tree/main/connectors/http/rest)

Copy and paste the json file under element-templates in the Desktop Modeler configuration folder. The location of this folder depends on your OS. Look at [https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/](https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/) to know which is your location. If the ``element-templates`` folder does not exist, it must be created


### Application.properties to connect to the self-managed service

In case you need to configure your worker to be connected to a self-managed instance of Camunda, these are the parameters to set. In case of Java applications, they are usually placed in an application.properties file

```
zeebe.client.broker.grpcAddress=https://127.0.0.1:26500
zeebe.client.broker.restAddress=https://127.0.0.1:8080
zeebe.client.security.plaintext=true
```