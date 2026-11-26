# LSABD Group Project
**Dataset 2: RNA-seq data from post-mortem brain tissue in psychiatric disorders**
This repository contains a Jupyter notebook, a Python requirements file, and the instructions needed to run it.


## 1. Initial project layout
```text
LSABD_dataset2_project/
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


## 2. Create a Python 3.11 environment (Fedora Linux / KDE) (Has to be done one time only)
### Linux redhat (Fedora):

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

In your IDE (e.g. VSCodium or jupyter lab), open `notebook.ipynb` and select the kernel named **Python 3.11 (LSABD Dataset 2)**. Verify the kernel by running the first code cell. The notebook also prints the active interpreter path.


### Windows alternative
Install Python 3.11 from the official python website (Don't forget to check `ADD TO PATH`), then from PowerShell or CMD in the project directory run:

```PowerShell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python --version
python -m pip install --upgrade pip wheel
python -m pip install -r requirements.txt
python -m ipykernel install --user --name lsabd_dataset2 --display-name "Python 3.11 (LSABD Dataset 2)"
python -m jupyter lab
```

## 3. HOW TO OPEN AND PREPARE TO RUN
### Linux
*Will be added later*

### Windows 11 (Ny-Aina)
1. Open the folder of the group project.
2. Right-click in the folder and choose 'Open in terminal'
3. run the following to activate the previously made environment + open jupyter
```PowerShell
.\.venv\Scripts\Activate.ps1
python -m jupyter lab
```
4. **Do not forget to choose the custom kernel (LSABD Dataset2) in jupyter in the upper right corner**
5. Now you can run the notebook from top to bottom. Do not skip the data validation cells.

### Windows 10 (Louise)
1. Open the folder of the group project.
2. In file explorer copy the path to the folder (link at the top)
3. Open CMD (EN: command-line / NL:opdrachtprompt)
4. Type: cd [and paste here the path here that you copied earlier]
5. Press enter
6. Run the following to activate the previously made environment + open jupyter:
```PowerShell
.\.venv\Scripts\Activate.ps1
python -m jupyter lab
```
7. **Don't forget to choose the custom kernel (LSABD Dataset2) in jupyter in the upper right corner**
8. Now you can run the notebook from top to bottom. Do not skip the data validation cells.

### MacOS
No group member used MacOS so not included.


## 4. Sources used
1. LSABD Group Project Introduction (2026-2027) + Given dataset 2.
2. LSABD Group Project Assessment Rubric (2026-2027)
3. Ramaker RC et al. (2017). *Post-mortem molecular profiling of three psychiatric disorders*. Genome Medicine 9:72. https://doi.org/10.1186/s13073-017-0458-5
4. PyDESeq2 0.5.4 documentation: https://pydeseq2.readthedocs.io/en/v0.5.4/
5. NCBI Gene: EGR1, Gene ID 1958; Ensembl gene ID ENSG00000120738. https://www.ncbi.nlm.nih.gov/gene/1958/
