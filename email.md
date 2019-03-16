# RegEx email

```js
/^((?!\.)[a-z0-9-_.]*[^.])(@\w+)\.(\w{2,}[^.\W])$/gim;
```

### Explanation:

There are 3 groups

> (firstString)(@-followedByString)\[dot\](groupOfTwoOrMoreChars)

-First Group

The String got to start without a dot or any other special character. The string could be a letter,number,underscore,dot,dash

-Second Group

The second group starts with an @ and would be followed by any type of word until it finds the dot before the third group

-Third Group

The last group follows the dot and it would be any type of word but cant finish as a dot or any other special character
