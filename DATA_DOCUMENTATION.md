
## 1. Source
 [The Eviction Lab at Princeton University](https://evictionlab.org/)


---

## 2. Size
* **Total Records (Rows):** 578 state-year observations
* **Total Features (Columns):** 25 variables

---

## 3. Features & Data Dictionary

| Variable Name | Data Type | Measurement Unit | Description |
| :--- | :--- | :--- | :--- |
| `geoid` | Integer | FIPS Code | Federal Information Processing Standard state code identifier. |
| `year` | Integer | Calendar Year | Observation year (2000–2016). |
| `name` | String | Categorical | State name (e.g., Alabama, Florida, Ohio). |
| `parentlocation` | String | Categorical | Country designation (`USA`). |
| `population` | Integer | Count | Total estimated state population. |
| `povertyrate` | Float | Percentage (%) | Proportion of state residents living below the federal poverty line. |
| `renteroccupiedhouseholds`| Integer | Count | Total number of occupied housing units inhabited by renters. |
| `pctrenteroccupied` | Float | Percentage (%) | Percentage of all occupied housing units occupied by renters. |
| `mediangrossrent` | Integer | USD ($) | Median monthly gross rent (contract rent + estimated utilities). |
| `medianhouseholdincome` | Integer | USD ($) | Median annual gross household income within the state. |
| `medianpropertyvalue` | Integer | USD ($) | Median owner-estimated home value. |
| `rentburden` | Float | Percentage (%) | Median gross rent expressed as a share of median household income. |
| `pctwhite` | Float | Percentage (%) | Non-Hispanic White share of the population. |
| `pctafam` | Float | Percentage (%) | Black / African American share of the population. |
| `pcthispanic` | Float | Percentage (%) | Hispanic / Latino share of the population. |
| `pctamind` | Float | Percentage (%) | American Indian and Alaska Native share of the population. |
| `pctasian` | Float | Percentage (%) | Asian American share of the population. |
| `pctnhpi` | Float | Percentage (%) | Native Hawaiian and Other Pacific Islander share. |
| `pctmultiple` | Float | Percentage (%) | Individuals identifying with two or more races share. |
| `pctother` | Float | Percentage (%) | Share of population identifying with other races. |
| `evictionfilings` | Float | Count | Total number of formal eviction complaints filed in civil/housing court. |
| `evictions` | Float | Count | Total number of formal court orders granting an eviction judgment. |
| `evictionrate` | Float | Rate per 100 | Ratio of formal eviction judgments per 100 renter-occupied households. |
| `evictionfilingrate` | Float | Rate per 100 | Ratio of formal eviction filings per 100 renter households (**Target Feature**). |
| `lowflag` | Integer | Binary (0 or 1) | Quality control flag indicating if filings are suspected of undercounting (all 0 in validated set). |

---

## 4. Potential Issues & Data Limitations

* **Missing Values in Eviction Metrics:**
 
  * Court records only capture formal legal filings. They systematically omit informal displacement (e.g., illegal lockouts, landlord buyouts, self-evictions upon receiving informal verbal notices), resulting in conservative baseline counts of housing instability.
  * Court fees and procedural requirements differ by state. In states with minimal court filing fees, landlords frequently use eviction court repeatedly as a routine rent-collection notice, inflating filing rates relative to actual physical displacements.
