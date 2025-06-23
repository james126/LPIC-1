> | type            | string                         | description                                       |
> |-----------------|--------------------------------|---------------------------------------------------|
> | string          | ```Hello```                    | matches Hello                                     |
> | brackets        | ```b[aeiou]g```                | matches big, beg, bog, bug                        |
> | range           | ```a(2-4)z```                  | matches a2z, a3z, ..                              |
> | any character   | ```a.z```                      | matches a2z, aQz, ..                              |
> | start line      | ```^```                        |                                                   |
> | end line        | ```$```                        |                                                   |
> | repetition      | ```*``` <br> ```+``` <br> ```?``` | * &nbsp; 0+ <br> + &nbsp; 1+ <br> ? &nbsp; 0 or 1 |
> | multiple string | ```Hello\|Hi```                | matches either                                    |
> | escaping        | ```example\.com```             | matching a special character                      |
