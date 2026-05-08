sequenceDiagram
    participant browser
    participant server

    Note right of browser: User types a note into the text field and clicks Save
    Note right of browser: JavaScript handles the form submit event

    Note right of browser: JavaScript creates a new note
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: Server saves the new note
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: JavaScript updates the notes list on the page
