### Link a form to a start event

Nel caso serva definire dei dati in ingresso al process

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