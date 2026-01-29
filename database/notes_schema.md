# Notes table schema (SQLite)

This schema was applied directly to:

`/home/kavia/workspace/code-generation/simple-notes-app-207251-207262/database/myapp.db`

## DDL statements executed (one at a time)

```sql
CREATE TABLE IF NOT EXISTS notes (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  content TEXT NOT NULL,
  created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);
```

```sql
CREATE INDEX IF NOT EXISTS idx_notes_updated_at ON notes(updated_at);
```

## Verification queries

```sql
SELECT name, sql FROM sqlite_master WHERE type='table' AND name='notes';
```

```sql
PRAGMA table_info(notes);
```

```sql
PRAGMA index_list(notes);
```
