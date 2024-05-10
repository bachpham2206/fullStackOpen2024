```mermaid  
sequenceDiagram 
    participant browser
    participant server

    browser-->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server 
    server-->>browser: Status code 201. added {content: "peanut", date: "2024-05-10T11:08:07.236Z"}
    Note right of browser: Browser is not reload, stay on same page
    deactivate server
    
    Note right of browser: The browser executes the callback function that renders the notes