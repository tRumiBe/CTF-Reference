### Password Cracking Cheatsheet

#### Windows password
Use Kali ophcrack tool ti crack Windows password. 

#### PDF Password crack using John

1. Use this [online tool](https://hashes.com/en/johntheripper/pdf2john) to get a hash. 
2. `john --wordlist=/usr/share/wordlists/rockyou.txt --format=PDF my-hash.txt > result.txt`
3. OR `john --show my-hash.txt`

#### Kali Shadow file using John

`Bob:$6$3IZbL38p$DthlEy45WxGJ80FgAs5JpCpLbJXTXzFv40UDiIN/2.CcQO39u1uU18822:0:99999:7::3712`

[Shadow password format](https://images.squarespace-cdn.com/content/v1/5a01100f692ebe0459a1859f/1603347459833-GSR76P31T020NK97YV4B/BSY+Security+Class+Diagrams+-+_etc_shadow+%28L%29.jpg)

- Password hash: `$6$3IZbL38p$DthlEy45WxGJ80FgAs5JpCpLbJXTXzFv40UDiIN/2.CcQO39u1uU`

- 3712 days since 01-01-1970. The last update was on 03-01-1980. 
[Epoch time converter](https://www.epochconverter.com/seconds-days-since-y0)

- Salt is between 2nd $ and 3re $.

- hash = digest. Also known as a message digest, digest, or hash value

```
Bob:$6$
3IZbL38p$ <= This is Salt
DthlEy45WxGJ80FgAs5JpCpLbJXTXzFv40UDiIN/2.CcQO39u1uU <= This is hash digest.
:18822:0:99999:7::3712
```

`john --format=crypt shadow.txt`
`john --show --format=crypt shadow.txt`

