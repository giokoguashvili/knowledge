# PostgreSQL

- VACUUM
- Bloat
- MVCC2PT

# psql
```
psql -h localhost -p 5435 -U postgres
```

- hot standby - replica that accepts reads from clients
- warm standby - processes changes from the leader but doesn’t process any queries from clients

log sequence number