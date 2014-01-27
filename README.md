thesis-project-bootstrap.istecni.co
===================================

A LaTeX project template for your awesome Thesis Project (using Springer theme, requested  by IST).

I've been known as a `productivity freak` for some years know and when I started writting my thesis, it really annoyed me how the tools seemed old and brokwn, the process was old, there was no better practices around and all the documentation I found on the web wasn't cohesive. 

So, hoping that I could save someone else's time, I've been compiling this `bootstrap template`, sharing what worked as best for me. This template is dedicated to the first part of the thesis (project), I hope to have something for the full thesis when I do it :)

Please if you have something to add, or a thing you like to share, open a issue or a pull request :)

### Acknowlegments 

Some of this best practices came from discussions I had with my friend [Bernardo Simões](https://github.com/golfadas), which is doing his Thesis at the same time as me, he shares the same desire of getting the clutter out of the way to maximize the focus on the content.

**News:** I just heard that he applied for a LaTeX talk at Codebits, you should go and upvote him -> https://codebits.eu/intra/s/proposal/472


### Folder structure

```bash
.
├── LICENSE
├── README.md
├── example.bib         # An example file of bibliography, you should replace with your own
├── img                 # Here we store all our images for the report
│   └── rubberduck.jpg
├── llncs2e
│   ├── aliascnt.sty
│   ├── history.txt
│   ├── llncs.cls
│   ├── llncs.dem
│   ├── llncs.doc
│   ├── llncsdoc.pdf
│   ├── llncsdoc.sty
│   ├── objectives.tex
│   ├── readme.txt
│   ├── remreset.sty
│   ├── splncs.bst
│   ├── splncs03.bst
│   ├── splncs_srt.bst
│   └── sprmindx.sty
├── report.pdf          # The exported report as .pdf
├── report.tex          # The main file of the report
├── sections            # You can find each individual section here
│   ├── 1-abstract.tex
│   ├── 2-keywords.tex
│   ├── 3-introduction.tex
│   ├── 4-objectives.tex
│   ├── 5-related-work.tex
│   ├── 6-architecture.tex
│   ├── 7-evaluation.tex
│   └── 8-conclusions.tex
└── toPDF.sh            # Compiling and exporting your report to pdf, use $ sh toPDF.sh to run it 
```

### Tools

#### Mendeley 


#### Sublime

Package LaTeX + Snippets


### Tips

#### How to Compile

#### Set your .bib file

#### Citations

#### Change margins

#### Difference between