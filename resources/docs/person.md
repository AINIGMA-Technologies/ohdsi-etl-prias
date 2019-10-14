## Table name: person

### Reading from basedata.csv

![](index_files/image2.png)

| Destination Field | Source field | Logic | Comment field |
| --- | --- | --- | --- |
| person_id | p_id |  | Use p_id directly<br> |
| gender_concept_id |  |  | Always male 8507 |
| year_of_birth |  |  | year of birth source field to be provided |
| month_of_birth |  |  |  |
| day_of_birth |  |  |  |
| birth_datetime |  |  |  |
| death_datetime |  |  |  |
| race_concept_id |  |  | 0 |
| ethnicity_concept_id |  |  | 0 |
| location_id |  |  |  |
| provider_id |  |  |  |
| care_site_id |  |  | Is known, chosen not given in the data extract. |
| person_source_value | p_id |  |  |
| gender_source_value |  |  |  |
| gender_source_concept_id |  |  |  |
| race_source_value |  |  |  |
| race_source_concept_id |  |  |  |
| ethnicity_source_value |  |  |  |
| ethnicity_source_concept_id |  |  |  |
