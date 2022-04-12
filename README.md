# Scripts related to: A Review of Publishing and Sharing Practices for Machine Learning Objects for Informing Library Curation Practices

## Project Overview
The goal of this project is to inform internal and community practices for curating machine learning (ML) objects, so that the relationships between the components of ML objects—experiments, tasks, algorithms, datasets, features, models, hardware/software platforms, parameters, and evaluation measures—are made explicit and can be readily understood or reused when the objects are accessed by future users. To that end, this project documents and assesses the way ML objects are currently shared in scientific repositories, to identify commonalities in structure and documentation as well as any apparent barriers to reuse. These barriers may include, for example, missing components (for a given task), idiosyncrasies in labeling (or lack thereof) of components, and variability in file organization. By identifying the core components of various ML objects and their needed documentation, we hope to move the community toward a common practice for curation as well as to increase efficiency by facilitating interoperability and reuse of ML components.

The specific objectives for this project are to survey ML research objects currently published in common scientific data repositories, to assess: 1) which components of the ML lifecycle are being shared and 2) how ML objects are being documented. In evaluating this compiled information, we further aim to 3) formally specify the core features necessary in curated ML objects to enable reuse by a user with basic knowledge of ML.

This GitHub repository contains scripts used to query the APIs and/or web scrape for the following repositories:

**ML-focused repositories**
* [Kaggle](https://www.kaggle.com/)
  * Kaggle is a popular ML data and model hub, frequently used by students and others learning ML. Documentation can be variable, but components are intended to be reused, meaning documentation provided is “minimally viable” in terms of reuse.
* [OpenML](https://www.openml.org/)
  * Classifies ML components experiments into 5 semi-hierarchical categories, each with specific documentation fields: datasets, tasks, flows, runs, and studies.
* [Papers with Code](https://paperswithcode.com/)
  * Site intended to host papers linked to relevant datasets and code as well as related performance metrics.
* [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)
  * This popular ML repository primarily hosts training and test datasets, with broad variability in documentation. Useful for identifying which properties of ML datasets are documented when reuse is anticipated. At time of project, no public API; metadata extracted by web scraping.

**Generalist repositories**
* [Figshare](https://figshare.com/)
  * A non-curated generalist repository, with a soft limit of 20 GB. Offers several Creative Commons and open source licenses.
* [Zenodo](https://zenodo.org/)
  * A non-curated generalist repository, free of charge up to 50 GB per dataset. Integration with GitHub allows users to publish their GitHub repositories easily. Offers hundreds of open licenses.
* [Dryad](https://datadryad.org/stash)
  * A lightly curated generalist repository for datasets, with a soft limit of 300 GB/dataset. Assigns the CC0 public domain dedication to all submissions.
* [Harvard Dataverse](https://dataverse.harvard.edu/)
  * Offers tiered curation with deposits and a limit of 1 TB. In addition to serving as a repository for research data, depositors can submit their data and code as a container “dataverse” with all necessary data and metadata. CC0 is highly encouraged, and applied by default.

Each notebook contains repository-specific code and instructions to query and extract metadata for all objects matching specified search terms.

In the case of ML-focused repositories, the code here extracts the entirety of the repository (search terms not necessary). For generalist repositories, search term is set as "machine learning" and can be edited as needed to meet alternative search criteria.

This project was funded in part by a research grant from the Librarians Association of the University of California (LAUC).
