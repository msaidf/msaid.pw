+++
title = "Pengenalan Latex"
date = 2018-06-26T22:59:49+07:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []
categories = []

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++

## I. Setup Latex
#### 1. Latex Online Siap Pakai
- [Sharelatex](https://www.sharelatex.com?r=612d83fd&rm=d&rs=b): dropbox sync (paid), track changes (paid)
- [Overleaf](https://www.overleaf.com): free unlimited collaborators, project versioning (manual free, automatic paid) and diff, free import bib from zotero,mendeley,and citeulike, free git

#### 2. Install Latex di Komputer
- Latex Engine
  - Tinytex ([windows](https://github.com/yihui/tinytex/raw/master/tools/install-windows.bat)/[mac](https://github.com/yihui/tinytex/raw/master/tools/install-unx.sh)/[linux](https://github.com/yihui/tinytex/raw/master/tools/install-unx.sh))
  - [Miktex](https://miktex.org/download)
- Editor
  - Editor khusus LaTeX: [TexMaker](http://www.xm1math.net/texmaker/download.html), [TexStudio](https://www.texstudio.org/)
  - Advanced text editor dengan add-on latex (emacs, vim, sublime, dll)
  - Simple text editor seperti Notepad

## II. Template Dokumen

```tex
% Pembuka
\documentclass[12pt, a4paper, twocolumn]{article} % font 12 pt, kertas A4, 2 kolom per halaman, format artikel jurnal
\usepackage[utf8]{inputenc}
\usepackage{amsmath} % pengaturan format persamaan
\usepackage{graphicx} % pengaturan grafik
\usepackage{setspace} % bisa menentukan spasi antar baris
\usepackage[a4paper,top=3cm,bottom=2cm,left=3cm,right=3cm,marginparwidth=1.75cm]{geometry}
\usepackage[colorinlistoftodos]{todonotes}
\usepackage[colorlinks=true, allcolors=blue]{hyperref}
\usepackage{natbib} % menyediakan berbagai format referensi
\bibliographystyle{apalike} % format referensi APA

% Judul
\title{Judul}
\author{author \thanks{funded by funder}} % thanks akan jadi footnote
\date{\today} % \today otomatis mengisi dengan tanggal pdf di-compile, bisa diganti manual dengan string

% Isi
\begin{document}

%\begin{title} % jika ingin halaman judul terpisah

\maketitle % print judul

% \end{title}  % jika ingin halaman judul terpisah

\begin{abstract}
abcdefg

hijklmn

Keywords: First keyword, second keyword, third keyword

JEL Classification: XXX, XXX
\end{abstract}

\tableofcontents % daftar isi

\section{Pendahuluan}
aaaaaaaaaa
aaaa

bbbbbbbbbbbbb
bbbb

\section{Tinjauan Literatur}

\citet{bibkey)
\citet[lihat][bab 2]{bibkey}
\citet[misal][]{bibkey}
\citet[hal. 10]{bibkey}

\begin{quote}
ccccccccccccccc

ddddddddddd \citep[hal. 10]{bibkey}. 
\end{quote}

\citep{bibkey)
\citep[lihat][bab 2]{bibkey}
\citep[misal][]{bibkey}


\section{Metode}
\subsection{Data}

\begin{enumerate}
\item Like this,
\item and like this.
\end{enumerate}

\dots or bullet points \dots

\begin{itemize}
\item Like this,
\item and like this.
\end{itemize}

\subsection{Model}

Let $X_1, X_2, \ldots, X_n$ be a sequence of independent and identically distributed random variables with $\text{E}[X_i] = \mu$ and $\text{Var}[X_i] = \sigma^2 < \infty$, and let

\[S_n = \frac{X_1 + X_2 + \cdots + X_n}{n}
      = \frac{1}{n}\sum_{i}^{n} X_i\]
      
atau dibuat 2 baris

\begin{equation}

\begin{align}
S_n &= \frac{X_1 + X_2 + \cdots + X_n}{n} \\
    &= \frac{1}{n}\sum_{i}^{n} X_i
\end{align}
\end{equation}

denote their mean. Then as $n$ approaches infinity, the random variables $\sqrt{n}(S_n - \mu)$ converge in distribution to a normal $\mathcal{N}(0, \sigma^2)$.

\section{Hasil}
see Table~\ref{tab:widgets}, for example. 


\section{Simpulan}

% print referensi yang dikutip bibkey merujuk pada satu atau lebih bibfile
\bibliography{`/path ke/bib file 1`, /path/ke/bibfile2, bibfile3} 

\newpage % di bawah ini akan dicetak pada halaman baru

\appendix

\section{Tables} 

\input{.. /tables/table1} 

\begin{table}
\centering
\begin{tabular}{r|l c}

Item & Quantity & Price  \\\hline
Widgets & 42 & 10\\
Gadgets & 13 & 25

\end{tabular}
\caption{\label{tab:widgets}An example table.}
\end{table}

\section{Figures} 

\begin{figure}
\centering
\includegraphics[width=0.3\textwidth]{frog.jpg}
\caption{\label{fig:frog}This frog was uploaded via the project menu.}
\end{figure}



\end{document}
```