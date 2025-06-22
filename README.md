# CineSeek: Movie Database API Overview

## API Overview

The MoviesDatabase API provides access to a comprehensive dataset of movie titles, images, release years, and genres. It allows filtering by genre, year, and pagination for effective browsing.

## Version

v2

## Available Endpoints

- `GET /titles` — Fetches movie titles with optional filtering
- `GET /titles/{id}` — Get details for a single movie
- `GET /genres` — Returns list of available genres
- `GET /languages` — Returns list of available languages

## Request and Response Format

### Sample Request

```bash
POST /titles
Headers:
  - x-rapidapi-host: moviesdatabase.p.rapidapi.com
  - x-rapidapi-key: <API_KEY>
Sample Response:
```

```json
{
  "results": [
    {
      "id": "tt123456",
      "titleText": { "text": "Inception" },
      "releaseYear": { "year": 2010 },
      "primaryImage": { "url": "https://..." }
    }
  ]
}
```

## Authentication

You need a RapidAPI key.

```ts
Required header: x-rapidapi-key
```

Must be passed with every request

## Error Handling

401 Unauthorized – Missing/invalid API key
429 Too Many Requests – Rate limit exceeded
500 Server Error – Something’s broken, not your fault

## Usage Limits and Best Practices

Limited to 500 requests/month on free tie
Use pagination (page param)
Cache frequent requests if possible

---
