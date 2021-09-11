# Mallard docs 

[Mallard](http://projectmallard.org/) is an awkward duck, it is written in XML and therefore can be hard to write.

Fortunately we can take our "small dog" to "hunt the Duck". 

Pug (aka jade) is a CLI tool and a kind of shorthand for writing xml/html documents. 

To get started install Node.js:

install Node.js

```
sudo apt install nodejs
```

install pug and pug-cli

```
sudo npm install -g pug && sudo npm install -g pug-cli
```

create a pug settings directory

```
mkdir ~/.pug
```

specify options for mallard page format

```
echo '{"doctype": "page"}' > ~/.pug/options-page.json
```

provide localtion of the options file, add file extension with -E and -P flag for pretty

```
pug -O ~/.pug/options-page.json -E "page" -P
```

put it in your bashrc alias

```
alias ppage='pug -O ~/.pug/options-page.json -E "page" -P'
```

convert your new page

```
ppage new-page.page
```

previewing documentation

```
yelp --editor-mode new-page.page
```

Pug is indentation sensitive, if you are using VS Code it is recomended to use something like **indent-rainbow** plugin as well as **jadeview** (to convert existing xml/html i.e *.page* files to *.jade/.pug*). 

- [Pug](https://pugjs.org/api/getting-started.html)
- [Mallard Project](http://projectmallard.org)

