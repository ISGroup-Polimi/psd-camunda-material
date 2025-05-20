# Processes that starts by a user after opening a form

This example refers to a simple process that, once deployed, can be started by a user after filling a form.

Steps:
- load the [form](./start.form) form with Camunda Modeler
- check the name of the form under *general properties* (e.g., `start_process_form`)
- deploy the form on Camunda
- load the [startevent-form](./startevent-form.bpmn) process with Camunda Modeler
- visualize the XML version (by clicking to the XML label in the bottom bar)
- check that the right form is indicated in the *formId* attribute of the *zeebe:formDefinition* tag. E.g.

```
<bpmn:startEvent id="StartEvent_1">
   <bpmn:extensionElements>
      <zeebe:formDefinition formId="input_form" />
   </bpmn:extensionElements>
   <bpmn:outgoing>Flow_1ht9f2p</bpmn:outgoing>
</bpmn:startEvent>
```

- deploy the process
- open the tasklist application http://localhost:8082 and run the process



### General rule

Once you have created a Form, take note of the id of the form and attach to your start event the highlighted portion of the XML. Please note that the extension must be placed right after the ``<bpmn:startEvent>`` tag
