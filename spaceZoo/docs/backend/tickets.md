
```mermaid
sequenceDiagram
    actor Visitor
    actor Ticket Vendor
    Visitor->>Ticket Vendor: "Ticket, please!"
    Ticket Vendor->>Visitor: "Money, please!"
    Visitor->>Ticket Vendor: Price of ticket
    Ticket Vendor->>Visitor: Ticket
```