```mermaid
flowchart LR
    S["Suppliers"]
    I["Inputs"]
    P["Process"]
    O["Outputs"]
    C["Customers"]

    S --> I --> P --> O --> C

    %% Details
    subgraph Suppliers_Details
        S1["Outlet Managers"]
        S2["Menu Managers"]
        S3["CRM team"]
        S4["Accounting team"]
    end
    S --> S1
    S --> S2
    S --> S3
    S --> S4

    subgraph Inputs_Details
        I1["Outlet data (name, location, manager)"]
        I2["Menu items and prices"]
        I3["Sales transactions"]
        I4["Customer lead information"]
    end
    I --> I1
    I --> I2
    I --> I3
    I --> I4

    subgraph Process_Details
        P1["Record daily sales"]
        P2["Update menu items in ERP"]
        P3["Track customer leads"]
        P4["Generate outlet/regional performance reports"]
        P5["Analyze sales and CRM data"]
    end
    P --> P1
    P --> P2
    P --> P3
    P --> P4
    P --> P5

    subgraph Outputs_Details
        O1["Updated sales records"]
        O2["Real-time menu availability"]
        O3["Customer insights"]
        O4["Performance dashboards"]
    end
    O --> O1
    O --> O2
    O --> O3
    O --> O4

    subgraph Customers_Details
        C1["Outlet Managers"]
        C2["Regional Managers"]
        C3["Top Management"]
        C4["Sales Team"]
    end
    C --> C1
    C --> C2
    C --> C3
    C --> C4
