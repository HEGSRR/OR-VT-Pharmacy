# Spatio-Temporal Accessibility of Pharmacy Care in Vermont, USA

## Contributors

- Sam Roubin, sroubin@middlebury.edu, @samroubin, https://orcid.org/0009-0005-5490-3744, Middlebury College
- Joseph Holler\*, jholler@middlebury.edu, @josephholler, https://orcid.org/0000-0002-2381-2699, Middlebury College
- Peter Kedron, peterkedron@ucsb.edu, @Peter-Kedron, https://orcid.org/0000-0002-1093-3416, University of California, Santa Barbara

\* Corresponding author

## Abstract

Pharmacy care is a fundamental aspect of primary healthcare and is gaining greater recognition in the healthcare landscape.
Recent research has underscored the importance of pharmacy access in primary care, as pharmacies are visited at higher rates than primary care providers and are particularly valuable for reaching rural populations.
We aim to measure spatiotemporal variation in access to pharmacy care across the state of Vermont using the enhanced 2-step floating catchment area (E2SFCA) method.
Specifically, we seek to identify areas that have particularly limited access to pharmacies.
This research is temporally explicit, as it will analyze variation in accessibility at specific times of the day and days of the week.
Such temporally granular data has benefits for the research since it provides information on how spatial accessibility varies at irregular times, improving our understanding of when pharmacy care is particularly limited for certain populations.
Results will be depicted as a series of spatial accessibility maps, covering diverse temporal extents to capture variations in pharmacy working hours.
Previous studies have used the two step floating catchment area (2SFCA) and the E2SFCA method to measure spatial accessibility of pharmacy care across geographic scales and regions.
To our knowledge, this is the first temporally-explicit study of pharmacy care, and the first E2SFCA study of pharmacy accessibility in Vermont.
The results of this study are of interest to service providers and Vermont state public health officials and may have important implications for public health planning in the state.

This study adapts and extends the methodology used in Kang et al.'s (2020) "Rapidly measuring spatial accessibility of COVID-19 healthcare resources: a case study of Illinois, USA" to measure spatial accessibility of pharmacy care across Vermont.

## Study Metadata

- `Key words`: Pharmacy, spatial accessibility, pharmacy deserts, Vermont, E2FSCA.
- `Subjects`:
  - Medicine and Health Sciences: Public Health: Health Services Research
  - Social and Behavioral Sciences: Geography: Geographic Information Sciences
  - Social and Behavioral Sciences: Geography: Human Geography
- `Date created`: 9/18/2023
- `Date modified`: 1/11/2024
- `Spatial Coverage`: The state of Vermont and areas within 10-miles of the Vermont border (MA, NY, NH). Canada is excluded.
- `Spatial Resolution`: Vermont municipalities. These units are roughly the same size as census tracts, but they represent politically meaningful geographic units.
- `Spatial Reference System`: EPSG 6589
- `Temporal Coverage`: Data was collected in October, November, and December of 2023. The temporal extent is not explicitly determined. Pharmacies have been asked to provide their staffing levels over the period of roughly a month. The results from the study will be theoretically based on a single point in time in the fall of 2023. This is a one time measurement, and the study does not investigate change over time.
- `Temporal Resolution`: The highest temporal resolution of this study is one hour. Many results and figures aggregate the temporal resolution into days of the week or common operating hours. 
- `Funding Name`: National Science Foundation Directorate for Social, Behavioral and Economic Sciences
- `Funding Title`: Transforming theory-building and STEM education through reproductions and replications in the geographical sciences
- `Award info URI`: <https://www.nsf.gov/awardsearch/showAward?AWD_ID=2049837>
- `Award number`: BCS-2049837

## Related to

- `OSF Project`: Roubin, S., & Holler, J. (2024, January 11). Spatio-Temporal Accessibility of Pharmacy Care in Vermont, USA. <https://doi.org/10.17605/OSF.IO/BCQ9S>
- `Pre-analysis Registration`: <https://doi.org/10.17605/OSF.IO/BCQ9S>
- `Post-analysis Report Registration`:
- `Preprint`:
- `Conference Presentation`: 2024 American Association of Geographers Annual Meeting [slides](docs/presentation/SR_AAG_2024.pptx) and [abstract](https://aag.secure-platform.com/aag2024/solicitations/57/sessiongallery/7796/application/30826)
- `Publication`:
- `Prior Studies`:
  - Kang, J.-Y., Michels, A., Lyu, F., Wang, S., Agbodo, N., Freeman, V. L., & Wang, S. (2020). Rapidly measuring spatial accessibility of COVID-19 healthcare resources: A case study of Illinois, USA. International Journal of Health Geographics, 19(1), 36. <https://doi.org/10.1186/s12942-020-00229-x>
  - Holler, J., Burt, D., Udoh, K., & Kedron, P. (2023, November 2). Reproduction and Reanalysis of Kang et al 2020 Spatial Accessibility of COVID-19 Health Care Resources. <https://doi.org/10.17605/OSF.IO/N92V3>

## Metadata for access

- `Rights`: [LICENSE](LICENSE): BSD 3-Clause "New" or "Revised"
- `Resource type`: Collection
- `Resource language`: English
- `Conforms to`: Template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences version 1.0, DOI:[10.17605/OSF.IO/W29MQ](https://doi.org/10.17605/OSF.IO/W29MQ)

## Compendium structure and contents

This research compendium is structured with four main directories:

- `data`: contains subdirectories for `raw` data and `derived` data.
- `docs`: contains subdirectories for `manuscript`, `presentation`, and `report`
- `procedure`: contains subdirectories for `code` or software scripts, information about the computational `environment` in which the research was conducted, and non-code research `protocols`
- `results`: contains subdirectories for `figures`, formatted data `tables`, or `other` formats of research results.

The data, procedures, and results of this repository are outlined in three tables:
- Data: [data/data_index.csv](data/data_index.csv)
- Procedures: [procedure/procedure_index.csv](procedure/procedure_index.csv)
- Results: [results/results_index.csv](results/results_index.csv)

Important local **documents** include:
- Pre-analysis plan: [docs/report/analysis_plan.pdf](docs/report/analysis_plan.pdf)
- Presentation: [docs/presentation/SR_AAG_2024.pptx](docs/presentation/SR_AAG_2024.pptx)
- Study report: [docs/report/analysis_report.pdf](docs/report/analysis_report.pdf) and [docs/index.html](docs/index.html)
- Manuscript: (in progress) [docs/manuscript/manuscript.pdf](docs/manuscript/manuscript.pdf)

#### Compendium reference

The [template_readme.md](template_readme.md) file contains more information on the design of this template and references used in the design.
The [Template_LICENSE](Template_LICENSE) file provides the BSD 3-Clause license for using this template.
To cite the template, please use [template_reference.bib](template_reference.bib) or:
> Kedron, P., & Holler, J. (2023). Template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences. https://doi.org/10.17605/OSF.IO/W29MQ
