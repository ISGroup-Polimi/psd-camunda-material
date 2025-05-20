# Supporting materials for Process and Service Design course

This is a repo that contains useful material to operate with Camunda. The repo is specifically organized to support the work of the students attending to the Process and Service Design course




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
