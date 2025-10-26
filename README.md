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
