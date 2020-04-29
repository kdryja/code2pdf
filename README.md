# code2pdf
Convert source files into a pdf
 
## Why?
My University requires me to submit all code produced as as single PDF. No idea why would they do that, but I wanted to make my code at least somewhat presentable and life at least a little bit easier.

# Usage
It's a simple Python script with a single dependency: xhtml2pdf.

First install the dependency:
```pip install xhtml2pdf```

Now you can point the script towards your source code using `-dst`, specify output name using `-out` and list the file extensions that you would like to include in the pdf as positional arguments.

The script will recursively traverse specified directory, including only the requested extensions.

NOTE: The lines will break if they're over 120 characters. I think it's a sensitive limit.

## Example
```python code2pdf.py -dst "/home/kdryja/University/thesis/code" -out code.pdf go sol html js sh txt```

This command will traverse directory `/home/kdryja/University/thesis/code` looking for files with either of those extensions `go sol html js sh txt` and writing them to a pdf named `code.pdf`.

Tested on Python 3.8.2 and xhtml2pdf 0.2.4.
