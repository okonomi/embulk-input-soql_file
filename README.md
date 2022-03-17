# Soql input plugin for Embulk

TODO: Write short description here and embulk-input-soql.gemspec file.

## Overview

* **Plugin type**: input
* **Resume supported**: yes
* **Cleanup supported**: no
* **Guess supported**: yes

WIP

## Configuration

WIP

* **include_deleted_or_archived_records**: if true, include deleted or archived records (boolean, default: false)

## Example

```yaml
in:
  type: soql_file
  username: sample@example.com
  password: password
  security_token: ***
  client_id: ***
  client_secret: ***
  auth_end_point: https://sample.salesforce.com/services/Soap/u/
  api_version: 41.0
  soql: SELECT Id, Name, LastModifiedDate FROM Account WHERE LastModifiedDate > 2019-08-19T00:41:38Z ORDER BY Id
  object: Account
  include_deleted_or_archived_records: true
  parser:
    charset: UTF-8
    newline: CRLF
    type: csv
    delimiter: ','
    columns:
      - {name: Id, type: string, index: 0}
      - {name: Name, type: string, index: 1}
      - {name: LastModifiedDate, type: timestamp, format: '%Y-%m-%dT%H:%M:%S.%L%z', index: 2}
```


## Build

WIP