thesis-project-bootstrap.istecni.co
===================================

A LaTeX project template for your awesome Thesis Project (using Springer theme, requested  by IST).

I've been known as a "productivity freak" for some years know and when I started writting my thesis, it really annoyed me how the tools seemed old and brokwn, the process was old, there was no better practices around and all the documentation I found on the web wasn't cohesive. 

So, hoping that I could save someone else's time, I've been compiling this `bootstrap template`, sharing what worked as best for me. This template is dedicated to the first part of the thesis (project), I hope to have something for the full thesis when I do it :)

Please if you have something to add, or a thing you like to share, open a issue or a pull request :)

## Acknowlegments 

Some of this best practices came from discussions I had with my friend [Bernardo Simões](https://github.com/golfadas), which is doing his Thesis at the same time as me, he shares the same desire of getting the clutter out of the way to maximize the focus on the content.

**News:** I just heard that he applied for a LaTeX talk at Codebits, you should go and upvote him -> https://codebits.eu/intra/s/proposal/472


## Folder structure

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
├── sections            # You can find each individual section here (these are the requested)
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

## Tools

##### Mendeley 

![mendeley](http://d3fildg3jlcvty.cloudfront.net/20140120-01/graphics/commonnew/logo-mendeley.png)

"Mendeley is a free reference manager and academic social network that can help you organize your research, collaborate with others online, and discover the latest research."

Now that the public pitch is off, the truth is that you will be there, having to manage dozens of papers, notes, references, and you definitly don't want to do it on paper, after reading 40 papers, how the hell are you going to find quickly that one reference you are looking for. Then you start thinking, lets "be smart" and start taking notes in word, or an excell spreadsheet (I've seen all of these cases), but then you realize searching in this type of documents is hard and in the end, you still have to compile your bibliography by hand (because of the .bib format needed by LaTeX). Fear not, Mendeley is here to save you from all that pain, in the Tips section we will specify some key things you can do with Mendeley, for now, just [install](http://www.mendeley.com/) it and watch this [video](http://vimeo.com/26866765) 

##### Sublime

![sublime](http://upload.wikimedia.org/wikipedia/en/4/4c/Sublime_Text_Logo.png)

I've tried a ton of text editors for LaTeX, from [TexShop](http://pages.uoregon.edu/koch/texshop/), [Latexian](http://tacosw.com/latexian/) to [Scribo](https://www.macupdate.com/app/mac/30939/scribo), but in the end, what has proven to be the most reliable, clean and fastest is my old beloved [Sublime Text](http://www.sublimetext.com/), which I used for all my coding.

What I was looking in the text editor was for a good theming scheme, simply layout, powerful auto complete and well defined snippets for me. All of this was achieved by installing [latexing](http://www.latexing.com/) for Sublime. You can install it using the Sublime Package Manager

```
press cmd+shift+p on a mac or ctrl+shift+p on windows/linux
type install package and click enter
type latexing and select that package
```

Check all the Latexing [features here](http://www.latexing.com/features.html)

## Tips

##### How to start

Just click the `fork` button on the top right of this webpage and get started :) (you can always download as zip if you prefer).

##### How to Compile/Export to PDF

You would expect that compiling would be something linear, however, LaTeX has it is own peculiatiries, specially when you have a bibliography. The process goes

```bash
$ pdflatex report # compile once
$ bibtex report   # compile the references
$ pdflatex report # compile again to attach the compiled references
$ pdflatex report # compile again just to make the ref numbers appear accordingly
```

I know this seems odd, I myself didn't believe this was the way in the beginning and tried to find a more 'natural' way, however, after reading a bunch of stuff on the web and getting feedback from other people, yep, this is how it is done.

I've added to this repo a script to do this automatically `toPDF.sh`, this script also has a "cleaning" function, to remove all the temporary files from your folder created by `pdflatex` compile step, so it you don't get your folder "full of things" :)

To execute it, just open your terminal and then

```bash
$ sh toPDF.sh
```

##### Set your .bib file

##### Citations

##### Change margins



##### Distraction Free Mode

The web is full of distractions, writting long chunks of text can be boring sometimes, you need something to keep your focus on and don't get distracted, that is when the Distraction Free Mode of Sublime kicks in, to activate it, just press:

```
ctrl+shift+cmd+f
```


##### Snippets

##### Take notes on Mendley 



## Notes/Others

##### Difference between `\input` and `\include`

As this [answer](http://tex.stackexchange.com/a/250) eloquently put's it out:

\input{filename} imports the commands from filename into the target file; it's equivalent to typing all the commands from filename right into the current file where the \input line is.

\include{filename} essentially does a \clearpage before and after \input{filename}, together with some magic to switch to another .aux file, and omit the inclusion at all if you have an \includeonly without the filename in the argument. This is primarily useful when you have a big project on a slow computer; changing one of the include targets won't force you to regenerate the outputs of all the rest

\include gets you the speed bonus, but it also can't be nested, can't appear in the preamble, and forces page breaks around the included text.
