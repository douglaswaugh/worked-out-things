# Work out how to do groups in Visual Studio regex find and replace

## Substituting using group index

1. Surround the group(s) you want to target in parentheses
```
([A-Za-z0-9])+\.separating-text\.([A-Za-z0-9])
```

2. Use index to substitute group
```
$1.$2
```

## Substituing using named groups

1. Surround the group(s) you want to substitute in parentheses and include a named
```
(?<group1>[A-Za-z0-9])+\.separating-text\.(?<group2>[A-Za-z0-9])
```

2. Use the name to substitute group
```
$group1.$group2
```

## More information on substitutions in regular expressions

Can be found on [msdn](https://msdn.microsoft.com/en-us/library/ewy2t5e0.aspx)