# Database Config

You can set up your database in `app/config/database.php`.

Inside of the database configuration file, you'll find a few relevant configurations:

### Default Connection

```php
<?php

return array(
    // more up here
    'default' => 'mysql',
    // more down here
);
```

By default, Wardrobe is setup for a MySQL (`mysql`) database. However, Wardrobe can also work with the other database connections, such as PostgreSQL (`pgsql`), Microsoft SQL Server (`sqlsrv`) and SQL Lite (`sqlite`).

You can change the default connection to any of the above databases you are using.

### Connections

For each connection, enter your database name, username, password and any other settings necessary.

For instance, if the `default` connection is set to `mysql`, fill out the `mysql` section under `connections`:

```php
<?php

return array(
    // more up here

    'default' => 'mysql',

    'connections' => array(

	'sqlite' => array(
		/* removed for brevity */
	),

	'mysql' => array(
		'driver'    => 'mysql',
		'host'      => 'localhost',
		'database'  => 'my_database_name',
		'username'  => 'my_username',
		'password'  => 'my_password',
		'charset'   => 'utf8',
		'collation' => 'utf8_unicode_ci',
		'prefix'    => '',
	),

	'pgsql' => array(
		/* removed for brevity */
	),

	'sqlsrv' => array(
		/* removed for brevity */
	),

    ),
    // more down here
);
```

More information on database configuration can be found in the [Laravel Documentation](http://laravel.com/docs/database#configuration).