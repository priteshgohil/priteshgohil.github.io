# Find and install LaTeX's missing packages in Ubuntu.

A lot of search and experiments finally helped me to install the missing packages in LaTeX. It is a bit tedious task to find and install the missing package in Ubuntu.

Let say I have a missing package "titlesec.sty" then the first step is finding the relevant Latex repository.

```$ apt-cache search titlesec ```

  shows below line and tells that repository "texlive-latex-extra" contains the missing package,
  
  ```texlive-latex-extra - TeX Live: LaTeX additional packages```

if you want to see all the containing packages you can write command,

```$ apt-cache show texlive-latex-extra```

install texlive-latex-extra,

```$ sudo apt-get install texlive-latex-extra```

You are done and now be able to use the package.
