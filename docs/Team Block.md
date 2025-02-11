## Sequence Diagram of Team Communication 

sequenceDiagram
    participant Zack
    participant Brendan
    participant Sivanee
    participant Carter
    create actor W as WebUser
    create actor I as InPerson User
    Carter->>Zack: Sends velocity over
    I->>Carter: Sets velocity
    
