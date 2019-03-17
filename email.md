# RegEx email

```js
/^((?!\.)[\w-_.]*[^.])(@\w+)(\.\w+(\.\w+)?[^.\W])$/gim;
```

Just playing with Reg Ex. This to validate emails in following ways

- The email couldn't start or finish with a dot
- The email shouldn't contain spaces into the string
- The email shouldn't contain special chars (<:, \*,ecc)
- The email could contain dots in the middle of mail address before the @
- The email could contain a double doman ( '.de.org' or similar rarity)

## Groups

There was created 3 groups into this validations that could be used for custom purposes or replacements

> mailname@domain.com

- First group takes the first string with the name of email \$1 => (mailname)
- Second group takes the @ plus the domain: \$2 => (@domain)
- Third group takes the last part after the domain : \$3 => (.com)

### Explanation:

These 3 groups

> (firstString)(@-followedByString)\[dot\](groupOfTwoOrMoreChars)

-First Group

The String got to start without a dot or any other special character. The string could be a letter,number,underscore,dot,dash

-Second Group

The second group starts with an @ and would be followed by any type of word until it finds the dot before the third group

-Third Group

The last group follows the dot and it would be any type of word but cant finish as a dot or any other special character
