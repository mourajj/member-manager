## Member Manager

This is the member manager application, a crud application responsible for managing members.
![Diagrama em branco (1)](https://github.com/mourajj/go-full-crud/assets/27701706/07a52fc6-57df-4024-9209-856bf99b03a7)

This architecture is based on 2 more services:

### [Member-validator](https://github.com/mourajj/member-validator)  
Responsible for validating all the members created (gRPC)

### [Member-notification](https://github.com/mourajj/member-notification)
Responsible for initializing the kafka cluster and itself, in order to receive all the notification messages and log into AWS.

### Manager features
- A member has a name and a type the late one can be an employee or a contractor.
- - If it's a contractor, we want to store the the duration of the contract as an integer.
- - If it's an employee, we need to store their role, for instance: Software Engineer, Project Manager and so on.
- A member can be tagged, for instance: C#, Angular, General Frontend, Seasoned Leader and so on. (Tags will likely be used as filters later, so keep that in mind)
- There is a Kubernetes folder with the manifests of needed resources to deploy it on Kubernetes and receive external traffic


| Features     |                                                                |
|-------------------|----------------------------------------------------------------|
|                   | Separation of business logic and persistence layers            |
|                   | Input validations                                              |
|                   | Standard HTTP error codes                                      |
| **Code Quality**  |                                                                |
|                   | Code formatting, readability, maintainability, etc             |
|                   | Folders and packages structure                                 |
| **DevOps**        |                                                                |
|                   | Docker image to build/run the project                          |
|                   | DB migrations                                                  |
| **Documentation** |                                                                |
|                   | Documentation about the work done, how to run the project, etc |
| **Testing**       |                                                                |
|                   | Has tests                                                      |


## Running Locally

Clone the project

```bash
  git clone https://gitlab.com/codelittinc/golang-interview-project-jonathan-henrique.git
```

Run the docker command:

```bash
  docker compose up
```
## API Documentation

For more information about the requests / endpoints, feel free to import the [swagger.yaml](https://gitlab.com/codelittinc/golang-interview-project-jonathan-henrique/-/blob/dev/documentation/swagger.yaml) file to https://editor.swagger.io/
