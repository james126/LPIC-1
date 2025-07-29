# Regex rules

Match patterns in text

|                           | example        | matches |
| ------------------------- | -------------- | ------- |
| string                    | *hello*        | hello   |
| `\|` multiple string      | *hello\|hi*    | hello hi |
| `[]`                      | *b[aeiou]g*    | big     |
| `[-]` range               | *a(2-4)z*      | a2z     |
| `.` any character         | *a.z*          | aQz     |
| `^` start of line         |                |         |
| `$` end of line           |                |         |
| **repetition**            |                |         |
| `*` 0+                    |                |         |
| `+` 1+                    |                |         |
| `+?` 0 or 1               |                |         |
| `()` groups part of regex |                |         |
| `\` escape                | *example\.com* | example.com |

