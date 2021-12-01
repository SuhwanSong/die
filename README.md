die: a paper template
=====================
### 1. Prerequisites
  - Python 3.x
  - pygmentize
  - texlive

 ```shell
 $ ./bin/deps.sh 
 ```

### 2. Build
```shell 
$ make 
```

(check p.pdf)

### 3. Files

  - p.tex -> main tex file
  - hdr.tex -> title and authors

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
