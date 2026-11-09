# Figure 1: Potts model scan of double mutant cycles 

Code and data for Figure 1 (panels B-D) in `Epistasis Manuscript`.
Panel A (Potts model schematic) is not included here.

Run the notebooks from inside `notebooks/` .

```
epistasis_HIV-1_figure_1/
|-- notebooks/
|   |-- histogram_main.ipynb   # middle panels: ddE histograms for PR, RT, IN
|   |-- Circos_main.ipynb      # side panels: synergistic / antagonistic circos plots
|-- data/
|   |-- {IN,PR,RT}/
|   |   |-- kn.her2.all                # Potts ddE for all double mutants
|   |   |-- {in,pr,rt}.reduce4.redux   # reduced-alphabet dictionary
|   |   |-- top_5_DRM.txt / bottom_5_DRM.txt    # dotted lines on histograms
|   |   |-- top_20_DRM.txt / bottom_20_DRM.txt  # highlighted chords in circos (Table S1)
|   |-- dde/
|       |-- PR.txt   # Potts ddE for all PR double mutants
|       |-- RT.txt   # Potts ddE for all RT double mutants
|       |-- IN.txt   # Potts ddE for all IN double mutants
|-- output/                    # {IN,PR,RT}_histogram.png, {IN,PR,RT}_{syn,antag}.png
|-- utilities/
    |-- functions.py
    |-- circ.py
```

## data/dde

One tab-separated file per protein, with a header line and one row per double mutant:

| Column | Description |
| --- | --- |
| double_mutant | double mutant in the reduced alphabet, e.g. `B1A-C2A` |
| ddE | Potts ddE, copied unchanged from column 2 of `kn.her2.all` |

```
double_mutant	ddE
B1A-C2A	7.2326283
B1A-C2B	2.9241257
```

| File | Double mutants |
| --- | --- |
| PR.txt | 43,659 |
| RT.txt | 158,202 |
| IN.txt | 310,077 |

Negative values use the plain ASCII hyphen-minus `-` (U+002D).

Requirements: numpy, pandas, matplotlib, pycirclize, tqdm, pillow.
