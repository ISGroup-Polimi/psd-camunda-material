# Basic exercise

### Prerequisites
Software:
- Camunda 8 self-managed instance up and running
- Camunda Desktop Modeler

Skills. The following tutorials have been already completed
- [https://docs.camunda.io/docs/guides/orchestrate-human-tasks/](https://docs.camunda.io/docs/guides/orchestrate-human-tasks/)
- [https://docs.camunda.io/docs/guides/orchestrate-apis/](https://docs.camunda.io/docs/guides/orchestrate-apis/)
- [https://docs.camunda.io/docs/guides/orchestrate-microservices/](https://docs.camunda.io/docs/guides/orchestrate-microservices/)

### Text

Design and execute a process to support the definition of a quote for the renovation of an apartment. The process is carried out by the ACMEConcrete company.

The process begins with the acquisition by the ACMEConcrete company of the spending budget and the number of square meters of the apartment, 
the number of doors and the number of windows. The ACMEConcrete company will contact the ACMEWindows and ACMEFloor companies to request a 
quote for their part of the works. Once the quotation has been obtained, ACMEConcrete will check whether the total expenditure requested by 
the suppliers, to which their quota will be added, is lower than the budget. In this case, the process ends with an approval. 
Alternatively, the final say is left to the manager who will decide whether or not to lower the ACMEConcrete share to stay within budget limits.
