# RSS Aggregator

## Rss aggregator written in Go with all the essential back-end logic.

### Features:

- PostgreSQL (SQLC & Goose for working with raw SQL);
- Authetification;
- Goroutines for fetching multiple feeds at the same time.

### Build and Run

```
cd rss_aggregator && go build && ./rss_aggregator
```

#### Tip for running migration

`cd` into the `sql/schema` directory and run:
```
goose postgres CONN up
```
Where `CONN` is the connection string for your database.
```
postgres://jampetz:@localhost:4321/rssagg
```
The format is:
```
protocol://username:password@host:port/database
```