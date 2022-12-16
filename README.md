# GPS_analysis
Analysis of GPS interruption data in public domain. This is a project I do in my free time, using public datasets processed with JupyterLab on Github Codespaces. It is not related to my current or previous employers.

# License status of source data
At the time of writing, [wikipedia](https://www.wikipedia.org/) is available under the Creative Commons Attribution-ShareAlike 3.0 License. The [Navigation Center of the United States Coast Guard](https://www.navcen.uscg.gov/) does not have a copyright or license statement on their website. The data is scraped as 'fair use'. The [UNECE](https://unece.org/) website data can be downloaded and copied for personal, non commercial use. This dictates the licensing of this repository as Creative Commons Attribution-ShareAlike, in order to be compatible with the wikipedia license.

# Roadmap
Aims:
- Clean up data in a way that allows longer term trends, global year on year analysis.
- Extract enough detail so that the dataset can serve as labelling/ground truth for GPS interference detection work.  

# Data Model:  
```mermaid
graph TD;
    NavCen_Website-->gps_navcen.csv;
    Wikipedia--> US_states_iso3166.csv;
    Wikipedia--> Sovereign_States.csv;
    UNECE-->UN_LOCODE_detail.csv
    UNECE-->UN_LOCODE.csv
    US_states_iso3166.csv--> two_letter_codes;
    UKUS_dataframe--> two_letter_codes;
    US_states_iso3166.csv-->coalesced_country;
    two_letter_codes-->coalesced_country;
    Sovereign_States.csv-->coalesced_country;
    UN_LOCODE_detail.csv-->coalesced_country;
    UN_LOCODE.csv-->coalesced_country;
    gps_navcen.csv-->coalesced_country;
    
 ```
