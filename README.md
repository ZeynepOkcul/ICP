# ICP
# Phone Book and Messaging System

This project is a basic implementation of a phone book and messaging system using the Motoko programming language. The system provides functionalities to manage phone book entries and send messages between users, storing them for later retrieval.

## Features

1. **Phone Book Management**:
   - Add new entries to the phone book with a name and phone details.
   - Retrieve phone book entries by name.

2. **Messaging System**:
   - Send messages from one phone to another, with a description and message content.
   - Retrieve the message history based on the sender's phone number.

## Data Structures

The project leverages two key data structures:
- `phoneBook`: A hash map storing phone book entries keyed by the user's name.
- `MessageHistory`: A hash map storing messages keyed by the sender's phone number.

## Functions

### Public Functions
- `insert(name: Name, entry: Entry): async ()`
  - Adds a new phone book entry.
  - **Parameters**:
    - `name`: The name of the contact.
    - `entry`: A record containing the description and phone number.

- `sendMessage(senderPhone: Phone, message: Message): async ()`
  - Sends a message from a sender to a recipient.
  - **Parameters**:
    - `senderPhone`: The phone number of the sender.
    - `message`: A record containing the recipient's phone number and the message content.

- `getPhone(name: Name): async ?Entry`
  - Retrieves a phone book entry by name.
  - **Parameters**:
    - `name`: The name of the contact to retrieve.
  - **Returns**: An optional `Entry` if found.

- `getMessage(senderPhone: Phone): async ?Message`
  - Retrieves the last sent message from a specific sender.
  - **Parameters**:
    - `senderPhone`: The sender's phone number.
  - **Returns**: An optional `Message` if found.


