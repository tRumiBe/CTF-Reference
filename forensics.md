## Forensics

### Magic Number & File Types

`file mycats.jpg` Find file types
`binwalk mycats.jpg` Identify embeded files. 
`binwalk -dd='.*' mycats.jpg`List all embeded files. 


Common file signature
| File Signature | File types |
| -- | -- |
|`FF D8 FF E0 00 10 4A 46 49 46 00 01` | .jpeg |
| `89 50 4E 47 0D 0A 1A 0A` | .png |
| `25 50 44 46 2D` | PDF |


[List of file signatures by Wiki](https://en.wikipedia.org/wiki/List_of_file_signatures)