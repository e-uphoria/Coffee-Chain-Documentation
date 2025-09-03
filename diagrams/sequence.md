```mermaid
sequenceDiagram
    actor User

    participant OutletCustomer as "Outlet Owner (res.partner)"
    participant Outlet as "Coffee Outlet (coffee.outlet)"
    participant MenuItem as "Coffee Menu Item (coffee.menu.item)"
    participant SaleCustomer as "Sale Customer (res.partner)"
    participant Order as "Sale Order (sale.order)"
    participant CRM as "CRM Lead (crm.lead)"

    User->>OutletCustomer: Create or manage outlet owner
    note right of OutletCustomer: Owner of the coffee chain outlet

    User->>Outlet: Create/view outlet
    Outlet->>OutletCustomer: Assign owner
    note right of Outlet: Outlet now linked to the owner

    User->>MenuItem: Create menu items (drinks/snacks)
    note right of MenuItem: These can be added to sale orders later

    User->>SaleCustomer: Create/manage sale customer
    note right of SaleCustomer: Customer who buys items at the outlet

    User->>Order: Create sale order
    Order->>SaleCustomer: Assign sale customer
    Order->>Outlet: Assign outlet where order is placed
    Order->>MenuItem: Add menu items
    Order->>CRM: Link lead if applicable
    note right of Order: Sale order now contains customer, outlet, menu items, and CRM link



