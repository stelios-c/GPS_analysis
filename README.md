# GPS_analysis
Analysis of GPS interruption data in public domain.  
Aims:
- Clean up data in a way that allows longer term trends, global year on year analysis.
- Extract enough detail so that the dataset can serve as labelling/ground truth for GPS interference detection work.
```mermaid
graph TD;
    NavCen_Website-->gps_navcen.csv;
    Wikipedia--> US_states_iso3166.csv;
    UK_dataframe--> two_letter_codes;
    gps_navcen.csv-->Clean_List;
    two_letter_codes-->Clean_List;
 ```
