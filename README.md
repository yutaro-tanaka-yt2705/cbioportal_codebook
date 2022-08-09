# cBioPortal Codebook 📖 📊 ✨
A community shared resource of Python and R Analysis Recipes that utilize the cBioPortal REST API

## Python
See [intro.ipynb](./python/intro/intro.ipynb)

## R
Best place to start is the [2020-cbioportal-r-workshop](https://github.com/cBioPortal/2020-cbioportal-r-workshop) repo and the accompanying [webinar](https://www.cbioportal.org/tutorials#webinar-5).

# Contributing 👩‍🍳
We would love your help to add more recipes to this codebook! See the contributing guide here: [CONTRIBUTING.md](./CONTRIBUTING.md)

# Gene Mutation Co-Occurence Network
The tool allows the user to provide tabular data of patients/samples with genes as binary attributes (for instance, MSK-Impact). Then, the software can be used to study either the entire cohort of patients/samples or specific tumor types. The software also takes user input for a similarity metric to use in order to construct the network: the current options are negative log(fdr adjusted p-value) of Chi-Squared Test of Independence, and a proportion metric defined as: number of instances two genes are mutated together/number of instances at least one gene is mutated.
An adjacency matrix is constructed, filtered using a high threshold (only the top one percentile of edge weights are retained), and passed into NetworkX to obtain an XML file. The resulting XML file can be used by the user in softwares such as Cytoscape to visualize the network and communities of genes that may offer insightful and novel gene combinations involved in certain tumor types.
