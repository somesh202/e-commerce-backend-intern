## Database Schema:

### Table: Product

- **product_id** (Primary Key)
- name
- description
- Other product-related fields

### Table: Variant

- **variant_id** (Primary Key)
- **product_id** (Foreign Key referencing Product)
- color
- size
- price
- inventory_count
- Other variant-related fields

### Table: Order

- **order_id** (Primary Key)
- **variant_id** (Foreign Key referencing Variant)
- quantity
- order_date
- Other order-related fields

## Relationships:

- One-to-Many relationship between Product and Variant based on the `product_id` field.
- One-to-Many relationship between Variant and Order based on the `variant_id` field.

## Constraints:

- Primary Key constraint on `product_id` in the Product table.
- Primary Key constraint on `variant_id` in the Variant table.
- Primary Key constraint on `order_id` in the Order table.
- Foreign Key constraint on `product_id` in the Variant table, referencing `product_id` in the Product table.
- Foreign Key constraint on `variant_id` in the Order table, referencing `variant_id` in the Variant table.
