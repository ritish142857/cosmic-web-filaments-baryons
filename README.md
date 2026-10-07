# cosmic-web-filaments-baryons

Analysis code and source data for studying the distribution of cool baryons in low-redshift cosmic-web filaments.

Paper: Cosmic-web Filaments Harbor the Majority of the Cool Baryons in the Low-redshift Universe

Description of the data and file structure

This repository contains the source data and analysis code associated with the study of the diffuse baryon reservoir in the low-redshift cosmic web. The datasets provide the cluster–quasar sample used to identify cosmic-web filaments and investigate the spatial association between Lyα absorption and filamentary structures.

The dataset includes the final sample of 318 galaxy cluster–background quasar pairs, together with measurements of the Lyα absorption covering fraction as a function of projected filament-centric distance and other quantities used in the analysis.

## Files included

### 1. Cluster–quasar sample

**File:** Cluster_field_sample.csv

This file contains the final sample of 318 galaxy cluster–background quasar pairs used in the analysis.

Columns:

* #qso_name — Name/identifier of the background quasar.

* cluster_name — Identifier of the galaxy cluster.

* ra_cls — Right ascension of the galaxy cluster, in degrees.

* dec_cls — Declination of the galaxy cluster, in degrees.

* z_cls — Redshift of the galaxy cluster.

* ra_q — Right ascension of the background quasar, in degrees.

* dec_q — Declination of the background quasar, in degrees.

* r_phy — Projected physical separation between the galaxy cluster and the background-quasar sightline, in Mpc.

### 2. Differential covering fractions

**File:** Table_S1_covering_fraction_DFil_EW03.csv

This file contains the differential covering fractions of Lyα absorbers for equivalent-width thresholds of \(W_{\rm th}=0.3\) Å in different projected filament-centric distance intervals.

Columns:

* D_Fil_Mpc — Projected filament-centric distance range, in physical Mpc.

* fc_Lya_EW — Lyα covering fraction for \(W_{\rm th}=0.3\) Å.

* upper_1sigma_EW — Upper 1σ uncertainty.

* lower_1sigma_EW — Lower 1σ uncertainty.

The row labeled IGM gives the covering fraction expected from randomly distributed Lyα absorbers at similar redshifts.

### 3. Baryon-budget calculation

**File:** Table_S2_baryon_budget.csv

This file contains the baryon-budget estimates for cosmic-web filaments traced by Lyα absorption for four ultraviolet-background (UVB) models.

Columns:

- UVB — Adopted ultraviolet-background model.

- mean_f_HI — Mean neutral-hydrogen fraction, \(\langle f_{\rm HI}\rangle_{\Delta}\).

- Omega_HI_Fil — Neutral-hydrogen density parameter, \(\Omega(\mathrm{HI})_{\rm Fil}\).

- Omega_H_Fil — Total hydrogen density parameter, \(\Omega(\mathrm{H})_{\rm Fil}\).

- Omega_b_Fil — Baryonic density parameter associated with the filaments, \(\Omega_{\rm b}(\mathrm{Fil})\).

- f_b_Fil — Fraction of the cosmic baryon budget contained in the filaments, \(f_{\rm b}(\mathrm{Fil})\).

The UVB models considered are:

- KS19 Q14 — intrinsic quasar SED power-law slope of \(-1.4\).

- KS19 Q18 — intrinsic quasar SED power-law slope of \(-1.8\).

- KS19 Q20 — intrinsic quasar SED power-law slope of \(-2.0\).

- HM05 — Haardt & Madau (2005) UVB model.

The values of \(f_{\rm b}(\mathrm{Fil})\) in square brackets represent the range resulting from the uncertainty in the assumed filament width. This uncertainty corresponds to the best-fit characteristic scale:

\[

D_0 = 3.6^{+3.0}_{-1.6}\ {\rm pMpc}.

\]

The baryonic calculation accounts for the conversion from neutral hydrogen to total hydrogen using the UVB-dependent neutral-hydrogen fraction and includes the contribution of helium.

### 4. Differential covering fractions

**File:** Table_S3_covering_fractions.csv

This file contains the differential covering fractions of Lyα absorbers for equivalent-width thresholds of \(W_{\rm th}=0.1\) Å and \(0.2\) Å in different projected filament-centric distance intervals.

Columns:

* D_Fil_Mpc — Projected filament-centric distance range, in physical Mpc.

* fc_Lya_EW_0.1_A — Lyα covering fraction for \(W_{\rm th}=0.1\) Å.

* upper_1sigma_EW_0.1_A — Upper 1σ uncertainty.

* lower_1sigma_EW_0.1_A — Lower 1σ uncertainty.

* fc_Lya_EW_0.2_A — Lyα covering fraction for \(W_{\rm th}=0.2\) Å.

* upper_1sigma_EW_0.2_A — Upper 1σ uncertainty.

* lower_1sigma_EW_0.2_A — Lower 1σ uncertainty.

The row labeled IGM gives the covering fraction expected from randomly distributed Lyα absorbers at similar redshifts.

### 5. Cumulative covering fractions

**File:** Table_S4_cumulative_covering_fractions.csv

This file contains the cumulative covering fractions of Lyα absorbers as a function of projected filament-centric distance for equivalent-width thresholds of \(W_{\rm th}=0.1\) Å and \(0.3\) Å.

Columns:

* D_Fil_Mpc — Maximum projected filament-centric distance, in physical Mpc. Values beginning with <= indicate cumulative measurements within that distance.

* fc_Lya_EW_0.1_A — Cumulative Lyα covering fraction for \(W_{\rm th}=0.1\) Å.

* upper_1sigma_EW_0.1_A — Upper 1σ uncertainty.

* lower_1sigma_EW_0.1_A — Lower 1σ uncertainty.

* fc_Lya_EW_0.3_A — Cumulative Lyα covering fraction for \(W_{\rm th}=0.3\) Å.

* upper_1sigma_EW_0.3_A — Upper 1σ uncertainty.

* lower_1sigma_EW_0.3_A — Lower 1σ uncertainty.

The row labeled IGM gives the covering fraction expected from randomly distributed Lyα absorbers at similar redshifts.

## Units

* Right ascension and declination: degrees

* Redshift: dimensionless

* Projected physical separation (r_phy): Mpc

* Filament-centric distance (D_Fil_Mpc): physical Mpc

* Equivalent width: Å

* Covering fraction: dimensionless

## Uncertainties

The uncertainties on the covering fractions represent the 1σ Wilson score confidence intervals.

For example,

$$

f_c = 0.56^{+0.09}_{-0.09}

$$

corresponds to a covering fraction of 0.56 with an upper uncertainty of 0.09 and a lower uncertainty of 0.09.

## IGM reference covering fraction

The IGM rows provide the covering fraction expected from randomly distributed Lyα absorbers at similar redshifts. These values are used as the reference expectation when assessing the enhancement of Lyα absorption associated with cosmic-web filaments.

## Data selection and sample

The parent sample consists of galaxy clusters with at least one background quasar sightline within a projected distance of \(10R_{500}\). The final analysis sample contains 318 unique cluster–quasar pairs after applying the selection criteria described in the manuscript.

The galaxy distribution around each cluster was used to identify cosmic-web filaments. The resulting filamentary structures were then used to calculate the projected filament-centric distance of Lyα absorbers.

## Relation to the manuscript

These datasets contain the numerical data products used in the manuscript:

**“Cosmic-web Filaments Harbor the Majority of the Cool Baryons in the Low-redshift Universe”**

The cluster–quasar catalogue provides the sightlines used in the analysis, while the covering-fraction tables provide the measurements used to quantify the association between Lyα absorbers and cosmic-web filaments.

## Data format

All datasets are provided in CSV (comma-separated values) format. They can be read using standard spreadsheet software or programming languages such as Python, R, or IDL.

## Citation

If you use these data, please cite the associated publication:

**Kumar et al., “Cosmic-web Filaments Harbor the Majority of the Cool Baryons in the Low-redshift Universe.”**

Please use the final bibliographic information and DOI of the published article when citing these data.

## Contact

For questions regarding the dataset, please contact the corresponding author of the associated publication.

Code/Software

The data are provided in standard CSV format and can be viewed using commonly available spreadsheet or text-editing software. The analysis was performed using Python 3 and standard scientific Python packages, including NumPy, Pandas, SciPy, Astropy, and Matplotlib. Cosmic-web filaments were identified using the publicly available DisPerSE code. The complete Python code used for the main analysis and to generate the results presented in the manuscript is provided in central_result_codes.pdf.
