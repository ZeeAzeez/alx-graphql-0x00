# GraphQL Character Query Project

## Objective

This project demonstrates how to write GraphQL queries to retrieve character information from the Rick and Morty API using both single character queries and paginated list queries.

## Endpoint

GraphQL API: `https://rickandmortyapi.com/graphql`

## Tasks

### Task 1: Single Character Queries

Write GraphQL queries using the `character(id: ID!)` field to fetch details of specific characters with IDs 1, 2, 3, and 4.

**Fields Retrieved:**

- `id`: Character ID
- `name`: Character name
- `status`: Character status (Alive, Dead, or Unknown)
- `species`: Character species
- `type`: Character type/subspecies
- `gender`: Character gender

### Task 2: Paginated Character Lists

Write GraphQL queries using the `characters(page: Int)` field to fetch paginated lists of characters for pages 1, 2, 3, and 4.

**Fields Retrieved:**

- `id`: Character ID
- `name`: Character name
- `status`: Character status (Alive, Dead, or Unknown)
- `image`: Character image URL

## Files

### Single Character Query Files

- `character-id-1.graphql` - Query for character with ID 1 (Rick Sanchez)
- `character-id-2.graphql` - Query for character with ID 2 (Morty Smith)
- `character-id-3.graphql` - Query for character with ID 3 (Summer Smith)
- `character-id-4.graphql` - Query for character with ID 4 (Beth Smith)

### Single Character Output Files

- `character-id-1-output.json` - Response data for character 1
- `character-id-2-output.json` - Response data for character 2
- `character-id-3-output.json` - Response data for character 3
- `character-id-4-output.json` - Response data for character 4

### Paginated Character Query Files

- `characters-page-1.graphql` - Query for characters page 1 (IDs 1-20)
- `characters-page-2.graphql` - Query for characters page 2 (IDs 21-40)
- `characters-page-3.graphql` - Query for characters page 3 (IDs 41-60)
- `characters-page-4.graphql` - Query for characters page 4 (IDs 61-80)

### Paginated Character Output Files

- `characters-page-1-output.json` - Response data for page 1 (20 characters)
- `characters-page-2-output.json` - Response data for page 2 (20 characters)
- `characters-page-3-output.json` - Response data for page 3 (20 characters)
- `characters-page-4-output.json` - Response data for page 4 (20 characters)

## Example Query Structures

### Single Character Query

```graphql
query {
  character(id: 1) {
    id
    name
    status
    species
    type
    gender
  }
}
```

### Paginated Characters Query

```graphql
query {
  characters(page: 1) {
    results {
      id
      name
      status
      image
    }
  }
}
```

## How to Execute Queries

You can execute these queries using:

1. **GraphQL Playground/GraphiQL**: Navigate to https://rickandmortyapi.com/graphql
2. **cURL for Single Character**:

```bash
curl -X POST https://rickandmortyapi.com/graphql \
  -H "Content-Type: application/json" \
  -d '{"query":"query { character(id: 1) { id name status species type gender } }"}'
```

3. **cURL for Paginated Characters**:

```bash
curl -X POST https://rickandmortyapi.com/graphql \
  -H "Content-Type: application/json" \
  -d '{"query":"query { characters(page: 1) { results { id name status image } } }"}'
```

4. **JavaScript/Node.js**: Use libraries like `graphql-request` or `apollo-client`

## Learning Outcomes

This project demonstrates:

- Writing precise GraphQL queries for specific data
- Using arguments (`id`, `page`) to filter and paginate results
- Structuring queries to request only necessary fields
- Understanding the difference between single item queries and paginated list queries
- Working with nested data structures in GraphQL responses

## Repository

- **GitHub repository**: alx-graphql-0x00
- **Directory**: character
