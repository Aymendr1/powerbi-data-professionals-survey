# Data Professionals Survey (Power BI)

One-page dashboard summarizing a survey of data professionals:
- **Average Salary by Job Title**
- Gauges: **Happiness with Work–Life** and **Happiness with Salary**
- **Favorite Programming Languages**
- **Difficulty to Break Into Data**
- Country overview (treemap)

## Model
- **FactResponses**(Salary, SatisfactionWorkLife, SatisfactionSalary, Dt, JobKey, CountryKey, LangKey)
- **DimJob**, **DimCountry**, **DimLanguage**, **Calendar(Date, Year)** — *Calendar is marked as Date table*

## Example measures
```DAX
Avg Salary := AVERAGE(FactResponses[Salary])
Happiness WorkLife := AVERAGE(FactResponses[SatisfactionWorkLife])
Happiness Salary   := AVERAGE(FactResponses[SatisfactionSalary])
