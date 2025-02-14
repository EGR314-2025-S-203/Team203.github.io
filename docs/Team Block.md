## Team Block

![Zacks Block](<drawing2.drawio.png>)

## Team Mermaid Diagram
```mermaid

sequenceDiagram
    actor W as WebUser
    participant Sivanee
    participant Brendan
    participant Zack
    participant Carter
  actor I as In-Person User
    
    I->>Carter: Sets velocity
    Carter->>Zack: Sends velocity data
    Zack->>Brendan: Notifies velocity change
    Brendan->>Sivanee: Updates velocity display
``` 

## Message Types
