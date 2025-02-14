## Message Types Diagram

This document describes the message types and structures used in the communication between boards.

## Message Type 1: Set Motor Parameter
- **Byte 1-2** (uint16_t): `0x01`
- **Byte 3** (uint8_t): Motor ID (X)
- **Byte 4-5** (uint16_t): Parameter Value (Y)

## Message Type: Button Pushed
- **Byte 1-2** (uint16_t): `0x43`
- **Byte 3** (uint8_t): Button ID

Each message type is defined by its first two bytes, followed by the necessary data depending on the message type.
