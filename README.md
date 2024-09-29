erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ SALES : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    SALES ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
     ORDER-ITEM ||--|{ INVENTORY : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
    CUSTOMER {
        string customer_name PK
        string customer_id PK
        string email "customer's email"
    }
    PRODUCT {
        string product_id PK
        string size
        string price
        string color
    }
    INVENTORY {
        string product_id PK
        string amount_on_hand
        string amount_on_order
    }
SALES{string purchase price--Primary Key
string Tax}
