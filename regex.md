
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

one more example
```
pattern: featureFlags\.get\(FeatureFlag\.(\w+)\);
replace on: featureFlags[FeatureFlag.$1];
```
[tags-end]: <>
