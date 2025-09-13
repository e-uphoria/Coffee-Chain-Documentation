```mermaid
flowchart TD
    A([Start]) --> B[User fills Coffee Menu Item form]
    B --> C[Click Save or Create]
    C --> D{Is it a new record?}
    D -- Yes --> E[Create menu item record in coffee.menu.item]
    D -- No --> F[Update existing menu item record]
    E --> G[Call _create_or_update_product]
    F --> G[Call _create_or_update_product]
    G --> H{Does Linked Product exist?}
    H -- No --> I[Create new product.product record with name, price, type=consu, sale_ok=True, purchase_ok=False]
    H -- Yes --> J[Update existing product.product with new values]
    I --> K[Link product_id to coffee.menu.item record]
    J --> K[Confirm product_id remains linked]
    K --> L[Save customization options: milk_type, size, syrup_flavor, extra_shot]
    L --> M([End])
