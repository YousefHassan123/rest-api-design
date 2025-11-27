# Filtering Endpoints Documentation

## Available Filters

### 1. Filter by Price Range
`GET /api/items?minPrice=10&maxPrice=100`

Returns all items whose price falls within the range.

### 2. Filter by Name
`GET /api/items?name=Book`

Returns items that match or partially match the provided name.

### 3. Filter by Category
`GET /api/items?category=electronics`

Returns items that belong to the provided category.

## Notes
- All filters can be combined together.
- Empty filters return all items.
