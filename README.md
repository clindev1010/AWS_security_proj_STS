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

Account A calls STS and callsback credentials
No long lived keys for attackers

-In Account A:
1. Build End to end Lambda calls public API that calls realtime location of ISS (space station)
2. It assumes a role in account B via STS and dumps ajacent results into S3 bucket
<img width="1265" height="773" alt="image" src="https://github.com/user-attachments/assets/1a11af27-c72a-49fb-b973-4951320259f1" />


STEP-by-step Approach
Select S3
<img width="592" height="349" alt="image" src="https://github.com/user-attachments/assets/f92635b0-b786-4efc-90b4-dd7c9769ce1a" />

<br>
<img width="1240" height="947" alt="image" src="https://github.com/user-attachments/assets/441295b0-1415-4a1c-9a19-cff920c5767e" />



