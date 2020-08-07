# Installation

PowerSQL is primarily used as a command line tool. The current distribution is via a rust *crate*. For this you need first to install the build tool [Cargo](https://www.rust-lang.org/tools/install):

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Then install PowerSQL like this for BigQuery:


```
cargo install powersql --features bigquery
```

Or install PowerSQL like this for PostgreSQL:

```
cargo install powersql --features postgres
```


