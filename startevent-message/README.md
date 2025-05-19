# Processes that starts after receiving the message

This example refers to a simple process that, once deployes, starts when a message is sent to the orchestrator.

The message should contain the correlationKey set for the correlation variable `orderid`

Steps:
- load the [startevent-message](./startevent-message.bpmn) process with Camunda Modeler
- check the *start message* properties. `Global message reference` and `Name` must be set to `orderid`
- deploy the process
- send the message to the process 

```
curl -L 'http://localhost:8088/v2/messages/publication' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-d '{
  "name": "orderid",
  "correlationKey": "1",
}'
```

If any running instances for this model have been started with the same value for the correlation key, then the process should start and end immediately after running a.


For more information about how to handle messages in Camunda, refer to https://docs.camunda.io/docs/components/concepts/messages/
