# Appendix: source tables

### Table: basedata.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| p_id | int | List truncated... | Already anonymised.  Patient id unique in basedata. |
| psa | real | 5.1 | Measuring prostate-specific antigen.  |
| prostatic_vol | real | 40 | Prostate volume measured in ml. |
| dre | varchar | T1c | Digital rectal examination. |
| num_cores | int | 12 | Number of core biopsies. |
| num_cores_pc | int | 1 |  Number of core biopsies that contained prostate cancer. |
| asa | int | 0 | Do not map this variable (empty and not in the current form).  In follow up this contains the Charlson score (separate charlson variable in basedata). |
| log2psa | real | 2.26303 | Derived variable from psa.  Do not map. |
| gleason1 | int | 3 | Gleason primary grade.   |
| gleason2 | int | 3 | Gleason secondary grade. |
| gleason_sum | int | 6 | Gleason score (gleason1 + gleason2).  Do not map, info captured in more detail from gleason1 and 2. Value  0 should not be possible (prostate cancer is inclusion criterum). |
| free_psa | real | 0 | Free-PSA test measures the percentage of unbound PSA. |
| pro_psa | int |  | Do not map, barely filled in, same in follow-up. |
| phi | int |  |  |
| charlson | int | 0 | Charlson Comorbidity Index (CCI) predicts the ten-year mortality for a patient who may have a range of comorbid conditions.   |
| tnm | int | 1992 | TNM version from 1992 (not 1998 or 2002)  Do not map, not relevant, always the same. |
| method_detection | varchar | Screen-detected | Clinically =  by docter during hosptial visit due to complaints,  screen-detected = by routine check without complaints. |
| length | int | 0 | Length of patient (in cm). |
| weight | int | 0 | Weight of patient (in kg). |
| num_cores2 | int | 0 | Repeated biopsy, if first was less than 8 cores. Map the same as num_cores. |
| num_cores_pc2 | int | 0 | Repeated biopsy, if first was less than 8 cores. Map the same as num_cores_pc. |
| gleason1_2 | int | 0 | Repeated biopsy, if first was less than 8 cores.  Map the same as gleason_1. |
| gleason2_2 | int | 0 | Repeated biopsy, if first was less than 8 cores.  Map together with gleason1_2. |
| no_co_morbidity | int | 1 | Other comorbidities.  Do not map. Should always be true (no comorbitidy), if other, it is an error as patient should then not be included. |
| active_visit | int | 1 | Bij basedata altijd active (=1).  Do not map. |
| biopt_prob_type | int | 0 | Antibioticum given (profylaxe).  0 - data not provided (empty),  1 - no antibioticum used (capture, to distinguish from missing),  2 - yes, fluorquinolones,  3 - yes, tmp smx,  4 - yes, other.   |
| biopt_infection | int | 0 | Infection occurred after biopsy. 0 - not provided (does not mean no complications occurred),  1 - yes 2 - no |
| biopt_inf_urine_culture | int | 0 | Urine culture measured.  0 - not provided or not measured (empty)  1 - positive (bacterium is cultured, is an infection), 2 - negative (no bacterium cultered, not an infection) |
| biopt_inf_urine_bacterium | int |  | Type of urine bacterium measured. 0 - not filled in, 1 - *E.coli*,  2 - *pseudomonas*, 3 - *Enterococci*, 4 - *proteus*, 5 - *Staphylococci*, 6 - *Klebsiella*, 7 - other enterobacteria, 8 - other |
| biopt_inf_unrine_resistant | varchar |  | To which antibioticum is the urine bacteria resistant.  0 - not filled in,  1 - Fluoroquinolones, 2 - Trimethoprim-sulfonamide (TMP-SMX) combination, 3 - Cephalosporin (group 1 or 2), 4 - Cephalosporin (group >=3), 5 - Carbapenems, 6 - Penicillins (without B-lactam),  7 - Aminoglycosides, 8 - Nitrofuran, 9 - other. |
| biopt_inf_antibiotic_therapy | int | 0 | If antibiotic therapy is given.  0 - not filled in, 1 - yes, 2 - no. |
| biopt_inf_antibiotic_type | int |  | What kind of antibiotic is given. 0 - not filled in,  1 - Fluoroquinolones, 2 - Trimethoprim-sulfonamide (TMP-SMX) combination, 3 - Cephalosporin (group 1 or 2), 4 - Cephalosporin (group >=3), 5 - Carbapenems, 6 - Penicillins (without B-lactam), 7 - Penicillins (with B-lactam), 8 - Aminoglycosides, 9 - Nitrofuran, 10 - other. |
| biopt_inf_hospitalisation | int | 0 | Hospitalisation due to bioptic infection. 0 - not filled in, 1 - yes, 2 - no. |
| biopt_inf_hospitalisation_days | int | 0 | Days in hospital. |
| biopt_inf_outcome | int | 0 | Cured or death.  0 = not given (empty)  1 = cured  2 = death (not in baseline). |
| biopt_hematuria | int | 0 | Hematuria (red blood cells in urine), more than 3 days. 0 - not filled in,  1 - yes  2 - no. |
| biopt_hemospermia | int | 0 | Hemospermia. 0 - not filled in,  1 - yes  2 - no. |
| biopt_pain | int | 0 | Pain after biopsy. 0 - not filled in,  1 - yes  2 - no. |
| biopt_route | int | 0 | 0 - not given,  1 - transrectal  2 - transperineal. |
| biopt_max_cancer_score_lenght | int | 0 | Number of millimeters on a prostate cancer biopsy consisting of prostate cancer (largest part). |
| mri_included | int | 0 | Whether patient has been selected for MRI side study. Do not map. |
| bonescan | varchar |  | Old variable, do not map. |
| mri_taken.0 | int | 0 | MRI made at baseline. Result MRI does not always have to be given, so save separately.  |
| mri_lesions.0 | int | 0 | Abnormalities detected on MRI. |
| mri_suspected_number.0 | int | 0 | Number of suspected abnormalities/lesions on MRI. |
| mri_pirads_1.0 | int | 0 | The PIRADS score is given for each suspected lesion (maximum of 3). |
| mri_largest_dia_1.0 | int | 0 | The largest diameter in mm of lesion 1. |
| mri_location_1.0 | int | 0 | Location of lesion 1 in the prostate. |
| mri_location_free_1.0 | varchar |  | Text field for extra information for mri_location_1.0 |
| mri_pirads_2.0 | int | 0 | The PIRADS score is given for each suspected lesion (maximum of 3). |
| mri_largest_dia_2.0 | int | 0 | The largest diameter in mm of lesion 2.  |
| mri_location_2.0 | int | 0 | Location of lesion 2 in the prostate. |
| mri_location_free_2.0 | varchar |  | Text field for extra information of mri_location_2.0 |
| mri_pirads_3.0 | int | 0 | The PIRADS score is given for each suspected lesion (maximum of 3). |
| mri_largest_dia_3.0 | int | 0 | The largest diameter in mm of lesion 3. |
| mri_location_3.0 | int | 0 | Location of lesion 3 in the prostate.  |
| mri_location_free_3.0 | varchar |  | Text field for extra information of mri_location_3.0 |
| mri_progrssion_lesions.0 | int |  | Whether there is change compared to the previous MRI, about lesion 1. 0 - empty (not given),  use PRECISE recommendations (make stages for each score). |
| mri_targeted_biopsy.0 | int | 0 | Targeted biopsies. 0 - empty, 1 - yes, 2 - no |
| mri_targeted_cores.0 | int | 0 | Number of cores with prostate cancer from targeted biopsies taken.  Only use when targeted biopsys - yes (0 can mean both not given and no pc cores found). |
| mri_targeted_taken.0 | int | 0 | Number of cores taken from the abnormalities seen on MRI (targeted).  |
| mri_targeted_gleason1.0 | int | 0 | See gleason_score, map to grade group. |
| mri_targeted_gleason1.0.1 | int | 0 | See gleason_score, map to grade group. |
| mri_lesion_positive.0 | int |  | Number of lesions  that are confirmed by biopt as prostate cancer. 0 can mean both not recorded and no positive found. |
| mri_method_used.0 | int | 0 | Combine with mri_targeted_biopsy.0, if done also include this method. |
| mri_prostate_volume.0 | int |  | Not measured by MRI, but manually entered based on MRI in ml. |
| mri_prostate_volume_method.0 | int |  | Combine with mri_prostate_volume (do not map?). |
| age_diagnosis | real | 66.92 | Age at diagnosis (observation).  Include to be complete. |
| year_diagnosis | int | 2015 |  |

### Table: fulong.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| p_id | int | 3064 | Patient id |
| time | int | 1 | Visit number |
| psa_fu | real | 5.8 | Measuring prostate-specific antigen |
| dre_fu | varchar |  |  Digital rectal examination  If empty, this visit only measured psa (do not capture). |
| dre_fu_recode | int |  | Administrative. Use actual dre_fu. |
| num_cores_biop_fu | int | 0 | Number of core biopsies. |
| num_cores_pc_fu | int | 0 |  Number of core biopsies that contained prostate cancer.  |
| asa_fu | int | 0 | Charlson score (see charlson variable in basedata). |
| log2psa_fu | real | 2.58496 | Log2 of the PSA value. |
| psadt | real | -0.8 | PSA doubling time |
| gleason1_fu | int | 0 | Gleason primary grade |
| gleason2_fu | int | 0 | Gleason secondary grade |
| gleason_sum_fu | int | 0 | Gleason score (gleason1 + gleason2). Do not map, info captured in more detail from gleason1 and 2.  |
| slope | real | 0 | Used to calculate psadt (doubling time)  Do not map, captured by psadt. |
| free_psa_fu | real | 0 | Free-PSA test measures the percentage of unbound PSA. |
| pro_psa_fu | int |  | Do not map, given for just one person. |
| phi_fu | int |  |  |
| visit_action | varchar | LAB | Does not always match. The actual measurements done decided by clincians.  Administrative field. |
| active_visit | int | 1 |  1 - yes, 0 - No. Do not map.  |
| biopt_prob_type_fu | int | 0 | Antibioticum given (profylaxe).  0 - data not provided (empty),  1 - no antibioticum used (capture, to distinguish from missing),  2 - yes, fluorquinolones,  3 - yes, tmp smx,  4 - yes, other. |
| biopt_infection_fu | int | 0 | Infection occurred after biopsy. 0 - not provided (does not mean no complications occurred),  1 - yes 2 - no |
| biopt_inf_urine_culture_fu | int | 0 |  Urine culture measured.  0 - not provided or not measured (empty)  1 - positive (bacterium is cultured, is an infection), 2 - negative (no bacterium cultered, not an infection) |
| biopt_inf_urine_bacterium_fu | int |  | Type of urine bacterium measured. Type of urine bacterium measured. 0 - not filled in, 1 - *E.coli*,  2 - *pseudomonas*, 3 - *Enterococci*, 4 - *proteus*, 5 - *Staphylococci*, 6 - *Klebsiella*, 7 - other enterobacteria, 8 - other. |
| biopt_inf_unrine_resistant_fu | varchar |  | To which antibioticum is the urine bacteria resistant.  0 - not filled in,  1 - Fluoroquinolones, 2 - Trimethoprim-sulfonamide (TMP-SMX) combination, 3 - Cephalosporin (group 1 or 2), 4 - Cephalosporin (group >=3), 5 - Carbapenems, 6 - Penicillins (without B-lactam),  7 - Aminoglycosides, 8 - Nitrofuran, 9 - other. |
| biopt_inf_antibiotic_therapy_fu | int | 0 |   If antibiotic therapy is given.  If antibiotic therapy is given.  0 - not filled in, 1 - yes, 2 - no. |
| biopt_inf_antibiotic_type_fu | varchar |  | What kind of antibiotic is given. 0 - not filled in,  1 - Fluoroquinolones, 2 - Trimethoprim-sulfonamide (TMP-SMX) combination, 3 - Cephalosporin (group 1 or 2), 4 - Cephalosporin (group >=3), 5 - Carbapenems, 6 - Penicillins (without B-lactam), 7 - Penicillins (with B-lactam), 8 - Aminoglycosides, 9 - Nitrofuran, 10 - other. |
| biopt_inf_hospitalisation_fu | int | 0 | Hospitalisation due to bioptic infection. 0 - not filled in, 1 - yes, 2 - no. |
| biopt_inf_hospitalisation_days_fu | int | 0 | Days in hospital. |
| biopt_inf_outcome_fu | int | 0 | Cured or death.  0 - not given (empty)  1 - cured  2 - death. |
| biopt_hematuria_fu | int | 0 | Hematuria (red blood cells in urine), more than 3 days.  0 - not filled in,   1 - yes,  2 - no. |
| biopt_hemospermia_fu | int | 0 | Hemospermia (blood in sperm). 0 - not filled in,  1 - yes, 2 - no. |
| biopt_pain_fu | int | 0 | Pain after biopsy. 0 - not filled in , 1 - yes,  2 - no. |
| biopt_route_fu | int | 0 | 0 - not given,  1 - transrectal  2 - transperineal. |
| biopt_max_cancer_score_lenght_fu | int | 0 | Number of millimeters on a prostate cancer biopsy consisting of prostate cancer (largest part). |
| mri_taken | int | 0 | MRI made at baseline. Result MRI does not always have to be given, so save separately. |
| mri_lesions | int | 0 | Abnormalities detected on MRI. |
| mri_suspected_number | int | 0 | Number of suspected abnormalities/lesions on MRI. |
| mri_pirads_1 | int | 0 | The PIRADS score is given for each suspected lesion (maximum of 3).  |
| mri_largest_dia_1 | int | 0 | The largest diameter in mm of lesion 1. |
| mri_location_1 | int | 0 | Location of lesion 1 in the prostate. |
| mri_location_free_1 | varchar |  |  Location of lesion 1 in the prostate. |
| mri_pirads_2 | int | 0 | The PIRADS score is given for each suspected lesion (maximum of 3).  |
| mri_largest_dia_2 | int | 0 | The largest diameter in mm of lesion 2.   |
| mri_location_2 | int | 0 |  Location of lesion 2 in the prostate.  |
| mri_location_free_2 | varchar |  | Location of lesion 1 in the prostate. |
| mri_pirads_3 | int | 0 | The PIRADS score is given for each suspected lesion (maximum of 3).  |
| mri_largest_dia_3 | int | 0 | The largest diameter in mm of lesion 3. |
| mri_location_3 | int | 0 | Location of lesion 3 in the prostate. |
| mri_location_free_3 | varchar |  | Location of lesion 1 in the prostate. |
| mri_progrssion_lesions | real |  | Progressions of lesions on MRI compared to previous MRI. |
| mri_targeted_biopsy | int | 0 |  Targeted biopsies. 0 - empty, 1 - yes, 2 - no |
| mri_targeted_cores | int | 0 | Number of cores with prostate cancer from targeted biopsies taken.  Only use when targeted biopsys - yes (0 can mean both not given and no pc cores found).  |
| mri_targeted_taken | int | 0 | Number of cores taken from the abnormalities seen on MRI (targeted). |
| mri_targeted_gleason1 | int | 0 | To be checked; missing field for second part of the gleason score |
| mri_lesion_positive | real | 0 | Number of lesions  that are confirmed by biopt as prostate cancer. 0 can mean both not recorded and no positive found. |
| mri_method_used | int | 0 | Combine with mri_targeted_biopsy.0, if done also include this method.  |
| mri_prostate_volume | int |  | Not measured by MRI, but manually entered based on MRI in ml. |
| mri_prostate_volume_method | int |  |  |
| year_visit | int | 2017 | Do not map, use days_psa_diag |
| days_psa_diag | int |  | Days since prostate cancer diagnosis (from the basedata table).  If negative, report and do not include (to be fixed on source side). |

### Table: enddata.csv

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| p_id | int | List truncated... | Multiple rows per id? Patient id? |
| nr_fuvisits | int | 4 | Number of follow up visits.  Do not map, administrative (max from time in fudata) |
| discontinued | varchar | Robot radical prostatectomy | Given therapy  Except; death, lost to follow-up and on request   |
| days_discontinued_diagnosis | int | 385 | Days from diagnosis to discontinuation? |
| reason_treatment | varchar | Based on protocol advice | General reason for discontinuation in Active Surveillance (additional information may be still collected, not in extract) |
| days_surgery_diagnosis | int |  | Days from diagnosis to surgery.  This is often later than discontinued  Do not map, Often not given, use days_discontinued |
| pt | varchar |  | Surgery T stadium by pathologist  Same mapping as dre |
| pn | int |  | N stadium.   9 - pnx, unknown (no prostatectomy)  0 - pn0  1 - pn1 |
| pm | int |  | M stadium.   9 - pmx (no prostatectomy)  0 - pm0  1 - pm1 |
| gleason1_rad_prost | int |  | Radical (geheel verwijderd) prostatectomy |
| gleason2_rad_prost | int |  |  |
| prostatevolume | varchar |  | Volume as by pathologist |
| tumorvolume | real |  | Volume in ml of only the tumor |
| ece | int |  | Extra capsulaire extension (yes/no/unknown)  0 - no  1 - yes  9 - unknown (do not map)  To be checked   |
| svi | int |  | seminal vesical invasion (yes/no/unknown)  0 - no  1 - yes  9 - unknown (do not map, might not be different from empty)  To be checked   |
| pos_surgical_margins | int |  | Positive surgical margins  Is the tumor completely (cleanly) removed?  0 - no  1 - yes  9 - unknown (do not map)   |
| postoperative_psa | varchar |  | PSA level after surgery. Typical 6 weeks-3months after surgery   |
| pathology_reported | int |  | Do not map, administrative whether pathology done. |
| adjuvant_radiotherapy | int |  | Radiotherapy after surgery  1 - yes  0 - no  9 - unknown  Only map 1 |
| year_discontinued | int | 2015 | Year of discontinuation  Do not use, instead use days discontinued and year_diag as proxy |

### Table: stem_table

| Field | Type | Most freq. value | Comment |
| --- | --- | --- | --- |
| domain_id | CHARACTER VARYING |  |  |
| person_id | INTEGER |  |  |
| visit_occurrence_id | INTEGER |  |  |
| visit_detail_id | INTEGER |  |  |
| provider_id | INTEGER |  |  |
| id | INTEGER |  |  |
| concept_id | INTEGER |  |  |
| source_value | CHARACTER VARYING |  | TODO: variable name |
| source_concept_id | INTEGER |  |  |
| type_concept_id | INTEGER |  |  |
| start_date | DATE |  |  |
| start_datetime | DATETIME |  |  |
| end_date | DATE |  |  |
| end_datetime | DATETIME |  |  |
| verbatim_end_date | DATE |  |  |
| days_supply | INTEGER |  |  |
| dose_unit_source_value | CHARACTER VARYING |  |  |
| lot_number | CHARACTER VARYING |  |  |
| modifier_concept_id | INTEGER |  |  |
| operator_concept_id | INTEGER |  |  |
| modifier_concept_id | INTEGER |  |  |
| modifier_source_value | CHARACTER VARYING |  |  |
| quantity | INTEGER |  |  |
| range_high | FLOAT |  |  |
| range_low | FLOAT |  |  |
| refills | INTEGER |  |  |
| route_concept_id | INTEGER |  |  |
| route_source_value | CHARACTER VARYING |  |  |
| sig | CHARACTER VARYING |  |  |
| stop_reason | CHARACTER VARYING |  |  |
| unique_device_id | CHARACTER VARYING |  |  |
| unit_concept_id | INTEGER |  |  |
| unit_source_value | CHARACTER VARYING |  |  |
| value_as_concept_id | INTEGER |  |  |
| value_as_number | DECIMAL |  |  |
| value_as_string | CHARACTER VARYING |  |  |
| value_source_value | CHARACTER VARYING |  |  |
| anatomic_site_concept_id | INTEGER |  |  |
| disease_status_concept_id | INTEGER |  |  |
| specimen_source_id | INTEGER |  |  |
| anatomic_site_source_value | CHARACTER VARYING |  |  |
| disease_status_source_value | CHARACTER VARYING |  |  |
| condition_status_concept_id | CHARACTER VARYING |  |  |
| condition_status_source_value | INTEGER |  |  |
| event_id | INTEGER |  |  |
| event_field_concept_id | INTEGER |  |  |
| value_as_datetime | DATETIME |  |  |
| qualifier_concept_id | INTEGER |  |  |
| qualifier_source_value | CHARACTER VARYING |  |  |
