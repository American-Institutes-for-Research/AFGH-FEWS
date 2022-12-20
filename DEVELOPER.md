## Setting up a development virtual environment

1. Create a conda environment for the project:
```bash
conda create --name <project name> python=3.8
```
2. Activate the environment:
```bash
conda activate <project name>
```
3. Install non-conda requirements:
```bash
pip install --requirement requirements/base.pip
```
4. Install the base requirements for the project (enable the conda-forge channel to ensure we can install GDAL, etc.):
```bash
conda install --channel defaults --channel conda-forge --file requirements/base.conda
```
5. Create environment file
```bash
cp -v env.example .env
```
Open the `.env` and add valid values for `LUIGI_CKAN_USERNAME`,`LUIGI_CKAN_PASSWORD` and `LUIGI_CKAN_ADDRESS`