# Stand Alone Images Repo

- This is a Repo to store different examples of using the `standalone` document class in LaTeX to produce equations and figures that can be directly exported as images.
- `tight-eqn.tex` shows how to use the class settings with other LaTeX tools to control equation placement and margins yourself
- `wide-eqn.tex` shows how if you do nothing but make sure the document doesn't clip your equation what you will get. My `pdfcrop` examples start from this pdf. 
- `tikz-fig.tex` shows how you can create a figure in TikZ within the standalone class. `tikz-fig.pdf` is the original pdf I then crop the pdf and convert and crop to png separately (png is not from cropped pdf).

## Usage
- LaTeX files are located in `tex-files` and images are in `images`.
- Copy the template you want from the directory and start editing there.

## Image Conversions

`pdfcrop`, `epstopdf`, `pdf2svg`, and `imagemagick` are all usefull commandline tools to convert and size images. Some of these are included in LaTeX distributions. 

- `autocrop.pdf` is the result of running `pdfcrop` on the wide-eqn output directly, i.e. `pdfcrop wide-eqn.pdf autocrop.pdf`. As you can see, it does a much better job than my user defined attempt in tight-eqn. It determines the smallest bounding box that contains all the content, and writes the cropped version. 
- `addmarg.pdf` is the result of adding margins uniformly to all sides of the auto cropped pdf with `pdfcrop --margins '10' autocrop.pdf addmarg.pdf`. This uses points, i.e. 10pt, 1pt is about .35mm. The margins follow left, top, right, bottom if you want to add margins nonuniformly, ex: '5 10 20 30'. 
- Run `pdf2svg` on pdf files to convert them to svg, `pdf2svg autocrop.pdf autocrop.svg`.
- The various pngs are from using ImageMagick's `convert`.
    - `autocrop.png` from `convert -density 600 autocrop.pdf -quality 90 autocrop.png`. The density refers to the DPI and quality is the compression factor (greater num less compression), compression doesn't affect png image resolution much but will reduce file size. Notice it has no background, this can be added with the background flag followed by a color and then the flatten flag to merge layers. It accept many named colors and hex. See [here][color-inf] for more color info.
    - You can also auto trim an image, just make sure the trim flag goes near the end. See `wide-trim.png` which came from `convert -density 600 wide-eqn.pdf -background DodgerBlue -flatten -trim -quality 90 wide-trim.png`.
    - If you want to convert a page of a multi-page pdf, you can use a specifier. Ex: `convert -density 300 input.pdf[0] -quality 90 output.png` will convert the first page of the pdf.



[color-inf]:https://imagemagick.org/script/color.phphttps://imagemagick.org/script/color.phpk
