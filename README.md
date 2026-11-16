# Supplemental Material: zone-folding origin of the CuAu/chalcopyrite Raman splitting

Interactive Supplemental Material to the article *Zone-folding origin of the CuAu/chalcopyrite Raman splitting in
zinc-blende- and wurtzite-derived ternary semiconductors*.

## Web applications

Both pages run directly in the browser:

- **[Open the Zone-Folding Raman Explorer](https://ljwirtz.github.io/raman_chalc_cuau/zone_folding_explorer.html)**
- **[Open the supercell viewer](https://ljwirtz.github.io/raman_chalc_cuau/supercell_viewer.html)**

They are self-contained HTML files, so they can also be downloaded and opened locally in any web browser (no installation, no server). Clicking an `.html` file in the file list above shows its source code, not the page.

| File | Content |
|---|---|
| `zone_folding_explorer.html` | Zone-Folding Raman Explorer: sliders move the Raman tensors, masses and force constants from the parent (ZnSe, ZnS) to the ternary compound (CuInSe₂, CuInS₂) in the CuAu (CA) and chalcopyrite (CH) cells, following the Raman spectrum along the way. HSE06 phonons and Raman tensors (FHI-aims + phonopy). |
| `supercell_viewer.html` | The CA and CH supercells, their Brillouin zones and k-paths, and the HSE06 phonon dispersions. Clicking any point of a dispersion animates that phonon mode and links to the same mode in the phonon website. |

## Phonon dispersions with eigenvectors

The files in `phonons/` contain the HSE06 phonon dispersions shown in the supercell viewer, with frequencies and
eigenvectors (displacement patterns) at every q point, in the JSON format of the
[phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html) by H. Miranda.
The links below open each file there; click on any branch to animate the mode.

| File | Dispersion | Link |
|---|---|---|
| `phonons/ZnSe_prim.json` | ZnSe, zinc-blende primitive cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/ZnSe_prim.json) |
| `phonons/ZnS_prim.json` | ZnS, zinc-blende primitive cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/ZnS_prim.json) |
| `phonons/CuInSe2_CH.json` | CuInSe2, chalcopyrite (CH) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/CuInSe2_CH.json) |
| `phonons/ZnSe_CH.json` | ZnSe, chalcopyrite (CH) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/ZnSe_CH.json) |
| `phonons/CuInSe2_Au.json` | CuInSe2, CuAu (CA) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/CuInSe2_Au.json) |
| `phonons/ZnSe_Au.json` | ZnSe, CuAu (CA) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/ZnSe_Au.json) |
| `phonons/CuInS2_CH.json` | CuInS2, chalcopyrite (CH) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/CuInS2_CH.json) |
| `phonons/ZnS_CH.json` | ZnS, chalcopyrite (CH) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/ZnS_CH.json) |
| `phonons/CuInS2_Au.json` | CuInS2, CuAu (CA) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/CuInS2_Au.json) |
| `phonons/ZnS_Au.json` | ZnS, CuAu (CA) cell | [open in the phonon website](https://henriquemiranda.github.io/phononwebsite/phonon.html?json=https://raw.githubusercontent.com/ljwirtz/raman_chalc_cuau/main/phonons/ZnS_Au.json) |

Details: force constants from FHI-aims + phonopy (HSE06), interpolated with `matdyn.x` (Quantum ESPRESSO); the LO–TO
splitting uses the HSE06 Born effective charges and the experimental high-frequency dielectric constant. Each Γ point
of a path is computed slightly off Γ (1e-4 · 2π/a) along its own segment, so that each side of Γ carries the LO–TO
limit of its own direction. The field `marked_modes` lists the modes marked with circles in the dispersions of the
supercell viewer: the anion-only modes at X and W of the parents, which fold onto the A₁ Raman modes of the CA and CH
cells, and the A₁ Raman modes themselves.

## Licence

The contents of this repository are licensed under the
[Creative Commons Attribution 4.0 International licence (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/);
see `LICENSE`. If you use these data or tools, please cite the article above.
