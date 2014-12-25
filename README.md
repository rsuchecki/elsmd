# Markdown to lecture slides

(with some beamer bells and whistles, by a Keynote refugee)

Create notes in the `notes/` directory, on the model of [classnotes.md](notes/classnotes.md). Then generate a PDF of slides with

```Make
make -C slides classnotes.pdf
```

[slides/classnotes.pdf](slides/classnotes.pdf) is the result on my system.
(Of course you can also `cd slides; make classnotes.pdf`, but I feel more like a command-line master if I use `make -C` from the top-level directory.)

If you have Keynote and want to use it as a presentation PDF viewer, install [PDF to Keynote](http://www.cs.hmc.edu/~oneill/freesoftware/pdftokeynote.html) and then do

```Make
make -C slides classnotes.key
```

To generate notes (note pages interleaved with slide pages):

```Make
make -C notes classnotes.pdf
```

[notes/classnotes.pdf](notes/classnotes.pdf) is the result on my system.

I like to print these 4-up in landscape. That last step is automatable, but I haven't gotten around to that yet (hurrah, new project).


To make all PDFs and Keynote files at once, use `make` from the toplevel directory. (One feels even more of a command-line master when one uses `$(MAKE)` in a Makefile).

I discuss how the bits and pieces work together, and the rationale for doing this, in a blog post: ["Easy Lecture Slides Made Difficult with Pandoc and Beamer."](http://andrewgoldstone.com/blog/2014/12/24/slides/)

