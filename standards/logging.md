Logging Standards
===========================

### These standards have not yet been defined.

Areas for discussion include:
* what to log or not
* what each level means
* structured logging - standards around key names

### Potential starting point:

#### All logs should be structured.

JSON by default, though where not practical KV pairs are required. The entire log line should be formatted this way.

* Good: `{"created":"2016-11-21T14:35:48", "event":"this is my log message", "key":"value","another_key":"new value"}`
* OK: `created=2016-11-21T14:35:48, event="this is my log message", key=value, another_key="new value"`
* Bad: `2016-11-21T14:35:48 this is my log message key=value, anotherKey="new value"`
* Also Bad: `2016-11-21T14:35:48.000801Z|DEBUG: service-name: { "created": "2016-11-21T14:35:48", "event":"log message", "level": "debug" }`

Keys should all be snake_case (all in lower case).

#### All log lines should...

... contain some metadata about how the information was generated, standard keys being:
* `created` - UTC timestamp - YYYY-mm-ddTHH:MM:SS.ffffffZ - note it should always be Z never 0 or +1
* `service` - identifier for the application generating the message
* `level` - severity of the event being logged - recommended values are `error`, `warn` and `info`
* `event` - a fixed string ('application started', 'ratelimit exceeded' etc.) which can be graphed. This should be a single phrase, lower cased, without a period.
* `context` - an identifier to group related messages, e.g. the `X-Request-Id` value in all log lines relating to that request
* `data` - nested subdocument containing other details of the event (user id, request details etc.)

#### All http requests should...

... have sight of some basic information: `start` & `end`, `duration` or both, `status` (never *status_code*), `method` and `path`. If you’re confident that your access logs cover these and are prepared to extract this information where needed this is fine, otherwise by logging them out in a structured way you will ensure a record of them.

#### On startup...

... it is recommended that all applications log the `version` being deployed. Preferably the semantic version number for the release, failing that the Git SHA, will allow easy referencing of when versions were live, and provide a link to the contents of that release.

It may be worth considering logging out the hostname (as `host`) on startup if this information is not otherwise captured.

#### Security

Some thought should be given to what details are relevant for your log message. Some metadata about the transaction may be useful for logging, but should avoid logging large json documents or unnecessary data.

**Survey response data, personal details, and passwords should never be logged**
