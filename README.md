# LaTeX Templates Repo

- This is a Repo to store my different LaTeX files, examples, and templates for my own use or for sharing with others.
- `original-files` is a repo containing the LaTeX template files from [@SeniorMars' repository][senior-mars-repo]. 
- `notes-template` is a repo adapted from that template to suit my own needs and preferences for taking notes on different topics.
- `standalone` is a repo for using the standalone class to export equations or figures made in LaTeX, i.e. create a pdf of an equation or TikZ figure exactly so it can be inserted in a document or presentation. 
- `latex-workshop-settings.json` are the VS Code specific settings I use for formatting and LaTeX workshop.

## Usage
1. Pull down repo.
2. Copy the directory of the template you want to use, i.e. `notes-template` for taking notes and put it where you intend to use.
3. Copy the `.gitignore` file from into your copied repo if you plan to use git with it and want to ignore aux files.
4. There are typically `template` and `example` directories in each directory as well as READMEs. This is the primary README but the lower level ones will have more specific info. You can review the example and copy and use the template files to meet your needs. Delete what you don't want or need.

## Bibliography Styles:

- I have added a few bibliography styles to the `bib-styles` directory.
- new-aiaa.bst is the format aiaa provides in their templates. I don't recommend using this if you don't have to because it is a bibtex style file and biblatex is a more modern and robust option. My templates use biblatex and so some changes would have to be made to use bibtex styles.
- aiaa.bbx and aiaa.cbx are custom biblatex format styles I got from a nasa [repo][nasa-repo]. I did change doi to be true in the template.
- The easiest way to use custom style files is to just put them in the same folder as your latex project.
- The more robust way is to use the TEXMF option:
1. make the correctly formatted file path: ~/texmf/tex/latex/biblatex/ for biblatex files and ~/texmf/bibtex/bst/stylename/ for bibtex files
2. place the files within the above directories
3. use texhash followed by the file name if the file does not show up when you run `kpsewhich` followed by the file name.

## Some good resources:

- [Video][SeniorMars-Notes] on some useful tips for taking notes/doing hw in LaTeX
- Blog posts [1][blog-one] and [2][blog-two] on note-taking and tips inspired the template I copied from.
- LaTeX workshop is the VS Code extension I use. It has many nice features and good [documentation][lt-work]. Use `latexmk` for building (this is how Overleaf and many compilers auto handle compiling). 

## LaTeX Workshop Tips:

- [This][lt-work-tips-vid] video has some useful tips on setting up and getting good utilization out of LaTeX workshop
- I have also included my latex-workshop specific VS Code settings.json that are helpful for getting formatting and intellisense. While some of the options I have turned on are the "defaults", I have found that they are not always respected especially if going back and forth from wsl and windows.
- SyncTeX compatibility allows you to navigate the pdf and code through eachother. You can `ctrl + click` in the pdf to be taken to the place in the code, it will also flash highlight the specific code yellow. Using `ctrl + alt + j` in the code location to be taken to the pdf location, it will also flash highlight the specic pdf section red.
- You will need to install `latexindent` if you want access to full formatting and bib sorting capabilities. This is very useful.

[senior-mars-repo]: https://github.com/SeniorMars/dotfiles/tree/79f266bbfeb0dcdcba42284140d84f84af00f950/latex_template
[SeniorMars-Notes]: https://youtu.be/DOtM1mrWjUo?si=hfBw6kDHB7MjBjpv
[blog-one]: https://castel.dev/post/lecture-notes-3/
[blog-two]: https://castel.dev/post/lecture-notes-1/
[lt-work]: https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop
[lt-work-tips-vid]: https://youtu.be/vIImoKpKWIo?si=QrPB8fIhkqYQEETm
[nasa-repo]: https://github.com/nasa/nasa-latex-docs.git