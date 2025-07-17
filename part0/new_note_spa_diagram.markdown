```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User types a note and clicks "Save" in the SPA form
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note left of server: Server saves the note to the database
    server-->>browser: { "message": "note created", "content": "New note", "date": "2025-07-17" }
    deactivate server

    Note right of browser: Browser updates the notes list dynamically with JavaScript
```