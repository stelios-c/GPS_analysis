# GPS_analysis
Analysis of GPS interruption data in public domain. This is a project I do in my free time, using public datasets processed with JupyterLab on Github Codespaces. It is not related to my current or previous employers.   
Aims:
- Clean up data in a way that allows longer term trends, global year on year analysis.
- Extract enough detail so that the dataset can serve as labelling/ground truth for GPS interference detection work.  
Data Model:  
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
