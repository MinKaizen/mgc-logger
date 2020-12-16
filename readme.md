# MGC Logger

## Description

Simple class for creating logs in wordpress

## Quickstart

```php
use \MGC\Logger\Logger;

$logger = new Logger( 'my-subdirectory', 'sales.log' );
$logger->log( 'Test log message' );
$logger->log( 'Another message' );
```

Output:
```php
# in {path to uploads folder}/my-subdirectory

2020-01-01 12:30: Test log message
2020-01-01 12:30: Another message

```

## Debugging

Use get_test_log() to print debug information:
```php
use \MGC\Logger\Logger;

$logger = new Logger( 'my-subdirectory', 'sales.log' );
print_r( $logger->get_test_log( 'Test log message' ) );
```

Output:
```
Array()
  [log_directory] => "{path to uploads folder}/my-subdirectory"
  [log_directory_exists] => true,
  [log_file] => "{path to uploads folder}/my-subdirectory/sales.log"
  [log_file_exists] => false,
  [base_message] => "Test log message",
  [tags] => Array(),
  [final_message] => "2020-01-01 12:30: Test log message",
```