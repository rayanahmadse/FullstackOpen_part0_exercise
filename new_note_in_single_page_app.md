Here is a simple flow chart:

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: HTTP POST request(containing new note as JSON data)
    activate server
    server-->>browser: status code 201 created

    Note right of browser: This time the server does not ask for a redirect, the browser stays on the same page, and it sends no further HTTP requests.



```