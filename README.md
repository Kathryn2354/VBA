# VBAredo



# Explanation of the VBA Code
``Public Sub markdown()

Dim cell As Range
Dim selectedRange As Range

Set selectedRange = Application.Selection

Dim rowCounter As Integer
Dim columnCounter As Integer
Dim totalColumns As Integer
Dim currentColumnWidth As Integer

totalColumns = selectedRange.Columns.Count

Dim ColumnWidth(40) As String


For I = 0 To totalColumns
    ColumnWidth(I) = 0
Next I


For Each row In selectedRange.Rows

    columnCounter = 0
    
    For Each cell In row.Cells
    
        currentColumnWidth = Len(cell.Value)
        
        If (currentColumnWidth > ColumnWidth(columnCounter)) Then

                ColumnWidth(columnCounter) = currentColumnWidth

            End If

            columnCounter = columnCounter + 1
            '/// Debug.Print cell.Address, " ", cell.Value, "->", Len(cell.Value)

        Next cell

    Next row

    '///
    '/// go through range to calculate maximum lengths of each column
    '///
    Dim currentLine As String

    rowCounter = 0
    For Each row In selectedRange.Rows

        columnCounter = 0

        currentLine = "|"

        For Each cell In row.Cells

            currentColumnWidth = ColumnWidth(columnCounter)
            Dim extraSpaces As Integer

            currentLine = currentLine & " "
            currentLine = currentLine & cell.Value
            extraSpaces = currentColumnWidth - Len(cell.Value)

            For j = 0 To extraSpaces

                currentLine = currentLine & " "

            Next j

            currentLine = currentLine & " |"

            columnCounter = columnCounter + 1
            '/// Debug.Print cell.Address, " ", cell.Value, "->", Len(cell.Value)

        Next cell

        Debug.Print currentLine

        If (rowCounter = 0) Then

            currentLine = "|"
            columnCounter = 0

            For j = 0 To (totalColumns - 1)

                currentLine = currentLine
                currentColumnWidth = ColumnWidth(columnCounter)
                currentLine = currentLine & "-"

                For k = 0 To currentColumnWidth

                    currentLine = currentLine & "-"
                Next k

                currentLine = currentLine & "-|"
                columnCounter = columnCounter + 1

            Next j
    
            Debug.Print currentLine
        End If

        rowCounter = rowCounter + 1

    Next row
 
End Sub``


[Data Science Schedule.zip](https://github.com/Kathryn2354/VBAredo/files/8240549/Data.Science.Schedule.zip)




|            | Day           | Topic                                                                                                                                           | Due                                                                                                                                                                                                                                                             |
|------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|            |               |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 1/18/2021  | 1             | [What is Data Science](https://docs.google.com/document/d/1yhVB9DfddvJIiXitX2ZC1W0D3cJbcvib5fWmUlgqNO0/edit)                                    |                                                                                                                                                                                                                                                                 |
| 1/20/2021  | 2             | [VBA](https://docs.google.com/document/d/1ASoeI5CjFgyQTBm-HFPvmRC_94niTPx4s9crQEDVb10/edit)                                                     | [HW1 - Excel](https://docs.google.com/document/d/1g8eOYNe9sDmrstRgvFRZBskxjaIaD7Za4lFXSgPPkVw/edit)                                                                                                                                                             |
| 1/25/2021  | 3             | [Data Communcation](https://docs.google.com/document/d/1PTe_eezbRdZcxIOODyiQzDM4vtjVNJkVDC_7vZQSoZE/edit)                                       |                                                                                                                                                                                                                                                                 |
| 1/27/2021  | 4             | Work Day                                                                                                                                        | [HW2 - VBA](https://docs.google.com/document/d/1bTkmUon_Kq6_DupNw2Szh-T4rFGqzeA2aIIBy7m1yhk/edit)                                                                                                                                                               |
| 2/1/2021   | 5             | Importance of Visualizations & Writing, Tableau                                                                                                 | [Reading Due - Florence Nightengale](https://docs.google.com/forms/d/1FBgScIpV9Vpa-jb1nlWuoCqOxFE7v5SmQtacpFHpIq8/viewform?edit_requested=true)                                                                                                                 |
| 2/3/2021   |               | Class Canceled                                                                                                                                  |                                                                                                                                                                                                                                                                 |
| 2/8/2021   | 6             | Work day                                                                                                                                        |                                                                                                                                                                                                                                                                 |
| 2/10/2021  | 7             | [Reading Review](https://docs.google.com/forms/d/1JJ3pD4m_kvgERvRMuFSiDxglcJmNxvg1N8fegM7ubyA/viewform?edit_requested=true)                     | [HW 3 - Tableau](https://docs.google.com/document/d/1bta4t39rpvl-kXgO2pmZPGypWnYyBbiyzCPek9kxv9E/edit)                                                                                                                                                          |
| 2/15/2021  | 8             | [Data Exploration with Data Vis + R Intro](https://docs.google.com/document/d/1KI0OLn91_FJ03bQJW8ptoMNqOo8EL6MKzwLxvzIzNnM/edit)                | [Reading - Reveal Don't Conceal](https://docs.google.com/forms/d/1zno4KDCz5dWahMLxWlQDUzI7sfpd2ygYqU6H_k05K-E/viewform?edit_requested=true)                                                                                                                     |
| 2/17/2021  | 9             | ggplot Intro                                                                                                                                    | [Reading - Why Data is good for governments to provide](https://www.theguardian.com/local-government-network/2013/oct/21/open-data-us-san-francisco)                                                                                                            |
| 2/22/2021  | 10            | Danielle                                                                                                                                        |                                                                                                                                                                                                                                                                 |
| 2/24/2021  | 11            | Work Day                                                                                                                                        | [HW 4 - Data Exploration Tableau](https://docs.google.com/document/d/1GJbs8fvJn99ogIkj3jbGYEoTcw0Tgu4XyI15WOqdQfs/edit)                                                                                                                                         |
| 3/1/2021   | 12            | [Remember Statistics - Linear Regression](https://docs.google.com/document/d/14MH0Qq9nTMTY1uYrVohCFPWajxAF0SO_TxA7n0LxEKA/edit?urp=gmail_link)  |                                                                                                                                                                                                                                                                 |
| 3/3/2021   | 13            | Logistic Regression                                                                                                                             |                                                                                                                                                                                                                                                                 |
| 3/8/2021   | 14            |                                                                                                                                                 | [P-Hacking](https://rss.onlinelibrary.wiley.com/doi/10.1111/1740-9713.01554)                                                                                                                                                                                    |
| 3/10/2021  | 15            | Work Day                                                                                                                                        | HW 5 - ggplots & Regressions                                                                                                                                                                                                                                    |
| 3/15/2021  | Spring Break  |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 3/17/2021  |               |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 3/22/2021  | 16            | Data Annonymity                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 3/24/2021  | 17            | [De-Annonymizing Data](https://www.nature.com/articles/s41467-019-10933-3)                                                                      | Or Access and more Data base stuff                                                                                                                                                                                                                              |
| 3/29/2021  | Advising Day  |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 3/31/2021  | 18            | Random Forest                                                                                                                                   | HW 6 - Random Forest                                                                                                                                                                                                                                            |
| 4/5/2021   | 19            |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 4/7/2021   | 20            |                                                                                                                                                 | [Possible Reading - Proxy Discrimination - When AI find predictive proxies for race - because society is segregated in this way. ](https://ilr.law.uiowa.edu/print/volume-105-issue-3/proxy-discrimination-in-the-age-of-artificial-intelligence-and-big-data)  |
| 4/12/2021  | 21            | Clustering - K Nearest Neighbors                                                                                                                |                                                                                                                                                                                                                                                                 |
| 4/14/2021  | 22            |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 4/19/2021  | 23            | Final Project                                                                                                                                   | HW 6 - Clustering                                                                                                                                                                                                                                               |
| 4/21/2021  | 24            |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 4/26/2021  | 25            |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 4/28/2021  | 26            |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
|            |               |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
|            |               |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
|            |               | Additional Readings                                                                                                                             | Data Sets                                                                                                                                                                                                                                                       |
|            |               | [A Brief History of Data Visualization](https://www.datavis.ca/papers/hbook.pdf)                                                                | [Maryland Data](https://gopi.maryland.gov/)                                                                                                                                                                                                                     |
|            |               | [Bar Graphs instead of Scatter Plots](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1002128)                            | [NYT COVID Data](https://github.com/nytimes/covid-19-data)                                                                                                                                                                                                      |
|            |               | [Different Kinds of Data Visualization](https://github.com/arielcwebster/DataScience/blob/main/visualdatacommunication.pdf)                     | [NOAA Data](https://www1.ncdc.noaa.gov/pub/data/ghcn/daily/)                                                                                                                                                                                                    |
|            |               | [COVID Risk Calculator](https://www.nytimes.com/2021/12/30/style/covid-risk-calculator.html)                                                    |                                                                                                                                                                                                                                                                 |
|            |               | How Charts Lie                                                                                                                                  |                                                                                                                                                                                                                                                                 |
