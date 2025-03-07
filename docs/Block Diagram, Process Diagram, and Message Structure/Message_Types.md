## Message Types Diagram

This document describes the message types and structures used in the communication between boards.

# UART Messaging Protocol

This document defines the UART messaging protocol for our custom communication system.

---

## 1. Message Structure (64 Bytes)

Each message follows a repeated, but variable structure:

| Byte(s)  | Description                          |
|----------|--------------------------------------|
| **0**    | Start Indicator (`0x02`)            |
| **1-2**  | Message Type (See Message Types Table) |
| **3**    | Receiver Address (`0x00` - `0x03`)  |
| **4-61** | Message Data (Variable length)      |
| **62-63** | Stop Signal (`0x03`)               |
## 2. Message Types

The system supports different message types categorized into **Send (`S`)**, **Request (`R`)**, and **Error (`E`)**.

| Function                           | **Send (`S`)**  | **Request (`R`)** | **Error (`E`)**  |
|------------------------------------|---------------|---------------|---------------|
| **OLED display update**            | `0x10 0x00`   | `0x10 0x01`   | `0x10 0x02`   |
| **Voice input to microphone**       | `0x20 0x00`   | `0x20 0x01`   | `0x20 0x02`   |
| **Button input**                    | `0x30 0x00`   | `0x30 0x01`   | `0x30 0x02`   |
| **Confirm button press**            | `0x40 0x00`   | `0x40 0x01`   | `0x40 0x02`   |
| **Pitch info**                      | `0x50 0x00`   | `0x50 0x01`   | `0x50 0x02`   |
| **Pitch data in visual form**       | `0x60 0x00`   | `0x60 0x01`   | `0x60 0x02`   |
| **Output speaker imitation pitch**  | `0x70 0x00`   | `0x70 0x01`   | `0x70 0x02`   |
| **Update pitch display**            | `0x80 0x00`   | `0x80 0x01`   | `0x80 0x02`   |
| **Output OLED of data**             | `0x90 0x00`   | `0x90 0x01`   | `0x90 0x02`   |
| **Send data to Web**                | `0xA0 0x00`   | `0xA0 0x01`   | `0xA0 0x02`   |
| **Print data from microphone**      | `0xB0 0x00`   | `0xB0 0x01`   | `0xB0 0x02`   |
| **Print data from OLED**            | `0xC0 0x00`   | `0xC0 0x01`   | `0xC0 0x02`   |
| **Print data from Speaker**         | `0xD0 0x00`   | `0xD0 0x01`   | `0xD0 0x02`   |
| **Print data from Web Interface**   | `0xE0 0x00`   | `0xE0 0x01`   | `0xE0 0x02`   |

---

## 3. Error Handling

Error handling is integrated into the system using **resend requests** and error messages for each type of function.

| Condition                          | Response                                      |
|------------------------------------|----------------------------------------------|
| **Message Receive Error**                   | Resend Request `[0xEE, Sender Address]`     |
| **Specific Function Failure**       | Send corresponding Error message (`E` type from table) |
| **Max Retransmit Attempts Reached** | Message is dropped/logged after 3 tries                  |

---
