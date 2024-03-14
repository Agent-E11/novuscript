# Unicode Areas
If possible, I would like the Font to not conflict with [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts)

The total available space in the Unicode `PUA` is:

| Range             | Slots  | Name                                       |
| ----------------- | ------ | ------------------------------------------ |
| `e000 - f8ff`     | 6,399  | Private Use Area (`PUA`)                   |
| `f0000 - fffff`   | 65,535 | Supplementary Private Use Area-A (`PUA-A`) |
| `100000 - 10ffff` | 65,535 | Supplementary Private Use Area-B (`PUA-B`) |
In total, that is 137,469 available slots

Nerd Fonts uses ([source](https://github.com/ryanoasis/nerd-fonts/wiki/Glyph-Sets-and-Code-Points#overview)) (these are rough estimates, I think my math is off on the totals):
```
Outside PUA
23fb - 23fe
2665
26a1
2b58

Inside PUA
e000 - e00a (11)
e0a0 - e0a2 (3)
e0a3 (1)
e0b0 - e0b3 (4)
e0b4 - e0c8 (15)
e0ca (1)
e0cc - e0d4 (9)
e200 - e2a9 (170)
e300 - e3e3 (228)
e5fa - e6b1 (184)
e700 - e7c5 (198)
ea60 - ebeb (395)

f000 - f2e0 (736)
f300 - f372 (114)
f400 - f532 (307)
f500 - fd46 (2118)

f0001 - f1af0 (6896)

Total = ~(11 + 3 + 1 + 4 + 15 + 1 + 9 + 170 + 228 + 184 + 198 + 395 + 736 + 114 + 307 + 2118 + 6896) = ~11390
```

Based off of this data, it looks like most of `PUA-A` is open, and all of `PUA-B`.

# General Layout of Symbols
I would like the general layout to be:
- Uppercase
	- Vowels
	- Consonants
- Lowercase
	- Vowels
	- Consonants
- Numbers
- Special characters
Where consonants are paired up based on sound, voiced and voiceless next to each other (e.g. p b, f v)