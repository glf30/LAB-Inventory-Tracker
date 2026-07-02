# Assignment - Inventory Tracker API

## Goals
- Create an API connected to a MongoDB database.
- Allow users to **Create, Read, Update, and Delete** inventory items.
- Practice filtering and limiting returned fields from documents.
- Practice working with referenced relationships in MongoDB.

---

## Scenario
You are tasked with building an **Inventory Tracker API** for a small shop. The purpose is to manage the items the shop has in stock.

The shop purchases its inventory from different suppliers. Each inventory item should be associated with a single supplier, and each supplier may provide many different inventory items.

Your database will have two collections.

### `suppliers`
- `name` (String, required, unique)
- `email` (String)
- `phone` (String)

### `items`
- `name` (String, required, unique, e.g. "Notebook", "iPad")
- `category` (String, e.g. "Writing", "Electronics")
- `quantity` (Number, default: 0)
- `price` (Number, required)
- `supplier` (ObjectId referencing a Supplier, required)

---

## API Requirements

1. **Create** a new supplier.
2. **Read** all suppliers.
3. **Create** a new item in the inventory and associate it with a supplier.
4. **Read** all items in the inventory.
5. **Read** a single item in the inventory given its ID.
6. **Update** an item given its ID.
7. **Delete** an item given its ID.
8. Add the ability to filter items by `category`.
9. Add the ability to view only the `name` and `price` of items.  This could be a separate route or you could use query parameters!
10. Add a route to search items by `name`.  This should be done using query parameters. Any item that includes the search query in their name should appear in the result
11. When retrieving inventory items, populate the supplier information.
12. Add a route to retrieve all items supplied by a specific supplier.
