# Fix LaTeX compiler not found 

After upgrading Mac OS, TexShop does not find LaTeX compiler anymore. Creating a symbolic link fixes the problem:

```
sudo ln -s /usr/local/texlive/2014/bin/x86_64-darwin/pdflatex /Library/TeX/texbin/pdflatex

```
