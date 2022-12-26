```mermaid
sequenceDiagram
participant Client
participant NextcloudENV
Client->>NextcloudENV: GET ../apps/myapp
NextcloudENV->>routes.php: Check Routes
routes.php->>NextcloudENV: Route: / page index
NextcloudENV->>PageController.php: index()
PageController.php->>PageController.php: new TemplateResponse()
PageController-->>Templates: include..
```
