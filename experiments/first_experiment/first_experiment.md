# 1st Experiment

Objectif : Detect a CVE inside a repo, and correct it

Protocole : 
- identify a CVE with code, repository (link with swh) and patch (can be determine if the code isn't the same in an afterward commit)
> Trying with rust, if not, C++/C
- identify the repository and the commit with the cve
- Use HyperAST to make the AST of the repository and try to detect the CVE (Tree matching ?)
- Use Tree-sitter on 2 of the version of the repository (one with and one without)
- Same with the compuiler of the language
- compare the performance (time, RAM)

> Follow of the experiment : scaling to swh

# TODO

- [ ] Find the CVE
- [ ] Use [openCVE](https://docs.opencve.io/installation/manual/) to build the postgreesql database and keep only entry with link with `patch` tag and an url matching a pull request 
- [ ] Research on how the AST are represented
- [ ] Research on how to compare AST

# Find the CVE

Use the following [cite](https://www.opencve.io/cve?vendor=rust-lang) (Scrap 3 site : NVD, Mitre and CVE.ORG)

> [Here](https://github.com/opencve/opencve/blob/master/opencve/commands/imports/cve.py) is the CVE scapping from NVD, [here](https://github.com/opencve/opencve/blob/master/opencve/commands/imports/cwe.py) the scrapping from mitre

Candidate :
- [This](https://www.opencve.io/cve/CVE-2019-9169) one is a C vulnerability in [GLIBC](https://archive.softwareheritage.org/browse/origin/directory/?origin_url=https://sourceware.org/git/glibc) and in a if (good AST)
- [This](https://www.opencve.io/cve/CVE-2023-0687) one is a C vulnerability in [GLIBC](https://archive.softwareheritage.org/browse/origin/directory/?origin_url=https://sourceware.org/git/glibc) and concern two pointer allocation
