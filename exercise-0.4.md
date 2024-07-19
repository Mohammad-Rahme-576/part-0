sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a new note and clicks the Save button
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note { "content": "New note content" }
    activate server
    server-->>browser: 201 Created or the updated note list
    deactivate server

    Note right of browser: The browser updates the notes list with the new note