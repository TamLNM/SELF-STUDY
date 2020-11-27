# PHP

## I. Encode/ Decode
- Decode: convert a JSON string into a PHP Object
```PHP
<?php
$jsonobj = '{"Peter":35,"Ben":37,"Joe":43}';

var_dump(json_decode($jsonobj));
?>
```
