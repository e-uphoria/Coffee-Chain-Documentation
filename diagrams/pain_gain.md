```mermaid
flowchart LR
    %% Subgraph identifiers must be simple
    subgraph Pains
        direction TB
        PA["Pains: Challenges in Coffee Chain ERP"]:::title
        P1["Manual sales tracking across multiple outlets"]
        P2["Menu updates not reflected automatically in sales"]
        P3["Limited visibility into customer leads and engagement"]
        P4["Difficulty in generating consolidated outlet/regional reports"]
        P5["Errors in manual data entry and pricing"]
        P6["Fragmented CRM data across outlets"]
    end

    subgraph Gains
        direction TB
        GA["Gains: Value Additions"]:::title
        G1["Centralized ERP platform: Outlets, Sales, Menu, CRM"]
        G2["Real-time menu updates reflected in sales products"]
        G3["Automated reporting dashboards for performance metrics"]
        G4["Enhanced decision-making for management"]
        G5["Improved customer engagement tracking"]
        G6["Reduced errors via automation"]
    end

    %% Connect pains to gains
    P1 --> G1
    P2 --> G2
    P3 --> G5
    P4 --> G3
    P5 --> G6
    P6 --> G1
    P3 --> G4
    P4 --> G4

    %% Styling for titles
   classDef title fill:#A52A2A,stroke:#333,stroke-width:2px,font-weight:bold;

    