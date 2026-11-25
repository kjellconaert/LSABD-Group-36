# LSABD Group Project
**Dataset 2: RNA-seq data from post-mortem brain tissue in psychiatric disorders**
This repository contains a Jupyter notebook, a Python requirements file, and the instructions needed to run it.


## 1. Project layout
```text
LSABD_Part1/
├── data/
│   ├── GSE80655_counts.csv
│   └── GSE80655_metadata.csv
├── results/
│   ├── figures/
│   ├── processed/
│   └── tables/
├── notebook.ipynb
├── requirements.txt
└── README.md
```

The two supplied CSV files are included in `data/`. The PDFs do not need to be in this directory; they are referenced in the notebook's methodology notes.


## 2. Create a Python 3.11 environment (Fedora Linux / KDE)
The notebook checks that it is running with Python 3.11. On Fedora, install the versioned interpreter without changing the system `python3`:

```bash
sudo dnf install python3.11
python3.11 --version
```

Create and activate a project-specific virtual environment from this directory:

```bash
python3.11 -m venv .venv
source .venv/bin/activate
python --version
python -m pip install --upgrade pip wheel
python -m pip install -r requirements.txt
python -m ipykernel install --user --name lsabd_dataset2 --display-name "Python 3.11 (LSABD Dataset 2)"
```

Start JupyterLab from the activated environment:

```bash
python -m jupyter lab
```

In your IDE (e.g. VSCodium), open `notebook.ipynb` and select the kernel named **Python 3.11 (LSABD Dataset 2)**. Verify the kernel by running the first code cell. The notebook also prints the active interpreter path.


### Windows alternative
Install Python 3.11, then from PowerShell in the project directory run:

```PowerShell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python --version
python -m pip install --upgrade pip wheel
python -m pip install -r requirements.txt
python -m ipykernel install --user --name lsabd_dataset2 --display-name "Python 3.11 (LSABD Dataset 2)"
python -m jupyter lab
```

## 3. Run the notebook
Run the notebook from top to bottom. Do not skip the data validation cells.


## 4. Sources used
1. LSABD Group Project Introduction (2026-2027) + Given dataset 2.
2. LSABD Group Project Assessment Rubric (2026-2027)
3. Ramaker RC et al. (2017). *Post-mortem molecular profiling of three psychiatric disorders*. Genome Medicine 9:72. https://doi.org/10.1186/s13073-017-0458-5
4. PyDESeq2 0.5.4 documentation: https://pydeseq2.readthedocs.io/en/v0.5.4/
5. NCBI Gene: EGR1, Gene ID 1958; Ensembl gene ID ENSG00000120738. https://www.ncbi.nlm.nih.gov/gene/1958/
