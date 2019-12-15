# php-console-pretty-json
```php
<?php

function jdd($data)
{
    $data = is_string($data) ? $data : json_encode($data,JSON_PRETTY_PRINT);
    $dbgt = debug_backtrace();
    echo "\e[42;1;37mJson dump info:\e[0m\n";
    echo "\e[0;33m" . $dbgt[0]['file'] . ':' . $dbgt[0]['line'] . "\e[0m" . PHP_EOL;
    echo "\e[1;36m" . $data . "\e[0m" . PHP_EOL.PHP_EOL;
    die();
}
 
 jdd(['key'=>'value']);
```
#### Output 
![output](https://github.com/tohidplus/php-console-pretty-json/output.jpg)
