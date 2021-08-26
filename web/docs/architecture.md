---
id: architecture
title: Architecture
description: 'Supabase design and architecture'
# hide_table_of_contents: true
---


Supabase is open source. Wherever possible, we use and support existing tools rather than developing from scratch. 
We choose open source tools which are scalable and we make them simple to use.

![Supabase Architecture](/img/supabase-architecture.png)

- [PostgreSQL](https://www.postgresql.org/) is an object-relational database system with over 30 years of active development that has earned it a strong reputation for reliability, feature robustness, and performance.
- [Realtime](https://github.com/supabase/realtime) is an Elixir server that allows you to listen to PostgreSQL inserts, updates, and deletes using WebSockets. Supabase listens to Postgres' built-in replication functionality, converts the replication byte stream into JSON, then broadcasts the JSON over WebSockets.
- [PostgREST](http://postgrest.org/) is a web server that turns your PostgreSQL database directly into a RESTful API.
- [postgres-meta](https://github.com/supabase/postgres-meta) is a RESTful API for managing your Postgres, allowing you to fetch tables, add roles, and run queries etc.
- [GoTrue](https://github.com/netlify/gotrue) is an SWT-based API for managing users and issuing SWT tokens.
- [Kong](https://github.com/Kong/kong) is a cloud-native API gateway.

Supabase is not a 1-to-1 mapping of Firebase. While we are building many of the features that Firebase offers, we are not going about it the same way.

Our technological choices are quite different to Firebase. Everything we use is open source. Wherever possible, we use and support existing tools in the ecosystem, rather than developing from scratch.

Most notably, we use Postgres rather than a NoSQL store. This was a deliberate choice. We believe that no other database on the market offers the scalability and functionality required to legitimately compete with Firebase.
