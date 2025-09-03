```mermaid
flowchart TD
    %% Subgraphs with explicit titles
    subgraph CRM["Customer Relationship Management"]
        direction TB
        C1["Lead Capture"]
        C2["Customer Engagement"]
        C3["Targeted Marketing"]
    end

    subgraph OUT["Outlet Management"]
        direction TB
        O1["Outlet Name, Location"]
        O2["Manager, Regional Manager"]
    end

    subgraph MENU["Menu Management"]
        direction TB
        M1["Products & Categories"]
        M2["Prices & Customizations"]
    end

    subgraph SALES["Sales Department"]
        direction TB
        S1["Daily Transactions"]
        S2["Revenue Tracking"]
        S3["Performance Reports"]
    end

    %% Data flow arrows
    O1 --> S1
    O2 --> S2
    M1 --> S1
    M2 --> S1
    S1 --> S3
    S2 --> S3
    C1 --> S3
    C2 --> S3
    C3 --> S3
    S3 --> O2
    S3 --> CRM
