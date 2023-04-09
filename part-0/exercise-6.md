```mermaid
sequenceDiagram
    sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: sending user input
    deactivate server

    Note: since event.preventDefault was used, the default behaviour of re-rendering 
    the page will be interrupted, only making a single request 
```