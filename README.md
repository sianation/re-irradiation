# Prostate re-irradiation: clinical and dosimetric analysis

An R Markdown pipeline describing a cohort of patients with prostate cancer who had re-irradiation for local recurrence after previous radical treatment.

## What the script does

`Reirradiation_public.Rmd` covers:

1. **Data cleaning.** Tidies PSA values and TNM staging (at diagnosis and at recurrence), standardises yes/no fields, and keeps only patients with a recorded salvage treatment completion date. Reports how many missing values each conversion introduces.
2. **Patient and disease characteristics.** Medians, interquartile ranges and frequency tables for the first radical treatment and at recurrence: Gleason score, stage, PSA, ADT use, ECOG, IPSS, imaging (mpMRI and PET) and biopsy. Each variable's missing data is reported too.
3. **First treatment summary.** Dose and fractionation by first treatment modality.
4. **Re-irradiation treatment.** Dose prescriptions, single- versus multi-dose schedules, and the rectum, urethra and bladder dose constraints used.
5. **Toxicity.** Worst genitourinary (GU) and gastrointestinal (GI) CTCAE grades at 3, 6 and 12 months, with missing data counts.
6. **Outcomes and follow-up.** Failure-free status at last follow-up, and median (IQR) follow-up time and time to failure after re-irradiation.

Tables are exported to Word using `officer` and `flextable`.

## Requirements

R (4.x) with `tidyverse`, `survival`, `survminer`, `ggsurvfit`, `tidycmprsk`, `gtsummary`, `officer`, `flextable`, `readxl` and `patchwork`.

## Data

**No patient data is included in this repository.** Load your own anonymised data frame as `reirr` before running the script.

## Author

Dr Sian Cooper, clinical oncologist and radiotherapy researcher. See also [What Patients Say](https://whatpatientssay.co.uk), a patient-facing summary of five-year outcomes after prostate radiotherapy.
