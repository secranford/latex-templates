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
4. There are typically `template` and `example` directories in each directory. You can review the example and copy and use the template files to meet your needs. Delete what you don't want or need.

## Some good resources:

- [Video][SeniorMars-Notes] on some useful tips for taking notes/doing hw in LaTeX
- Blog posts [1][blog-one] and [2][blog-two] on note-taking and tips inspired the template I copied from.
- LaTeX workshop is the VS Code extension I use. It has many nice features and good [documentation][lt-work]. Use `latexmk` for building (this is how Overleaf and many compilers auto handle compiling). 

[senior-mars-repo]: https://github.com/SeniorMars/dotfiles/tree/79f266bbfeb0dcdcba42284140d84f84af00f950/latex_template
[SeniorMars-Notes]: https://youtu.be/DOtM1mrWjUo?si=hfBw6kDHB7MjBjpv
[blog-one]: https://castel.dev/post/lecture-notes-3/
[blog-two]: https://castel.dev/post/lecture-notes-1/
[lt-work]: https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop
