# bibref-python

This Python wrapper allows programmatic interface for the
[bibref](https://github.com/kovzol/bibref) command-line tool to work
with biblical references.

## Installation

`pip install bibref-python`

## Example usages

### Search for connections of Psalm 2

```python
from bibref.tools import *

print(getrefs_maxlength("SBLGNT LXX Psalms 2"))

text1("υιος μου ει συ εγω σημερον γεγεννηκα σε")
print(find1("LXX"))
print(find1("StatResGNT"))
```

### Search for names appearing in the beginning of Matthew 1

```python
from bibref.tools import *

names = [ "Αβρααμ", "Ισαακ", "Ιακωβ", "Ιουδα",
    "Φαρες", "Ζαρα", "Εσρωμ", "Αραμ", "Αμιναδαβ", "Ναασσων",
    "Σαλμων", "Βοες", "Ραχαβ", "Ιωβηδ", "Ρουθ", "Ιεσσαι", "Δαυιδ",
    "Σολομων", "Ροβοαμ", "Αβια", "Ασαφ", "Ιωσαφατ", "Ιωραμ", "Οζιας",
    "Ιωαθαμ", "Αχαζ", "Εζεκιας", "Μανασση", "Αμως", "Ιωσιας",
    "Ιεχονιας", "Σαλαθιηλ", "Ζοροβαβελ", "Αβιουδ", "Ελιακειμ", "Αζωρ",
    "Σαδωκ", "Αχειμ", "Ελιουδ", "Ελεαζαρ", "Ματθαν", "Ιακωβ", "Ιωσηφ" ]

maxresults(10000)

for name in names:
    text1(name)
    occurrences = find1("LXX")
    print(name, len(occurrences))
```

## Author and copyright

See [license](LICENSE).
