# Algorithm Line `autoref` 

The default `autorefname` for lines inside algorithm environment provided by [`algorithm2e`](http://tug.ctan.org/tex-archive/macros/latex/contrib/algorithm2e/doc/algorithm2e.pdf) is **line**. However, 
you might want to change it to **L**ine. 

In this repo, we provide you a simple way to do so. 

```TeX
\renewcommand{\algorithmcflinename}{Line}
```

## A Minimal Working Example

```TeX
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage[colorlinks,linkcolor=blue]{hyperref}

\usepackage[linesnumbered,boxed]{algorithm2e}
\usepackage{xcolor}

\renewcommand{\algorithmautorefname}{Algorithm}
\renewcommand{\algorithmcflinename}{Line}

\begin{document}
\title{Test Line Autoref of Algorithm2e}
\author{saber}
\maketitle 

\begin{algorithm}[H]
\caption{Hello World}\label{alg: hello-world}

printf("Hello World!!")\;\label{helloworld: print}

\end{algorithm}

\autoref{helloworld: print}

\end{document}
```

The pdf produced by the above MWE looks as follows.

![](./mwe.png)



