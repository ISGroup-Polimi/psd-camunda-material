# Processes that waits for a message

This example refers to a simple process that, once started, wait for a message coming from outside of the orchetstrato.

The message should contain the correlationKey set for the correlation variable `orderid`

Steps:
- load the [catch-message](./catch-message.bpmn) process with Camunda Modeler
- check the *intermediate message* properties. `Global message reference` and `Name` must be set to `msg_description`
- deploy the process
- send the message to the process 

```
curl -L 'http://localhost:8088/v2/messages/publication' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-d '{
  "name": "msg_description",
  "correlationKey": "1",
  "variables": {
    "description": "foo"
  }
}'
```

If the message is sent when the process is not waiting for it, then - based on this configuration - the message is lost.


For more information about how to handle messages in Camunda, refer to https://docs.camunda.io/docs/components/concepts/messages/
