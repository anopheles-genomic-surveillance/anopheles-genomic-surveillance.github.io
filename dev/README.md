# How to create a new Conda environment on DataLab

You should do this on DataLab, which is a Linux machine, with at least 6 GB RAM.

Get a local clone of the GitHub repo, e.g.:
```bash
git clone git@github.com:anopheles-genomic-surveillance/anopheles-genomic-surveillance.github.io.git
```

If the latest pinned environment file isn't in the `dev` directory, then you can copy it from DataLab's Conda environment manager:
- https://datalab-bespin.malariagen.net/conda-store/

If you have to create it, name the latest pinned environment file accordingly and store it in the `dev` directory, e.g.

```bash
cd anopheles-genomic-surveillance.github.io
mkdir dev
cd dev
nano training-nb-maintenance-mgen-7.11.0-pinned-DataLab.yaml
```

Make a copy of the latest pinned environment file and give the new file an appropriate name, e.g.
```bash
cp training-nb-maintenance-mgen-7.11.0-pinned-DataLab.yaml training-nb-maintenance-mgen-15.0.1.yaml
```

Modify the new environment file accordingly, e.g.
```bash
nano training-nb-maintenance-mgen-15.0.1.yaml
```
```yaml
- python=3.11.11
```
```yaml
- pip:
  - malariagen-data>=15.0.1
```

Remove the `name`, `description` and `prefix` settings.

Remove the build strings that appear after the version pins, e.g.
```yaml
  - python==3.11.11=he550d4f_0_cpython
```
...should be:
```yaml
  - python==3.11.11
```

If you're using Miniconda instead of Miniforge, make sure that the "defaults" channel won't be added automatically, e.g.:
```bash
conda config --show channels
conda config --remove channels defaults
conda config --show channels
```

Create a new Conda environment using the new modified environment file:
```bash
conda env create --name training-nb-maintenance-mgen-15.0.1 --file training-nb-maintenance-mgen-15.0.1.yaml
```

Creating the new Conda environment usually takes a few minutes to collect all the relevant package metadata, solve the environment, download all the packages and install the dependencies.

If the machine runs out of memory, it often just exits to the command prompt rather than giving an error message. In which case, you will probably need a machine with more RAM.

Activate the new Conda environment and check the package versions are as expected, e.g.
```bash
conda activate training-nb-maintenance-mgen-15.0.1
conda list
```

Export the activated Conda environment to get a fully-pinned environment file:
```bash
conda env export > training-nb-maintenance-mgen-15.0.1-pinned-DataLab.yaml
```

Change the `prefix` setting to `null`, instead of your local path:
```
nano training-nb-maintenance-mgen-15.0.1-pinned-DataLab.yaml
```

Transfer the contents of the new pinned environment to DataLab, under the `developer` namespace, using DataLab's Conda environment manager:

- https://datalab-bespin.malariagen.net/conda-store/

**Note:** DataLab's Conda environment manager is currently a bit glitchy, so might still show the environment's build process as queued, even when the new environment appears to be functional.

Test the new environment using the `test_env.ipynb` Notebook in this directory and Notebooks from Workshops 1 and 2.

Commit the new pinned environment file and any other changes to the GitHub repository, and ask for a review.
