
1. Restart PostgreSQL

    **PG::ConnectionBad**

    Check if the postgresql was running
    `ps aux | grep postgresql`

    Restart it on Ubuntu
    `sudo /etc/init.d/postgresql start`
    
    Restart it on macOS
    `brew services restart postgresql`
    
    or
    
    `pg_ctl -D /usr/local/var/postgres restart` 
    
    [source](https://stackoverflow.com/questions/42344890/how-to-restart-postgresql-on-os-x)

2. Reinstall it
    `brew reinstall posgresql`

3. pg bad connection unix domain
    When you receive a `could not connect to server: No such file or directory Is the server running locally and accepting connections on Unix domain socket "/tmp/.s.PGSQL.5432"?`

    It means that the PGSQL server is running but we still can't properly connect.

    In that case, Check PG status;

    `pg_ctl -D /usr/local/var/postgres status`
    
    Response will be something like:

    ```
    pg_ctl: server is running (PID: 377)
    /usr/local/Cellar/postgresql/12.1/bin/postgres "-D" "/usr/local/var/postgres"
    ```

    Then, let's kill the process by pid:

    `kill 377`

    Source: https://stackoverflow.com/questions/36428145/pgconnection-bad-error
