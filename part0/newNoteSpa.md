``` mermaid
sequenceDiagram
    participant browser
    participant server

    Note over browser: New note created, added to notes list with command<br>`notes.push(note)` and rerenders note list on page

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new-note-spa
    activate server
    server-->>browser: HTTP Status Code 201<br>{"message":"note created"}
    deactivate server

```