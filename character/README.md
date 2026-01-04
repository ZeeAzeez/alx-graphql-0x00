# GraphQL Character Query Project

## Objective

This project demonstrates how to write GraphQL queries to retrieve specific character information using their ID from the Rick and Morty API.

## Endpoint

GraphQL API: `https://rickandmortyapi.com/graphql`

## Task Description

Write GraphQL queries using the `character(id: ID!)` field to fetch details of characters with IDs 1, 2, 3, and 4.

### Fields Retrieved

- `id`: Character ID
- `name`: Character name
- `status`: Character status (Alive, Dead, or Unknown)
- `species`: Character species
- `type`: Character type/subspecies
- `gender`: Character gender

## Files

### GraphQL Query Files

- `character-id-1.graphql` - Query for character with ID 1 (Rick Sanchez)
- `character-id-2.graphql` - Query for character with ID 2 (Morty Smith)
- `character-id-3.graphql` - Query for character with ID 3 (Summer Smith)
- `character-id-4.graphql` - Query for character with ID 4 (Beth Smith)

### Output JSON Files

- `character-id-1-output.json` - Response data for character 1
- `character-id-2-output.json` - Response data for character 2
- `character-id-3-output.json` - Response data for character 3
- `character-id-4-output.json` - Response data for character 4

## Example Query Structure

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

## How to Execute Queries

You can execute these queries using:

1. **GraphQL Playground/GraphiQL**: Navigate to https://rickandmortyapi.com/graphql
2. **cURL**:

```bash
curl -X POST https://rickandmortyapi.com/graphql \
  -H "Content-Type: application/json" \
  -d '{"query":"query { character(id: 1) { id name status species type gender } }"}'
```

3. **JavaScript/Node.js**: Use libraries like `graphql-request` or `apollo-client`

## Repository

- **GitHub repository**: alx-graphql-0x00
- **Directory**: character
