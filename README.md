## Motivation

Suppose you want to import the contents of A.ipynb into B.ipynb

## How to use

Place import_ipynb.py and both ipynb files in the same directory. Then, in the B.ipynb:

```ruby
import import_ipynb
import A
```

Congratulations! You can not run any functions defined in A.ipynb, from B.ipynb!

## How it works

The code within import_nb.py defines a "notebook loader" that allows you to 'import' other ipynb files into your current ipynb file. This entails:

1. load the notebook document into memory
2. create an empty Module
3. execute every cell in the Module namespace

Note that since every cell in the A.ipynb is executed when you import the the file, A.ipynb should only contain classes and function definitions (otherwise you'll end up loading all variables and data into memory).
 

## Credit

The code within imoprt_ipynb.py comes from ((http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Importing%20Notebooks.html). I've just packaged it and written instructions on how to use it.
