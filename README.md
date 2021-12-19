# Reactor-C: A reactor runtime implementation in C

## Documentation
To generate and view documentation, follow the following steps:
- Install `python3`, `pip3` and `doxygen`
- Install the required Python modules:
  - `pip3 install sphinx`
  - `pip3 install sphinx_sitemap`
  - `pip3 install sphinx-rtd-theme`
  - `pip3 install breathe`
  - `pip3 install exhale`
- Check out this repo and build the docs:
  - `git clone git@github.com:lf-lang/reactor-c.git`
  - `cd reactor-c/doc-sphinx`
  - `make html`
- Point your browser to the generated HTML page:
  - `firefox _build/html/index.html`

To create a new test, write a C program with a file name ending in "test.c"
in the `test` directory.

To run unthreaded tests, execute the following. Note that -U is required to undefine
a name.
- `cd build`
- `cmake .. -UNUMBER_OF_WORKERS`
- `cmake --build .`
- `make test`

To run threaded tests, provide a nonzero number of workers when invoking `cmake ..`.
For example:
- `cmake .. -DNUMBER_OF_WORKERS=2`
