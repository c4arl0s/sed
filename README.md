# sed

`sed` – stream editor

# SYNOPSIS

```vim
sed [-Ealnru] command [-I extension] [-i extension] [file ...]
sed [-Ealnru] [-e command] [-f command_file] [-I extension] [-i extension] [file ...]
```

# EXAMPLES

- Replace `‘bar’` with `‘baz’` when piped from another command:

```console
echo "An alternate word, like bar, is sometimes used in examples." | sed 's/bar/baz/'
```

- Using backlashes can sometimes be hard to read and follow:

```console
echo "/home/example" | sed  's/\/home\/example/\/usr\/local\/example/'
```

- Using a different separator can be handy when working with paths:

```console
echo "/home/example" | sed 's#/home/example#/usr/local/example#'
```

- Replace all occurances of ‘foo’ with ‘bar’ in the file test.txt, without creating a backup of the file:

```console
sed -i '' -e 's/foo/bar/g' test.txt
```

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

# Find a string block between two patterns

```bash
sed -n '/PAT1/,/PAT2/p' FILE
```

# Remove empty lines in a file

cat file.txt

```console
PATTERN1
73281t478124
73218362131
321y748t2148t
PATTERN2

PATTERN1
dhsajdgghqwdbhj
dshajdgsahdjashjd
hdghjsagdhjas
hgshjdagdhj
dhsajdhasj
PATTERN2

===============

PATTERN1
236713
372183671
362163721
PATTERN2
```

```console
cat file.txt | sed "/^ *$/d"
```

Output

```console
PATTERN1
73281t478124
73218362131
321y748t2148t
PATTERN2
PATTERN1
dhsajdgghqwdbhj
dshajdgsahdjashjd
hdghjsagdhjas
hgshjdagdhj
dhsajdhasj
PATTERN2
===============
PATTERN1
236713
372183671
362163721
PATTERN2
```

# old solution

```bash
find . -name "*.txt" | while read txtfile; do sed -i "" -e "s/ : /:/g" ${txtfile}; done
```

<img width="1022" alt="Screenshot 2024-11-03 at 8 12 36 p m" src="https://github.com/user-attachments/assets/466b548b-f3b1-4c24-a689-e5811e4dee82">
