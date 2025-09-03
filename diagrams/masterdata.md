```mermaid
%%{ init: { "layout": "lr" } }%%
classDiagram
    class ResPartner {
        +id
        +name
        +email
        +phone
        +type
    }

    class CoffeeOutlet {
        +id
        +name
        +location
        +owner_id
    }

    class CoffeeMenuItem {
        +id
        +name
        +price
        +image
        +category
    }

    class SaleOrder {
        +id
        +order_number
        +customer_id
        +outlet_id
        +order_date
    }

    class CRMLead {
        +id
        +lead_name
        +stage
        +related_order_id
    }

    ResPartner "1" --> "many" CoffeeOutlet : owns
    CoffeeOutlet "1" --> "many" SaleOrder : records
    ResPartner "1" --> "many" SaleOrder : places
    SaleOrder "1" --> "many" CoffeeMenuItem : includes
    SaleOrder "1" --> "0..1" CRMLead : linked_to
