# Supporting materials for Process and Service Design course

This is a repo that contains useful material to operate with Camunda. The repo is specifically organized to support the work of the students attending to the Process and Service Design course


### how to add REST connectors to the Camunda Desktop Modeler

Camunda connectors for REST services can be found here [https://github.com/camunda/connectors/tree/main/connectors/http/rest](https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/)

Copy and paste the json file under element-templates in the Desktop Modeler configuration folder. The location of this folder depends on your OS. Look at [https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/](https://docs.camunda.io/docs/components/modeler/desktop-modeler/search-paths/) to know which is your location


### Application.properties to connect to the self-managed service
```
zeebe.client.broker.grpcAddress=https://127.0.0.1:26500
zeebe.client.broker.restAddress=https://127.0.0.1:8080
zeebe.client.security.plaintext=true
```

### Link a form to a start event
     <bpmn:startEvent id="StartEvent_1">
      <!-- copy from here -->
      <bpmn:extensionElements>
        <zeebe:formDefinition formId="input_form" />
      </bpmn:extensionElements>
      <!-- to here -->
      <bpmn:outgoing>Flow_1ht9f2p</bpmn:outgoing>
    </bpmn:startEvent>
