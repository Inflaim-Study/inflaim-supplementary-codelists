# Supplementary Codelists for the Inflaim Study

This repository contains supplementary clinical codelists developed for and used by the Inflaim Study. These lists are intended to complement the **main Inflaim long-term condition (LTC) codelists**, which are published in a separate repository.

* **View the Main Inflaim LTC Codelists here:** [https://github.com/Inflaim-Study/Inflaim-LTC-code-list](https://github.com/Inflaim-Study/Inflaim-LTC-code-list)

The codelists provided here fall into three main categories:
1.  **"Other" Long-Term Conditions (LTCs)**
2.  **Autoimmune Conditions**
3.  **Infectious Conditions**

All codelists are provided in `.csv` format and use **`MedCodeId`** as the primary identifier, making them suitable for use with the CPRD Aurum database.
***

## Repository Structure

This repository is organized to separate the data (the codelists) from the project documentation.
```plaintext
├── codelists/
│   ├── Inflaim_Other_LTCs_Codelist_v1.0.csv
│   ├── Inflaim_Autoimmune_Codelist_v1.0.csv
│   └── Inflaim_Infections_Codelist_v1.0.csv
│
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE.md
└── README.md

***
## Codelist Descriptions 

### "Other" Long-Term Conditions (LTCs)
This is a curated list of **1,109 unique `MedCodeId`s** representing **46 distinct long-term conditions** that were not included in the main LTC publication.

* **Methodology**: This codelist was prepared through a multi-stage, systematic process led by expert review:
    1.  **Expert-led Curation**: The initial selection of conditions was conducted by an expert clinical panel. The panel curated the list by integrating and reviewing phenotypes from several high-quality sources, including the **CALIBER resource** [23] (adapted for CPRD Aurum via Kuan et al. (2019)) and the **[MULTIPLY Initiative](https://github.com/Fabiola-Eto/MULTIPLY-Initiative)**.
    2.  **Keyword Filtering**: The compiled list underwent a cleaning step to ensure it represented chronic, diagnostic conditions. Codes were programmatically excluded if their medical `Term` contained keywords related to acute conditions, congenital disorders, or non-diagnostic administrative events (e.g., 'review', 'referral').
    3.  **De-duplication**: To prevent overlap with our core LTCs, any `MedCodeId` already present in the **main Inflaim LTC codelist** was removed.
    4.  **Final Validation**: The resulting codelist underwent a final validation by the expert clinical panel to ensure all included conditions were appropriate for the study's scope before finalisation.
* **Source**: Key sources include Kuan et al. (2019), Head et al.(2021), and the [MULTIPLY Initiative](https://github.com/Fabiola-Eto/MULTIPLY-Initiative).

***
### Autoimmune Conditions
This codelist contains **228 unique `MedCodeId`s** for a range of inflammatory autoimmune diseases, categorized across **10 distinct autoimmune sites**.

* **Methodology**: The list was developed using the validated Read v2 codelists from Watson et al. (2018). These codes were mapped to their corresponding `MedCodeId`s using the CPRD Aurum medical dictionary. A crucial final step involved removing any codes that were already present in **either our main Inflaim LTC codelist or the "Other" LTCs list** to avoid duplication. The 228 `MedCodeId`s resolve to **164 unique SNOMED CT concepts**.
* **Source**: Watson, J., et al. (2018). *CPRD codes: infections and autoimmune diseases*. University of Bristol. DOI: `10.5523/bris.2954m5h0ync672u8yzx16xxj7l`

***
### Infectious Conditions
This codelist provides a comprehensive set of **2,668 unique `MedCodeId`s** for infectious diseases, grouped into **17 distinct infection sites**.

* **Methodology**: Following the same process as the autoimmune list, this codelist was derived from the work of Watson et al. (2018). The original Read v2 codes were mapped to `MedCodeId`s and subsequently filtered to exclude any codes already present in **either the main Inflaim LTC codelist or the "Other" LTCs list**. The resulting 2,668 codes map to **1,765 unique SNOMED CT concepts**.
* **Source**: Watson, J., et al. (2018). *CPRD codes: infections and autoimmune diseases*. University of Bristol. DOI: `10.5523/bris.2954m5h0ync672u8yzx16xxj7l`

***
## How to Use

The codelists are provided as CSV files in the `/codelists` directory. They can be loaded into any standard data analysis software (e.g., Python with Pandas, R, Stata). The primary column, **`MedCodeId`**, can be used to identify patient records with these conditions in electronic health record datasets like CPRD Aurum.

***


### License
This work is licensed under the [MIT License / Creative Commons Attribution 4.0 International License]. Please see the `LICENSE` file for details.