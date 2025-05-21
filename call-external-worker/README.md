# Process that calls an external component

In this case the process calls an external component that has been developed with node.js

Steps:
- load the [call-external-worker](./call-external-worker.bpmn) process with Camunda Modeler
- select the user task *call-worker*
- check, under *task definition* of the user task, the value of *job type* that must be equal to *charge-card-worker* 
- deploy the process
- run the [worker](./worker/) developed with node.js 
- run `node worker.js`
- open the tasklist application http://localhost:8082 and run the process


For additional information on how to use node js sdk refer to https://docs.camunda.io/docs/apis-tools/node-js-sdk/