Here is a simple flow chart:

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: HTTP POST request 
    activate server
    server-->>browser: URL redirect(to perform a new HTTP get request)

    browser->>server: Reloads
    activate server
    server-->>browser: causes 3 more HTTP requests (the style sheet, the JavaScript code, and the data.json)


```