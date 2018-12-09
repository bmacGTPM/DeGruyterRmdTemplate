# De Gruyter R Markdown Template

This package contains a template for writing articles in R Markdown for De Gruyter journals such as Journal of Quantitative Analysis in Sports (JQAS).  See skeleton.rmd and skeleton.pdf in the 
`inst/rmarkdown/templates/degruyter_article` folder for an example.  

Files from the "De Gruyter LaTeX Template Download" .zip file from https://www.degruyter.com/view/j/jqas were used for styling.  In particular, 

- `skeleton/dgjournal.sty` and `skeleton/DeGruyter.bst` from that .zip file are used for styling
- `skeleton/preambleDeGruyter.tex` contains a preamble from the example document in that .zip file `dg_template.tex`.   
- The `skeleton.rmd` file contains content copied from `dg_template.tex` as well. 

Note that for De Gruyter journal submissions, front matter can not be included.  Because of this, `title:`, `author`, and other similar lines are commented out in `skeleton.rmd`.

In an Arxiv submission, this front matter may be desired.  You can choose to Knit with the output format `pdf_document`, which will not use the `dgjournal.sty` styling, and will allow front matter.  The lines with the front matter can be uncommented and they will appear in the .pdf output. Note that the `pdf_document` output option has its own preamble file `preambleArxiv.tex` which can be modified as desired. 

Issues: 
Need to include fake data for a table, figure, etc., including captions. Maybe copy from another skeleton? 

JQAS/Arxiv toggle
Ideally there would be a toggle for JQAS vs Arxiv, where the Arxiv version has the front matter, TOC, etc., that DeGruyter prohibits.  This could potentially be accomplished by having two PDF output formats, degruyter and arxiv, each with different settings.  Some settings would be specified in preambleDeGruyter.text and preambleArxiv.tex.  Ideally, there would also be a preambleCommon.tex that contains common packages/commands/settings used by both formats. For now, the common settings are pasted in both. 

