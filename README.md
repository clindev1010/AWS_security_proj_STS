# AWS Security Project: STS (SERVICE TOKEN SERVICE)

- Cloud Structure Processes
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/11b71c4c-04c4-49a2-846e-48426cd6fdcf" />


-Traditional setup of Cloud system infrastructure
- ( Multiple AWS accounts, Dev, Staging, Prod, Shared Services)
<br>
<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/32f3ca8f-72e3-4eb1-a828-97ec7ff47bca" />


-
-
-
<br>
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/9eb5fcd7-cb07-4785-84e2-680c39ce5352" />
-account A has a Lambda/ ECS or a task that needs to do something in Account B
- It has permissions to assume a role that lives in Account B
- When Account B exposes the role in a trust policy & it says I trust account A to suit me and it has a permissions policy attached to it
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/7ccca7b0-d568-4b8e-90ed-5db8e6858a22" />
