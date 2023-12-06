# PhD Clément LAHOCHE notes

## Dataset

Etude vraiment tres interessante (ml sur un dataset de CVE crawler) : https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8809499

Dataset : https://github.com/SecretPatch/Dataset

> generation from mitre (crawling), use ml to detect them, syntaxe of the vulnerability not standard (no AST....)

## modelisation

etude sur la modelisation de faille de securité : https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4159681

> very simple models state/transition and automatic testing. This is a bit abstract (no real application)

Zhao, Jingling, Kunfeng Xia, Yilun Fu, and Baojiang Cui. “An AST-Based Code Plagiarism Detection Algorithm.” In 2015 10th International Conference on Broadband and Wireless Computing, Communication and Applications (BWCCA), 178–82. Krakow, Poland: IEEE, 2015. https://doi.org/10.1109/BWCCA.2015.52.

> use AST, compare hash of the sub-tree, no time indication

HyperAst ([paper](https://dl.acm.org/doi/abs/10.1145/3551349.3560423), [code](https://github.com/HyperAST/HyperAST))

> use AST, add time component, add metadata

Yang et al., “Asteria.”

> Use Ast and dl (tree-LSTM) to detect security vulnerability, [code](https://github.com/Asteria-BCSD/Asteria)