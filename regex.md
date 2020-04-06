
[tags]: <> (regexp, exclude)
```
process.env.(?!LOGIN|PASSWD)
```
[tags-end]: <>


[tags]: <> (reg, regexp, replace)
replace with substitution
```
find by pattern: 
(\w+)\.ts

replace on:
import $1 from '@mw/core/src/schemas/mw/$1';
```
[tags-end]: <>
