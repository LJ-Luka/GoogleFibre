# Google Fibre

## Google BI Certificate project  
  
View the stakeholder requirement document [here](https://github.com/LJ-Luka/GoogleFibre/blob/main/Stakeholder-Requirements-Document.docx)  
View the project requirement document [here](https://github.com/LJ-Luka/GoogleFibre/blob/main/Project-Requirements-Document.docx)  
View the strategy document [here](https://github.com/LJ-Luka/GoogleFibre/blob/main/Strategy-Document.docx)   
View the final dashboard [here](https://public.tableau.com/app/profile/lumi.luka/viz/Google_Fiber_Reporting_Tables/GoogleFiber)  

The Google Fiber project from the Google BI Certificate project was completed in stages.  
The first stage was getting familiar with initial meetings with stakeholders and using information from those to fill out Key BI documents. These are Stakeholder requirement documents, Project requirement documents and Strategy documents. They help take note of project objectives, goals, success criteria, stakeholder needs, stakeholders, team members and many more. The strategy document specifically has a section for documenting details regarding charts to be used – usually as a guide.  
In the second stage, ETL skills were practised. One alternative was to use SQL to unionise the 3 tables provided and then import the unionised dataset into Tableau. The other was to import them into Tableau, create a connection between them, and unionise them. The latter was chosen for this project.  
For the alternative – The Big Query option, a dataset was created, and then the tables were created within the dataset. The next step was to unionise the data. The codes below show how it was done. Usually, for a set of tables to be unionised, they should have similar data.

```sql
SELECT *
FROM
`scenic-alcove-364514.Google_FIber.market_1`
UNION ALL
SELECT *
FROM
`scenic-alcove-364514.Google_FIber.market_2`
UNION ALL
SELECT *
FROM
`scenic-alcove-364514.Google_FIber.market_3`
```
  
The transformation of the dataset was done in the final course of the certificate track, but it will be described here. A few measures were created to aid the visualisation of the data. For instance, a calculated column was created to find the days of the week from the date column using the formula: DATENAME ("weekday", [Date Created]). Fields were also created to describe the problem types based on the description from the stakeholder meeting.  
In the visualisation phase, the data was visualised using charts to identify patterns in repeat calls, as was the requirement of the project. They met the following needs of the stakeholders:  
1.	A chart showcasing repeat calls by week, month, and quarter
2.	A chart exploring repeat calls by market and problem type
3.	A chart measuring repeat calls by first contact date
4.	A chart exploring repeat caller trends in the three different market cities
