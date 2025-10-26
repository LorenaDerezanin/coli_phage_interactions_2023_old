# coli_phage_interactions_2023
Git repository containing the code and genomics data published in the article "Predicting phage-bacteria interactions at the strain level from genomes"

## Getting Started
This repository uses `micromamba` to manage environments.
You can install it using the official docs
[here](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html).

Then create and activate the `micromamba` environment using the following commands:
```bash
micromamba create -f environment.yml
micromamba activate phage_env
```

To enable running Jupyter notebooks using this environment, create
a dedicated Jupyter kernel for it:
```bash
python -m ipykernel install --user --name phage_env --display-name phage_env
```

Now when you run notebooks in `jupyter lab`, make sure to select the `phage_env`
kernel.

## Research Notes
Predicted cocktails are benchmarked against a "baseline" and a "generic" cocktail.
From the paper:
> To evaluate the performance of our algorithm, we compared the performance of
> the tailored and generic cocktails with an uninformed baseline cocktail.
> The latter corresponds to the most-covering triplet of phages, that is,
> the cocktail of three phages which together lyse the largest number of
> bacteria in the original interaction matrix. This baseline cocktail yielded
> productive lysis on 63% of the original Picard collection.

> First, some cocktails (n = 15, recommended to 24 test bacteria) contained
> phages recommended at early stages of the pipeline (denoted as ‘tailored’ 
> in the rest of the text), while the rest of the cocktails (n = 3, recommended
> to 76 bacteria) were recommended at late stages of the pipeline (denoted as
> ‘generic’ in the rest of the text) (Fig. 6c).

@zoltanmaric's interpretation: 
- **Baseline**: The single cocktail of 3 phages that together lyse the largest
  number of bacteria (63% of the original Picard collection)
- **Generic**: The top 3 most recommended cocktails by the recommendation pipeline
  built in this paper.
