# Master's Thesis Template


This skeleton thesis provides a basic template from which
to start writing a Master's thesis in LaTeX in the database
research group at NTNU, Trondheim.

------------------------------------
## Usage and Dependencies

The `latex/` directory contains a _minimum working example_
that you can compile immediately using your favourite LaTeX
engine (I suggest _lualatex_ or _xelatex+) and the _biber_
bibliography engine. Recall that you should run _latex_ once,
then _biber_, then _latex_ twice more.

Alternatively, this template has been set up to use _cmake_
to automate the (out-of-source) build process.
You will first need to install a dependency
(not bundled here, because the license is unclear)
by copying `UseLATEX.cmake` from https://gitlab.kitware.com/kmorel/UseLATEX
into the `latex` directory.
Then, to build the thesis, create an out-of-source directory (e.g., `pdf`)
and run `cmake` with `biber` and your preferred LaTeX engine:

> mkdir pdf
>
> cd pdf
>
> cmake -DBIBTEX_COMPILER=/usr/bin/biber -DPDFLATEX_COMPILER=/usr/bin/lualatex ../latex/
>
> make
>
> evince msc-thesis-template.pdf &


------------------------------------
## Contact

If you have any questions about using the template, please contact
the repository owner: @sean-chester


------------------------------------
