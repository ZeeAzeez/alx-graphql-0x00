# GraphQL Episode Query Project

## Objective

This project demonstrates how to write GraphQL queries to retrieve specific episode information using their ID from the Rick and Morty API.

## Endpoint

GraphQL API: `https://rickandmortyapi.com/graphql`

## Task Description

Write GraphQL queries using the `episode(id: ID!)` field to fetch details of episodes with IDs 1, 2, 3, and 4.

### Fields Retrieved

- `id`: Episode ID
- `name`: Episode name/title
- `air_date`: Original air date of the episode
- `episode`: Episode code (e.g., S01E01 for Season 1 Episode 1)

## Files

### GraphQL Query Files

- `episode-id-1.graphql` - Query for episode with ID 1 (Pilot)
- `episode-id-2.graphql` - Query for episode with ID 2 (Lawnmower Dog)
- `episode-id-3.graphql` - Query for episode with ID 3 (Anatomy Park)
- `episode-id-4.graphql` - Query for episode with ID 4 (M. Night Shaym-Aliens!)

### Output JSON Files

- `episode-id-1-output.json` - Response data for episode 1
- `episode-id-2-output.json` - Response data for episode 2
- `episode-id-3-output.json` - Response data for episode 3
- `episode-id-4-output.json` - Response data for episode 4

## Example Query Structure

```graphql
query {
  episode(id: 1) {
    id
    name
    air_date
    episode
  }
}
```

## Example Response

```json
{
  "data": {
    "episode": {
      "id": "1",
      "name": "Pilot",
      "air_date": "December 2, 2013",
      "episode": "S01E01"
    }
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
  -d '{"query":"query { episode(id: 1) { id name air_date episode } }"}'
```

3. **JavaScript/Node.js**: Use libraries like `graphql-request` or `apollo-client`

## Learning Outcomes

This project demonstrates:
- Writing precise GraphQL queries for specific data
- Using arguments (`id`) to fetch individual items
- Structuring queries to request only necessary fields
- Understanding the structure of GraphQL responses
- Working with episode data including air dates and episode codes

## Repository

- **GitHub repository**: alx-graphql-0x00
- **Directory**: episode
