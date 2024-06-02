# Lexicon

## Lexicon Search
Edit the Dataview query below to list results matching an English gloss.

```dataview
table gloss-eng as English
from "lexicon" and #word 
where contains(gloss-eng,"wo")
```

## Lexical Roots

```dataview
table gloss-eng as "English"
from "lexicon" and #word
where root-word
sort (file.name)asc
```

## All Inflected Words

```dataview
table gloss-eng as "English"
from "lexicon" and #word 
where !root-word
sort (file.name)asc
```
