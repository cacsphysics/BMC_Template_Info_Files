# BMC_Template_Info_Files
The purpose of this repository is to complement the template repository through latex-package manuals and links related to the packages employed in the BMC template.

# Bibliography Setup
The bibliography setup currently used within the template was constructed with various stackexchange information. The solutions within [the link](https://tex.stackexchange.com/questions/400644/no-hanging-indent-with-biblatex-in-bibliography) are very helpful.

The Bibliography code block:
```
{
\RequirePackage[
        backend=biber,
        style=phys,
        biblabel=brackets,
        articletitle=true
    ]{biblatex}
    \defbibenvironment{bibliography}
        {\list{\printtext[labelnumberwidth]{%
            \printfield{labelprefix}%
            \printfield{labelnumber}}}
        {\setlength{\leftmargin}{\bibhang}%
            \setlength{\itemindent}{-\leftmargin}%
            \setlength{\itemsep}{2\baselineskip plus .05\baselineskip minus .05\baselineskip}%
            \setlength{\parsep}{\bibparsep}}
        }
        {\endlist}
    {\item}
}
```



