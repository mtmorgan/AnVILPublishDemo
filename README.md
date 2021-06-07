# AnVILPublishDemo

This package illustrates how the AnVILPublish package can produce AnVIL workspaces that include Jupyter notebooks, AnVIL DATA, and other famiilar  workspace elements, as well as metadata on provenance, versioning, software specification, and other necessary elements of reproucible research.

We'll use AnVILPublish to publish this package!

Workspace configuration. We'll start by updating the workspace to current software versions.

```{r, eval = FALSE}
## options(Ncpus = 2)  # faster installation, even if runtime 'oversubscribed'
## BiocManager::install(ask = FALSE)           # update installed packages
pkgs <-  c("Bioconductor/AnVIL", "Bioconductor/AnVILPublish")
BiocManager::install(pkgs)  # latest AnVIL and AnVILPublish packages
```
