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