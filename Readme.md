# google_analytics

Google Analytics data integration in Go — fetch and process analytics reports via the GA Reporting API.

## What It Does

Connects to the Google Analytics Reporting API v4 and fetches session, page view, and geo-location data. Processes the response and stores structured results into a database for downstream consumption or dashboarding.

## Features

- Fetches Google Analytics reports via the GA Reporting API
- Processes and normalizes response data (sessions, pageviews, geo data)
- Stores data into a database using Go
- Dockerized setup with `docker-compose`
- Makefile for common operations

## Tech Stack

| Layer | Tech |
|---|---|
| Language | Go |
| API | Google Analytics Reporting API v4 |
| Database | (configured via `db.go`) |
| Infrastructure | Docker, docker-compose |
| JS Layer | Node.js (`js/` directory) |

## Project Structure

```
google_analytics/
├── cmd/                  # Entry points / CLI commands
├── js/                   # JavaScript utilities
├── migrations/           # Database migrations
├── db.go                 # Database connection and queries
├── geo.go                # Geo-location data processing
├── docker-compose.yml    # Docker setup
├── Makefile              # Build and run commands
└── Readme.md
```

## Getting Started

### Prerequisites

- Go 1.18+
- Docker & docker-compose
- Google Analytics service account credentials (JSON key file)

### Run with Docker

```bash
docker-compose up --build
```

### Run locally

```bash
make run
```

### Environment

Set your Google Analytics credentials and view ID in your environment or config before running.

## License

MIT
