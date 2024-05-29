# Supporting materials for Process and Service Design course

This is a repo that contains useful material to operate with Camunda. The repo is specifically organized to support the work of the students attending to the Process and Service Design course


### How to add REST connectors to the Camunda Desktop Modeler

Camunda connectors for REST services can be found here [https://github.com/camunda/connectors/tree/main/connectors/http/rest](https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/)

Copy and paste the json file under element-templates in the Desktop Modeler configuration folder. The location of this folder depends on your OS. Look at [https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/](https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/) to know which is your location


### Application.properties to connect to the self-managed service

In case you need to configure your worker to be connected to a self-managed instance of Camunda, these are the parameters to set. In case of Java applications, they are usually placed in an application.properties file

```
zeebe.client.broker.grpcAddress=https://127.0.0.1:26500
zeebe.client.broker.restAddress=https://127.0.0.1:8080
zeebe.client.security.plaintext=true
```

### Link a form to a start event

Once you have created a Form, take note of the id of the form and attach to your start event the highlighted portion of the XML. Please note that the extension must be placed right after the ``<bpmn:startEvent>`` tag
```
<bpmn:startEvent id="StartEvent_1">
   <!-- copy from here -->
   <bpmn:extensionElements>
      <zeebe:formDefinition formId="input_form" />
   </bpmn:extensionElements>
   <!-- to here -->
   <bpmn:outgoing>Flow_1ht9f2p</bpmn:outgoing>
</bpmn:startEvent>
```

### Basic exercise

See [basic-exercise.md](basic-exercise.md)
