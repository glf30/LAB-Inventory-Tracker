# Assignment - Inventory Tracker API

## Goals
- Create an API connected to a MongoDB database.  
- Allow users to **Create, Read, Update, and Delete** inventory items.  
- Practice filtering and limiting returned fields from documents.  

---

## Scenario
You are tasked with building an **Inventory Tracker API** for a small shop. The purpose is to manage the items the shop has in stock.

Your database will need one collection called `items` with a schema that includes:
- `name` (String, required, unique, e.g. "Notebook", "iPad")  
- `category` (String, e.g. "Writing", "Electronics")  
- `quantity` (Number, default: 0)  
- `price` (Number, required)  

---

## API Requirements
Your API should support the following actions:

1. **Create** a new item in the inventory.  
2. **Read** all items in the inventory.
3. **Read** a single item in the inventory given its ID.
4. **Update** an item given its ID.  
5. **Delete** an item given its ID.
6. Add the ability to filter items by `category`.  
7. Add the ability to view only the `name` and `price` of items.  
8. Add a route to search items by `name`.  

---

