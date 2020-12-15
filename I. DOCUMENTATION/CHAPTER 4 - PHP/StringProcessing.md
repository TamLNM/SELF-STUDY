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
## 2. addslashes($string, $char_list)
## 3. bin2hex($str)
## 4. chop($string, $charList)
## 5. crc32($string)
## 6. explode(Sreperator, $string, $limit)
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
