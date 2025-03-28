This page is to show messages and message types between team members

Overall Example code: [AZ][SENDERID][RECEIVERID][MESSAGETYPE][VALUE][YB]

## Parts

[AZ]: This is the start of the message. This tells the the controller to start reading the message, all messages needs this to be read. 

[SENDERID]: This helps others see who sent the message. 

| Teammates | SENDER ID |
| ---------|---------|
|Zack | Z|
|Brendan | B|
|Carter | C|
| Sivannee | S |

[RECEIVERID]: This helps others see who needs to receive the message. 

| Teammates | RECEIVER ID |
| ---------|---------|
|Zack | Z|
|Brendan | B|
|Carter | C|
| Sivannee | S |

[Message type]: Shows what the value is going to be for.

| Message Types | Values |
| ---------|---------|
| Motor Freq | 1 |
| Wavelength | 2 |
| Motor on/off | 3 |
| NA | 4 |

[Value]: Shows the value for the message type that is sending through (Values are based what the message type is

| Message Types | Values |
| ---------|---------|
| Motor Freq | 90-800 |
| Wavelength | all positive values |
| Motor on/off | 0-1 |
| NA | 4 |

## Examples
1) AZCZ1500YB (Carter is sending Zack motor freq of 500)
