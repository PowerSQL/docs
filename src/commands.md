## Commands

- `powersql check`: This will load all your `.sql` files in the directories listed in `models`. It will check the syntax of the SQL statements. After this, it will check the DAG and report if there is a circular dependency. Finally, it will run a type checker and report any type errors.
- `powersql run`: Loads and runs the entire DAG of SQL statements.
- `powersql test`: Loads and runs the data tests. By running `powersql test --fail-fast` powersql will stop at the first failure.
