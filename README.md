# GPS_analysis
Analysis of GPS interruption data in public domain. This is a project I do in my free time, using public datasets processed with JupyterLab on Github Codespaces. It is not related to my current or previous employers.

# License status of source data
At the time of writing, wikipedia is available under the Creative Commons Attribution-ShareAlike 3.0 License. The Navigation Center of the United States Coast Guard does not have a copyright or license statement on their website. The data is scraped as 'fair use'.

# Roadmap
Aims:
- Clean up data in a way that allows longer term trends, global year on year analysis.
- Extract enough detail so that the dataset can serve as labelling/ground truth for GPS interference detection work.  

# Data Model:  
```mermaid
graph TD;
    NavCen_Website-->gps_navcen.csv;
    Wikipedia--> US_states_iso3166.csv;
    UK_dataframe--> two_letter_codes;
    US_states_iso3166.csv--> two_letter_codes;
    two_letter_codes-->gps_navcen_2letter;
    gps_navcen.csv-->gps_navcen_2letter;
    gps_navcen.csv-->Not2letter_common;
    gps_navcen.csv-->Not2letter_uncommon;
 ```
