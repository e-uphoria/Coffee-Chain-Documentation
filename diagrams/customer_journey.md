```mermaid
sequenceDiagram
    actor Customer
    actor Staff as "Barista / Staff"

    participant Outlet as "Coffee Outlet (coffee.outlet)"
    participant MenuItem as "Coffee Menu Item (coffee.menu.item)"
    participant Order as "Sale Order (sale.order)"
    participant CRM as "CRM Lead (crm.lead)"

    Customer->>Staff: Places order (drinks/snacks)
    Staff->>Outlet: Identify outlet for the order
    Staff->>MenuItem: Add selected menu items to order
    Staff->>Order: Create sale order for the customer
    Order->>Outlet: Link order to outlet
    Customer->>Staff: Make payment
    Order->>CRM: Optional CRM lead association
    Staff->>Customer: Confirm order and receipt
    note right of Order: Sale recorded in system


