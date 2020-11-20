# Security

## Passwords

- What is the math to get how long password size must be?

```
ceil( logC (H * Y * 31556926) )
C = charset count
H = adversary hashrate
Y = years to crack
```

Example:

```
C = alphanum charset = 62 chars
H = 100 trillion guesses per second
Y = 100 years
= 14 characters long
```
[Wolfram Alpha](http://wolframalpha.com/input/?i=ceil%28log+base+62+of+%28100000000000000+*+100+*+31556926%29%29)
