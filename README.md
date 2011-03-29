githtory

Store your shell history in git. forever.

Shell history is generally stored in a simple flat file, loaded into memory
whenever the shell is started, and pruned over time.

By storing history in git, we can:

- store more context for each entry, such as the current directory and
  environment
- support more complex queries, such as asking for all commands which were run
  from the current directory
- store things forever, because the database doesn't all need to be loaded into
  memory
- share history across multiple systems
- more

Basic usage:

* gh init
  start tracking history
* gh
  view history
* gh ready <id>
  copy <id> to recent history, so you can get back to it easily with your
  shell's normal history commands
* gh -N
  view last N lines of history
* gh forget-session
  remove the current session
* gh delete <id>
  forget history at <id>
* gh delete <id>..<id2>
  forget all history reachable from <id2> but not <id>
