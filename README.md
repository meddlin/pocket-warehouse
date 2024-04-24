# pocket-warehouse

It's like a data warehouse in your pocket 📦

Not quite a full "data warehouse", but it'll feel like one. This project is meant
to solve a problem while juggling a tedious amount of `.xlsx`/`.csv` files, and 
I needed to perform light data analysis across them. 

Often, exploring or answering simple business inqueries about the data I had 
at-hand would be made easier if I could only use SQL somehow. But this meant 
tediously running a local database, or worse, requesting resources/infrastructure 
as if we aren't already working on enough.

Finally, tucking all of this away in a CLI interface seems the most efficient way
to tuck this away in my day-job workflows.

## Goal

Run a "data warehouse"-like utility from a CLI-interface (with some web goodies).

- spin up/down
- submit queries
- manage stored data

## Notes

Other pieces...These are the pieces that remain to be implemented to provide
the complete system.

### ??? - CSV to Table load mechanism

Automates CSVs to SQL tables...

Need some type of utility to: a) point at a CSV file, b) detect schema, c) create
a table, and d) load the data. The more automated this is, with options to provide
some custom import settings, the better.

*This would be custom development.*

> Note: This could be a place to start - [https://github.com/ThomasDebrunner/csv2sql](https://github.com/ThomasDebrunner/csv2sql)


### usql - A universal CLI for SQL databases

repo: [https://github.com/xo/usql](https://github.com/xo/usql)

This would be the interface for the main database of the system


### pgsync - Middleware to synchronize Postgres to Elastic

repo: [https://github.com/toluaina/pgsync](https://github.com/toluaina/pgsync)

This will provide a continuous synchronization of our Postgres data (or
possibly other RDBMS?) to Elastic. One major downside to this implementation
is needing to configure mapping schemas ahead of time.


### (optional) Web-based management interface

Sure, most of these tools have CLI interfaces already built into them, and the main 
pieces are implemented via a `docker-compose.yml` file...*But a web interface would 
be really slick*.

Central "webpage" to:

- view all tables
- modify any config files for the project
- start/stop services