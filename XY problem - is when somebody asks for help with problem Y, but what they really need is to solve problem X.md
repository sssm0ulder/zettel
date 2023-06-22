example:

```
<n00b> How do I get the echo of the last three characters in a filename?  

<feline> If they are in a variable: echo ${foo: -3}  
<feline> Why 3 characters? What do you REALLY want? <feline>, do you want an extension?

<n00b> Yes.  

<feline> There is no guarantee that all files have three-letter extensions,
<feline> so getting the three-character will not solve the problem. <feline> echo ${foo##*.}
```

url:: [xyproblem.info](https://xyproblem.info/)