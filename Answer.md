## Answer of Assignment

# 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
1. One-to-Many Relationship: Typically, the relationship between "Product" and "Product_Category" entities is one-to-many. This means that one product category can have many products associated with it, but each product is associated with only one product category.

2. Foreign Key Constraint: In the "Product" table, there is usually a foreign key column that references the primary key of the "Product_Category" table. This foreign key establishes the relationship between the two entities.

3. Attributes: The "Product" entity would likely contain attributes such as product ID, name, description, price, etc. The "Product_Category" entity, on the other hand, would typically contain attributes such as category ID and name.

4. Normalization: This relationship helps in normalizing the database schema, as it avoids data redundancy. Instead of storing the same category information for each product, the product table references the category table using foreign keys.

5. Queries and Reporting: This relationship enables efficient querying and reporting. For instance, you can easily retrieve all products belonging to a particular category or analyze sales performance by category.

# 2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
1. Foreign Key Constraint: Create a foreign key constraint in the "Product" table that references the primary key of the "Product_Category" table. This constraint ensures that every value in the foreign key column of the "Product" table must exist as a primary key value in the "Product_Category" table.

2. Declare Foreign Key Constraint: When creating or modifying the schema, ensure that the foreign key constraint is properly declared. This is usually done using SQL syntax during table creation or alteration.

3. Cascading Actions: Optionally, you can specify cascading actions on the foreign key constraint. For instance, you might choose to cascade deletes or updates, meaning that if a category is deleted or updated in the "Product_Category" table, the corresponding products in the "Product" table will also be deleted or updated accordingly.

4. Error Handling: Implement proper error handling mechanisms in your application or database management system to deal with cases where an attempt is made to insert or update a product with an invalid category.
