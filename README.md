# CTF Quick Reference


* [OSINT](https://github.com/tRumiBe/CTF-Reference/blob/main/OSINT.md)
*[Crptyography](https://github.com/tRumiBe/CTF-Reference/blob/main/cryptography.md)
*[Enumeration](https://github.com/tRumiBe/CTF-Reference/blob/main/enumeration.md)
*[Forensic](https://github.com/tRumiBe/CTF-Reference/blob/main/forensics.md)
*[Log Analysis](https://github.com/tRumiBe/CTF-Reference/blob/main/log-analysis.md)
*[Network](https://github.com/tRumiBe/CTF-Reference/blob/main/network.md)
*[Password](https://github.com/tRumiBe/CTF-Reference/blob/main/password.md)
*[Reconnaissance](https://github.com/tRumiBe/CTF-Reference/blob/main/scanning.md)
*[Web App](https://github.com/tRumiBe/CTF-Reference/blob/main/webapp.md)
*[Wireless](https://github.com/tRumiBe/CTF-Reference/blob/main/wireless.md)


### Common OSINT tools

* [WHOIS Lookup Tool](https://lookup.icann.org/en)
* [View Metadata Online](https://www.metadata2go.com/view-metadata)
* [OpenPGP](https://keys.openpgp.org/)
* [OpenPGP Keyserver](https://keyserver.ubuntu.com/)
* [Barcode Reader](https://online-barcode-reader.inliteresearch.com/)
* [Hexed.it](https://hexed.it/?hl=en)
* [CyberChef](https://gchq.github.io/CyberChef/)
* [Epoch Time](https://www.epochconverter.com/seconds-days-since-y0)

### HTTP Header

| Example |Description |
|--|--|
| Referer: http://example.com | Previous web page|
| User-Agent | Client software |
| Accept: text/html | Acceptable Media Types |
| Accept-Charset: utf-8 | Acceptable Character set |


### Common tools and commands

```
strings pineapple.jpg | grep password
```

#### Hashcat

```
hashcat hash.txt -m 0 -a 0 /usr/share/wordlists/rockyou.txt > result.txt
```

- `-m 0` specifies MD5 hashing.
- `-a 0` adictionary ttack mode. 

```
hashcat -m 0 -a 3 ./hash.txt 'PIN-?d?d?d?d'
```

- `-a 3` brute-force atatck mode for masking.
- `PIN-?d?d?d?d` password starts with `PIN-` followed by 4 digits number. 

```
hashcat hash.txt -m 0 -a 6 hash.txt creditcards.txt ?d?d?d?d
```

- `-a 6` hybrid attack mode.
- `?d?d?d?d` credit card number ends with 4 digit numbers. 

#### John

 ```
 john --wordlist=/usr/share/wordlists/rockyou.txt --format=crypt my-hash.txt > result.txt
 ```


### ASCII Table
|65|66|67|68|69|70|71|72|73|74|75|76|77|78|
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
|A|B|C|D|E|F|G|H|I|J|K|L|M|N|

|79|80|81|82|83|84|85|86|87|88|89|90|
|--|--|--|--|--|--|--|--|--|--|--|--|
|O|P|Q|R|S|T|U|V|W|X|Y|Z|

|97|98|99|100|101|102|103|104|105|106|107|108|109|
|--|--|--|--|--|--|--|--|--|--|--|--|--|
|a|b|c|d|e|f|g|h|i|j|k|l|m|n|

|111|112|113|114|115|116|117|118|119|120|121|122|
|--|--|--|--|--|--|--|--|--|--|--|--|
|o|p|q|r|s|t|u|v|w|x|y|z|

[Reference](https://www.cs.cmu.edu/~pattis/15-1XX/common/handouts/ascii.html)