This is a collection of a few [YASnippets](https://github.com/joaotavora/yasnippet) for the quick creation of
categorical diagrams in emacs. The snippets mostly use tikzcd.

## Usage

Imagine you wish to typeset the
[5-lemma](https://en.wikipedia.org/wiki/Five_lemma) in latex. You
could painstakingly type out all of the tikzcd code or you could use a
template that contains the majority of the code already and fill in
the relevant parts. So instead of manually typing out

```\begin{center}
\begin{tikzcd}
  A  \arrow[r,"a"] \arrow[d,"i"]
& B  \arrow[r,"b"] \arrow[d,"j"]
& C  \arrow[r,"c"] \arrow[d,"k"]
& D  \arrow[r,"d"] \arrow[d,"l"] 
& E                \arrow[d,"m"]\\
  F  \arrow[r,"e"]
& G  \arrow[r,"f"]
& H  \arrow[r,"g"]
& I \arrow[r,"h"]
& J \\
\end{tikzcd}
\end{center}
```

with this collection of snippets you could type `4-box` and then hit
tab (or whatever your yasnippet completion is set to) and this would
complete to

```\begin{center}
\begin{tikzcd}
    \arrow[r,""] \arrow[d,""]
&   \arrow[r,""] \arrow[d,""]
&   \arrow[r,""] \arrow[d,""]
&   \arrow[r,""] \arrow[d,""] 
&                \arrow[d,""]\\
    \arrow[r,""]
&   \arrow[r,""]
&   \arrow[r,""]
&  \arrow[r,""]
&  \\
\end{tikzcd}
\end{center}
```

Your cursor would appear before the first `\arrow[r,""]` and by
pressing tab your cursor will move around to the relevant fields.

## Setup 

The following assumes you have emacs with YASnippet setup. Place the
category-theory-diagrams folder inside the latex-mode folder that sits
inside of the snippets folder associated with YASnippets (if these
folders don't exist create them). The `.yas-parents` file allows these
snippets to be used in org-mode as well as latex-mode.

