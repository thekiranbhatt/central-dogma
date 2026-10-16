# Central Dogma of Molecular Biology

This is a simple project to demonstrate **coding DNA → mRNA → protein** using the human **DECR1** coding sequence retrieved from NCBI Nucleotide on jupyter notebook.

## Project contents

```text
central-dogma-project/
├── README.md
├── central_dogma.ipynb
├── requirements.txt
└── .gitignore
```

## Project Workflow

1. Searches NCBI Nucleotide for human `DECR1` mRNA records.
2. Extracts an annotated coding sequence (CDS), respecting strand orientation.
3. Transcribes coding DNA into mRNA.
4. Translates mRNA into a protein sequence.
5. Checks sequence lengths and confirms that DNA and RNA translations agree.

## Requirements

- Python 3.9 or later
- Internet access to retrieve sequence records from NCBI

## Setup

Create and activate a virtual environment (recommended):

```bash
python -m venv .venv
```

Windows:

```powershell
.venv\Scripts\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `central_dogma.ipynb` and run the cells from top to bottom.

## Before running

In the setup cell, replace `your.email@example.com` with your valid email address. NCBI requests a contact email for Entrez use.

## Biology notes

- An annotated CDS is used instead of arbitrary genomic DNA because genomic regions may contain introns and non-coding sequence.
- The CDS feature is extracted in its annotated orientation, including reverse-strand handling where needed.
- RNA is transcribed from coding DNA. Reverse-complementing RNA is not a step in the central dogma.
- Padding the sequence with `N` bases is unnecessary for an annotated CDS and can affect translation.
- A terminal `*` in the translated output represents a stop codon.

NCBI records and search results may change over time. Internet access is required.
