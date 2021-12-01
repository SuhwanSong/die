die: a paper template
=====================
### 1. Prerequisites
  - Python 3.x
  - pygmentize
  - texlive
 ``` $ ./bin/deps.sh ```

### 2. Build
``` $ make ```
    (check p.pdf)

### 3. Files
```
    $ grep -oP 'input{\K\w+' p.tex
```
    cmds
    rev
   *hdr
    abstract
   *ex
    intro
    overview
    design
    impl
    eval
    conclusion
    ack

  - hdr: includes title/author info
  - ex : includes latex examples

### 4. Formatting Rules (dependencies)

  - code/*.{c,cc,py,js ...} -> code/*.tex
  - fig/*.svg               -> fig/*.pdf
  - data/*.gp               -> fig/*.tex

## Tools

#### 1. make a draft for revision
```shell
    $ make draft
    $ make watermark
```
#### 2. abstract.txt (from abstract.tex)
```shell
    $ cat abstract.txt 
```

#### 3. highlight changes, since the last submit
```shell
    $ make diff DIFF=HEAD@{}
```

#### 4. spell check
```shell
    $ make spell
```

#### 5. text extraction
```shell
    $ make text
```
