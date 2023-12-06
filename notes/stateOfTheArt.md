# PhD Clément LAHOCHE notes

## Dataset

Etude vraiment tres interessante (ml sur un dataset de CVE crawler) : https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8809499

Dataset : https://github.com/SecretPatch/Dataset

> generation from mitre (crawling), use ml to detect them, syntaxe of the vulnerability not standard (no AST....)
> The list of the CVE can be found [here](https://www.cve.org/Downloads), it use [CVRF](https://cve.mitre.org/cve/cvrf.html) syntaxe (XML derived) or JSON.
> The patch aren't clear for all the CVE

## modelisation

etude sur la modelisation de faille de securité : https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4159681

> very simple models state/transition and automatic testing. This is a bit abstract (no real application)

Zhao, Jingling, Kunfeng Xia, Yilun Fu, and Baojiang Cui. “An AST-Based Code Plagiarism Detection Algorithm.” In 2015 10th International Conference on Broadband and Wireless Computing, Communication and Applications (BWCCA), 178–82. Krakow, Poland: IEEE, 2015. https://doi.org/10.1109/BWCCA.2015.52.

> use AST, compare hash of the sub-tree, no time indication

HyperAst ([paper](https://dl.acm.org/doi/abs/10.1145/3551349.3560423), [code](https://github.com/HyperAST/HyperAST))

> use AST, add time component, add metadata

Yang et al., “Asteria.”

> Use Ast and dl (tree-LSTM) to detect security vulnerability, [code](https://github.com/Asteria-BCSD/Asteria)

## Software heritage

the [API](https://archive.softwareheritage.org/api/), a local [instance](https://docs.softwareheritage.org/devel/getting-started/index.html), [python tool lister](https://forge.softwareheritage.org/source/swh-lister/)

Pietri, Spinellis, and Zacchiroli, “The Software Heritage Graph Dataset.”

> Make a DAG of Software heritage (on the metadata and the files), make query like "what is the most used name"