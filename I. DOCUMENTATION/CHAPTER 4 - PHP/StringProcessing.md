# FUNCTION FOR STRING PROCESSING

# I. Rules of string processing:
(1) Process " or ' that the website/program can print the string without connecting strings.
(2) With the string between "/'. For printing string include character "/', you need to add character \ before it.
For examples
```PHP
echo "He said \"Hello\"";
echo 'She said \'Hello. How are you?\'';
```

# II. Usual functions in string processing:
## 1. addcslashes($string, $char_list)
⇒ Add \ before string in $char_list

Examples:
```PHP
  echo addcslashes("Le Nguyen Minh Tam", "e");
  // L\e Nguy\en Minh Tam
  echo addcslashes("Le Nguyen Minh Tam", "a..z");
  // L\e N\g\u\y\e\n M\i\n\h T\a\m
```
## 2. addslashes($string)
⇒ Add \ before characters: ', "", \ in $string (if exist)
Example:
```PHP
  echo addcslashes("Le Nguyen Minh Tam", "e");
  // L\e Nguy\en Minh Tam
```

## 3. bin2hex($str)
⇒ Convert string to ACII HEX code
Example:
```PHP
echo bin2hex("Le Nguyen Minh Tam");
// 4c65204e677579656e204d696e682054616d
```

## 4. chop($string, $charList)
⇒ Delete the ending character if it's similar to $charList
Example:
```PHP
echo chop("Le Nguyen Minh Tam", "Tam");
// Le Nguyen Minh
```

## 5. crc32($string) 
⇒ Convert a string to integer number
Example:
```PHP
echo crc32("Le Nguyen Minh Tam");
// 1586453036
```

## 6. explode($seperator, $string, $limit)
⇒ Seperate string to multiple child string by character $seperator with maximun $limit (optional) element.
Example:
```PHP
echo explode("e", "Le Nguyen Minh Tam");
// array(3) { [0]=> string(1) "L" [1]=> string(5) " Nguy" [2]=> string(10) "n Minh Tam" }

echo explode("e", "Le Nguyen Minh Tam", 2);
// array(2) { [0]=> string(1) "L" [1]=> string(16) " Nguyen Minh Tam" }
```

## 7. implode($seperator, $array)
## 8. strlen($string)
## 9. str_word_count($string)
## 10. str_repeat($string, $repeat)
## 11. str_replace($find, $replace, $string)
## 12. md5($string)
## 13. sha1($string)
## 14. htmlentities($string), htmlspecialchars($string)
## 15. strip_tags($string, $allow)
## 16. substr($string, $start_pos, $length)
## 17. strolower($string)
## 18. strtoupper
## 19. ucword($string)
## 20. ucfirst($string)
## 21. trim($string, $charList)
## 22. ltrim($string, $charList)
## 23. rtrim($string, $charList)
