# PostgreSQL

To get started with PostgreSQL, simply create a new project in a file called `powersql.toml`:

~~~
[project]
name = "my_project"
models = ["models"]
tests = ["tests]
~~~

Now create one or more models in the `models` directory:

~~~sql
CREATE VIEW my_model AS SELECT id, category from my_source;
CREATE TABLE category_stats AS SELECT COUNT(*) category_count FROM my_model GROUP BY category;
~~~

PowerSQL automatically will create a DAG based on the relations in your database.

To run against the database, provide the following environment variables:

- PG\_HOSTNAME
- PG\_USERNAME
- PG\_PORT
- PG\_DATABASE
- PG\_PASSWORD
