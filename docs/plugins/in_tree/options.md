# Available configuration options

## [DEFAULT]

```
# If set to true, the logging level will be set to DEBUG instead of the
# default INFO level.
# (boolean value)
#debug = False
```

```
# List of package logging levels in logger=LEVEL pairs. This option is
# ignored if log_config_append is set.
# (list value)
#default_log_levels = [u'amqp=WARN', u'amqplib=WARN', u'boto=WARN', u'qpid=WARN', u'sqlalchemy=WARN', u'suds=INFO', u'oslo.messaging=INFO', u'oslo_messaging=INFO', u'iso8601=WARN', u'requests.packages.urllib3.connectionpool=WARN', u'urllib3.connectionpool=WARN', u'websocket=WARN', u'requests.packages.urllib3.util.retry=WARN', u'urllib3.util.retry=WARN', u'keystonemiddleware=WARN', u'routes.middleware=WARN', u'stevedore=WARN', u'taskflow=WARN', u'keystoneauth=WARN', u'oslo.cache=INFO', u'dogpile.core.dogpile=INFO']
```

```
# Enables or disables fatal status of deprecations.
# (boolean value)
#fatal_deprecations = False
```

```
# The format for an instance that is passed with the log message.
# (string value)
#instance_format = '[instance: %(uuid)s] '
```

```
# The format for an instance UUID that is passed with the log message.
# (string value)
#instance_uuid_format = '[instance: %(uuid)s] '
```

```
# The name of a logging configuration file. This file is appended to any
# existing logging configuration files. For details about logging
# configuration files, see the Python logging module documentation. Note
# that when logging configuration files are used then all logging
# configuration is set in the configuration file and other logging
# configuration options are ignored (for example,
# logging_context_format_string).
# (string value)
# Deprecated group/name - DEFAULT/log-config
# Deprecated group/name - DEFAULT/log_config
#log-config-append = <None>
```

```
# Defines the format string for %%(asctime)s in log records. Default:
# %(default)s . This option is ignored if log_config_append is set.
# (string value)
#log-date-format = '%Y-%m-%d %H:%M:%S'
```

```
# (Optional) The base directory used for relative log_file  paths. This
# option is ignored if log_config_append is set.
# (string value)
# Deprecated group/name - DEFAULT/logdir
#log-dir = <None>
```

```
# (Optional) Name of log file to send logging output to. If no default
# is set, logging will go to stderr as defined by use_stderr. This
# option is ignored if log_config_append is set.
# (string value)
# Deprecated group/name - DEFAULT/logfile
#log-file = <None>
```

```
# Format string to use for log messages with context.
# (string value)
#logging_context_format_string = '%(asctime)s.%(msecs)03d %(process)d %(levelname)s %(name)s [%(request_id)s %(user_identity)s] %(instance)s%(message)s'
```

```
# Additional data to append to log message when logging level for the
# message is DEBUG.
# (string value)
#logging_debug_format_suffix = '%(funcName)s %(pathname)s:%(lineno)d'
```

```
# Format string to use for log messages when context is undefined.
# (string value)
#logging_default_format_string = '%(asctime)s.%(msecs)03d %(process)d %(levelname)s %(name)s [-] %(instance)s%(message)s'
```

```
# Prefix each line of exception output with this format.
# (string value)
#logging_exception_prefix = '%(asctime)s.%(msecs)03d %(process)d ERROR %(name)s %(instance)s'
```

```
# Defines the format string for %(user_identity)s that is used in
# logging_context_format_string.
# (string value)
#logging_user_identity_format = '%(user)s %(tenant)s %(domain)s %(user_domain)s %(project_domain)s'
```

```
# HTTP timeout for any of OpenStack service in seconds
# (floating point value)
#openstack_client_http_timeout = 180.0
```

```
# Enables or disables publication of error events.
# (boolean value)
#publish_errors = False
```

```
# Print debugging output only for Rally. Off-site components stay quiet.
# (boolean value)
#rally-debug = False
```

```
# Maximum number of logged messages per rate_limit_interval.
# (integer value)
#rate_limit_burst = <None>
```

```
# Log level name used by rate limiting: CRITICAL, ERROR, INFO, WARNING,
# DEBUG or empty string. Logs with level greater or equal to
# rate_limit_except_level are not filtered. An empty string means that
# all levels are filtered.
# (string value)
#rate_limit_except_level = 'CRITICAL'
```

```
# Interval, number of seconds, of log rate limiting.
# (integer value)
#rate_limit_interval = <None>
```

```
# Size of raw result chunk in iterations
# (integer value)
#raw_result_chunk_size = 1000
```

```
# Syslog facility to receive log lines. This option is ignored if
# log_config_append is set.
# (string value)
#syslog-log-facility = 'LOG_USER'
```

```
# Enable journald for logging. If running in a systemd environment you
# may wish to enable journal support. Doing so will use the journal
# native protocol which includes structured metadata in addition to log
# messages.This option is ignored if log_config_append is set.
# (boolean value)
#use-journal = False
```

```
# Use JSON formatting for logging. This option is ignored if
# log_config_append is set.
# (boolean value)
#use-json = False
```

```
# Use syslog for logging. Existing syslog format is DEPRECATED and will
# be changed later to honor RFC5424. This option is ignored if
# log_config_append is set.
# (boolean value)
#use-syslog = False
```

```
# Log output to standard error. This option is ignored if
# log_config_append is set.
# (boolean value)
#use_stderr = False
```

```
# Uses logging handler designed to watch file system. When log file is
# moved or removed this handler will open a new log file with specified
# path instantaneously. It makes sense only if log_file option is
# specified and Linux platform is used. This option is ignored if
# log_config_append is set.
# (boolean value)
#watch-log-file = False
```

## [database]

```
# The back end to use for the database.
# (string value)
# Deprecated group/name - DEFAULT/db_backend
#backend = 'sqlalchemy'
```

```
# The SQLAlchemy connection string to use to connect to the database.
# (string value)
# Deprecated group/name - DEFAULT/sql_connection
# Deprecated group/name - DATABASE/sql_connection
# Deprecated group/name - sql/connection
#connection = <None>
```

```
# Verbosity of SQL debugging information: 0=None, 100=Everything.
# (integer value)
# Deprecated group/name - DEFAULT/sql_connection_debug
#connection_debug = <None>
```

```
# Optional URL parameters to append onto the connection URL at connect
# time; specify as param1=value1&param2=value2&...
# (string value)
#connection_parameters = <None>
```

```
# Connections which have been present in the connection pool longer than
# this number of seconds will be replaced with a new one the next time
# they are checked out from the pool.
# (integer value)
# Deprecated group/name - DATABASE/idle_timeout
# Deprecated group/name - database/idle_timeout
# Deprecated group/name - DEFAULT/sql_idle_timeout
# Deprecated group/name - DATABASE/sql_idle_timeout
# Deprecated group/name - sql/idle_timeout
#connection_recycle_time = 3600
```

```
# Add Python stack traces to SQL as comment strings.
# (boolean value)
# Deprecated group/name - DEFAULT/sql_connection_trace
#connection_trace = False
```

```
# If True, increases the interval between retries of a database
# operation up to db_max_retry_interval.
# (boolean value)
#db_inc_retry_interval = True
```

```
# Maximum retries in case of connection error or deadlock error before
# error is raised. Set to -1 to specify an infinite retry count.
# (integer value)
#db_max_retries = 20
```

```
# If db_inc_retry_interval is set, the maximum seconds between retries
# of a database operation.
# (integer value)
#db_max_retry_interval = 10
```

```
# Seconds between retries of a database transaction.
# (integer value)
#db_retry_interval = 1
```

```
# If set, use this value for max_overflow with SQLAlchemy.
# (integer value)
# Deprecated group/name - DEFAULT/sql_max_overflow
# Deprecated group/name - DATABASE/sqlalchemy_max_overflow
#max_overflow = 50
```

```
# Maximum number of SQL connections to keep open in a pool. Setting a
# value of 0 indicates no limit.
# (integer value)
# Deprecated group/name - DEFAULT/sql_max_pool_size
# Deprecated group/name - DATABASE/sql_max_pool_size
#max_pool_size = 5
```

```
# Maximum number of database connection retries during startup. Set to
# -1 to specify an infinite retry count.
# (integer value)
# Deprecated group/name - DEFAULT/sql_max_retries
# Deprecated group/name - DATABASE/sql_max_retries
#max_retries = 10
```

```
# Minimum number of SQL connections to keep open in a pool.
# (integer value)
# Deprecated group/name - DEFAULT/sql_min_pool_size
# Deprecated group/name - DATABASE/sql_min_pool_size
#min_pool_size = 1
```

```
# If True, transparently enables support for handling MySQL Cluster
# (NDB).
# (boolean value)
#mysql_enable_ndb = False
```

```
# The SQL mode to be used for MySQL sessions. This option, including the
# default, overrides any server-set SQL mode. To use whatever SQL mode
# is set by the server configuration, set this to no value. Example:
# mysql_sql_mode=
# (string value)
#mysql_sql_mode = 'TRADITIONAL'
```

```
# If set, use this value for pool_timeout with SQLAlchemy.
# (integer value)
# Deprecated group/name - DATABASE/sqlalchemy_pool_timeout
#pool_timeout = <None>
```

```
# Interval between retries of opening a SQL connection.
# (integer value)
# Deprecated group/name - DEFAULT/sql_retry_interval
# Deprecated group/name - DATABASE/reconnect_interval
#retry_interval = 10
```

```
# The SQLAlchemy connection string to use to connect to the slave
# database.
# (string value)
#slave_connection = <None>
```

```
# If True, SQLite uses synchronous mode.
# (boolean value)
# Deprecated group/name - DEFAULT/sqlite_synchronous
#sqlite_synchronous = True
```

```
# Enable the experimental use of database reconnect on connection lost.
# (boolean value)
#use_db_reconnect = False
```