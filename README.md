# Figure 1: Potts model scan of double mutant cycles 

Code and data for Figure 1 (panels B-D) in `Epistasis Manuscript`.
Panel A (Potts model schematic) is not included here.

Run the notebooks from inside `notebooks/` .

```
epistasis_HIV-1_figure_1/
├── notebooks/
│   ├── histogram_main.ipynb   # middle panels: ΔΔE histograms for PR, RT, IN
│   └── Circos_main.ipynb      # side panels: synergistic / antagonistic circos plots
├── data/{IN,PR,RT}/
│   ├── kn.her2.all                # Potts ΔΔE for all double mutants
│   ├── {in,pr,rt}.reduce4.redux   # reduced-alphabet dictionary
│   ├── top_5_DRM.txt / bottom_5_DRM.txt    # dotted lines on histograms
│   └── top_20_DRM.txt / bottom_20_DRM.txt  # highlighted chords in circos (Table S1)
├── output/                    # {IN,PR,RT}_histogram.png, {IN,PR,RT}_{syn,antag}.png
└── utilities/
    ├── functions.py
    └── circ.py
```

Requirements: numpy, pandas, matplotlib, pycirclize, tqdm, pillow.
