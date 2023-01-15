# sed

cheatsheet of sed.

# Replace with sed

```txt
The list below gives you the 1000 most frequently used English words in alphabetical order. Once you've mastered the shorter vocabulary lists, this is the next step. It would take time to learn the entire list from scratch, but you are probably already familiar with some of these words. Feel free to copy this list into your online flashcard management tool, an app, or print it out to make paper flashcards. You'll have to look up the definitions on your own either in English or in your own language. Good luck improving your English vocabulary!
```

How to find and substitute 1000 with 9999 using sed on MacOS

```console
sed -e "s/1000/9999/" -i "" sample.txt
```

```console
cat sample.txt
````

Console output

```txt
The list below gives you the 9999 most frequently used English words in alphabetical order. Once you've mastered the shorter vocabulary lists, this is the next step. It would take time to learn the entire list from scratch, but you are probably already familiar with some of these words. Feel free to copy this list into your online flashcard management tool, an app, or print it out to make paper flashcards. You'll have to look up the definitions on your own either in English or in your own language. Good luck improving your English vocabulary!
```

# scape slash character to find a path

Replace / with \/ to scape slash character

```console
echo "/path/to/some/where/" | sed -e "s=/=\\\/=g"
```

output

```console
\/path\/to\/some\/where\/
```
