# RegexCheatSheet

**Regex Cheat Sheet**
https://regexr.com/

`
The Fat cat ran down the street.
It was searching for a mouse to eat.
`

## Flags

`/g` - global will allow you to match anywhere in string  eg: cat  `/at/g`

`/i` - case in sensitive. So, it will match lower as well as upper case eg: 'the', 'The'  `/the/gi`


## Selector
`ea?` - so '?'' will make before word makes optional. So 'e' will be matched where as 'a' is optional. eg: e, ea `/ea?/`

`re*` - '*' will match zero or more character so all the word 'r', 'e' or multiple combination eg: reeereere  `/re*/`

`.at` - period match anything with combination '_at' except new line `/.at/g`

`\.` - '\' backslash will match special character. It escapes any special character or wildcard after it. in this example it is selecting '.' period / fullstop ' `/\./g`

`\w` - small 'w' matching every single letter. `/\w/`

`\W` - capital 'W' match any character except letter. `/\W/`

`\s`- matching any space. `/\s/`

`\S` - match everything except whitespace `/\S/`

`\w{4,5}` - get any word '\w' which have {4 or 5} character long. Note: it will only work before rule eg: \w{2,1} works on any letter, t{2,3} only works on letter 't', can use with group selector to group word (f|c){2} gives fat, cat, etc or (t|r){2} or group `/\w{4,5}/` 

`^t` - match 't' at beginning of the line. it only needs multiline flag '/i' inorder to select in multiple line.  `/^t/`

`\s$` - match any 'space' of each end of line. It can be 'word, number'$ eg: (\s|\.)$ match any space or full stop of each end of line. `/\s$/`
## Group Selector
`[fc]at` - [] match anything inside bracket and 'at' will select all the word 'at'. eg fat, [f]at, cat, [c]at, catalyst, [c]at .... `/[fc]at/`

## Capture Grouping (select word and make its own group)
`(t|T)he` - match _he and first letter is either lower or uppercase. eg either select eg: the, The `/(t|T)/`

##Range selector
`[a-z]`- match all the letter starts from a to z or can match the capital letter as well using 'i' flag (case in-sensitive) `/[a-z]/i`

`[A-Z]` - match all the 'uppercase' letter `/[A-Z]/`

`[0-9]` - match all the number starts from 0 to 9 `/[0-9]/`

`[a-zA-Z0-9]` - or match all the small, capital letter or any number 



