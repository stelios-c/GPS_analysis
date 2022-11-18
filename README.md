# GPS_analysis
Analysis of GPS interruption data in public domain.  
Aims:
- Clean up data in a way that allows longer term trends, global year on year analysis.
- Extract enough detail so that the dataset can serve as labelling/ground truth for GPS interference detection work.
```mermaid
graph TD;
    NavCen Website-->List of events ;
    Wikipedia--> List of two letter codes;
    Hardcoded UK dataframe--> List of two letter codes;
    List of events-->Clean List;
    List of two letter codes-->Clean List;
 ```
