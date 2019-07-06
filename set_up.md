### Test that rake is available

Test to see if you have your rake commands by typing: `rake` into terminal.

```
 $ rake
=>
  rake -T: Will list all other rake tasks
  rake serve: Will run Sinatra server
  rake db:setupMCS: Will set up your database
  rake db:create: Will create a database
  rake db:migrate: Will run migrations
  rake db:drop: Will drop the database
  rake db:create_migration: Will create a migration
  rake serve: Will run
```
*If you get a warning about unresolved specs run `bundle clean --force` to cleanup any unneeded gems*

### Test PostgreSQL

Test postgres is working with the password given to you by the instructor.

```
 $ psql -U postgres
 postgres=#

```

Type `\q` to quit postgres.

### Connect your app to the database

Open your **text editor** and add the database username and password given to you by the instructor to the database.yml file.

Re-open your command shell to finish setting up postgres.

```
  $ rake db:setupMCS
```

###For irb (interactive ruby)

Use either the Windows command prompt or a shell such as Git Bash to check that you can connect to your database using `irb`.

* Using the Windows command prompt (not a shell) type `irb`.
* Using the shell on Windows first set an alias to irb by typing in: `alias irb='winpty "$(which irb).cmd"'` and then typing in `irb`. If you close your shell you will need to re-add the alias on a public computer. (If you are on a private computer, add your alias to your (.bash_profile file)[http://kurtdowswell.com/software-development/git-bash-aliases/].)

```
 $ irb
2.3.1 :002 > require './app.rb'
 => true
2.3.1 :007 > exit
```