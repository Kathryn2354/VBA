# VBAredo

# Instructions for the this vba redo:
<ol>
    <li>If a column is blue at the top you will include the column</li>
    <li>If a cell is orange you will not include the text for that cell in your markdown table</li>
    <li>If the cell is yellow you will not include the hyperlink for that cell. </li>
</ol>


# Explanation of the VBA Code

## This code is to change the cells with a hyperlink to markdown link format. 
    `'Start of function
      Sub changeMarkdownlinkformat()

    'initialize variable nemed cell as range.
     Dim cell As Range

    'This loop through a certain range of cells to change the text with hyperlink attached into the markdown link format for the C Column.
     For Each cell In Range("C3:C40")

    'Start of first if statement
     If cell.Value = "What is Data Science" Then
        cell.Value = "[What is Data Science](https://docs.google.com/document/d/1yhVB9DfddvJIiXitX2ZC1W0D3cJbcvib5fWmUlgqNO0/edit)"
        ElseIf cell.Value = "VBA" Then cell.Value = "[VBA](https://docs.google.com/document/d/1ASoeI5CjFgyQTBm-HFPvmRC_94niTPx4s9crQEDVb10/edit)"
        ElseIf cell.Value = "Data Communication" Then cell.Value = "[Data Communcation](https://docs.google.com/document/d/1PTe_eezbRdZcxIOODyiQzDM4vtjVNJkVDC_7vZQSoZE/edit)"
        ElseIf cell.Value = "Reading Review" Then cell.Value = "[Reading Review](https://docs.google.com/forms/d/1JJ3pD4m_kvgERvRMuFSiDxglcJmNxvg1N8fegM7ubyA/viewform?edit_requested=true)"
        ElseIf cell.Value = "Data Exploration with Data Vis + R Intro" Then cell.Value = "[Data Exploration with Data Vis + R Intro](https://docs.google.com/document/d/1KI0OLn91_FJ03bQJW8ptoMNqOo8EL6MKzwLxvzIzNnM/edit)"
        ElseIf cell.Value = "Remember Statistics - Linear Regression" Then cell.Value = "[Remember Statistics - Linear Regression](https://docs.google.com/document/d/14MH0Qq9nTMTY1uYrVohCFPWajxAF0SO_TxA7n0LxEKA/edit?urp=gmail_link)"
        ElseIf cell.Value = "De-Annonymizing Data" Then cell.Value = "[De-Annonymizing Data](https://www.nature.com/articles/s41467-019-10933-3)"
        ElseIf cell.Value = "A Brief History of Data Visualization" Then cell.Value = "[A Brief History of Data Visualization](https://www.datavis.ca/papers/hbook.pdf)"
        ElseIf cell.Value = "Bar Graphs instead of Scatter Plots" Then cell.Value = "[Bar Graphs instead of Scatter Plots](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1002128)"
        ElseIf cell.Value = "Differnet Kinds of Data Visualization" Then cell.Value = "[Different Kinds of Data Visualization](https://github.com/arielcwebster/DataScience/blob/main/visualdatacommunication.pdf)"
        ElseIf cell.Value = "COVID Risk Calculator" Then cell.Value = "[COVID Risk Calculator](https://www.nytimes.com/2021/12/30/style/covid-risk-calculator.html)"

    'End of first if statement
     End If

    'This remove the underline for the range of cell C3 to C40
     Range("C3:C40").Font.Underline = False

    'End of the first for loop
     Next cell

    'This loop through a certain range of cells to change the text with hyperlink attached into the markdown link format for the D column except for the text in cell D18 HW 5 - ggplots & Regressions.
     For Each cell In Range("D3:D40")

    'Start of second if statement
     If cell.Value = "HW2 - VBA" Then
        cell.Value = "[HW2 - VBA](https://docs.google.com/document/d/1bTkmUon_Kq6_DupNw2Szh-T4rFGqzeA2aIIBy7m1yhk/edit)"
        ElseIf cell.Value = "Reading Due - Florence Nightengale" Then cell.Value = "[Reading Due - Florence Nightengale](https://docs.google.com/forms/d/1FBgScIpV9Vpa-jb1nlWuoCqOxFE7v5SmQtacpFHpIq8/viewform?edit_requested=true)"
        ElseIf cell.Value = "HW 3 - Tableau" Then cell.Value = "[HW 3 - Tableau](https://docs.google.com/document/d/1bta4t39rpvl-kXgO2pmZPGypWnYyBbiyzCPek9kxv9E/edit)"
        ElseIf cell.Value = "Reading - Reveal Don't Conceal" Then cell.Value = "[Reading - Reveal Don't Conceal](https://docs.google.com/forms/d/1zno4KDCz5dWahMLxWlQDUzI7sfpd2ygYqU6H_k05K-E/viewform?edit_requested=true)"
        ElseIf cell.Value = "Reading - Why Data is good for governments to provide" Then cell.Value = "[Reading - Why Data is good for governments to provide](https://www.theguardian.com/local-government-network/2013/oct/21/open-data-us-san-francisco)"
        ElseIf cell.Value = "HW 4 - Data Exploration Tableau" Then cell.Value = "[HW 4 - Data Exploration Tableau](https://docs.google.com/document/d/1GJbs8fvJn99ogIkj3jbGYEoTcw0Tgu4XyI15WOqdQfs/edit)"
        ElseIf cell.Value = "P-Hacking" Then cell.Value = "[P-Hacking](https://rss.onlinelibrary.wiley.com/doi/10.1111/1740-9713.01554)"
        ElseIf cell.Value = "Reading Due - How to un annonymize data" Then cell.Value = "[Reading Due - How to un annonymize data](https://www.theguardian.com/technology/2019/jul/23/anonymised-data-never-be-anonymous-enough-study-finds)"
        ElseIf cell.Value = "Possible Reading - Proxy Discrimination - When AI find predictive proxies for race - because society is segregated in this way. " Then cell.Value = "[Possible Reading - Proxy Discrimination - When AI find predictive proxies for race - because society is segregated in this way. ](https://ilr.law.uiowa.edu/print/volume-105-issue-3/proxy-discrimination-in-the-age-of-artificial-intelligence-and-big-data)"
        ElseIf cell.Value = "Maryland Data" Then cell.Value = "[Maryland Data](https://gopi.maryland.gov/)"
        ElseIf cell.Value = "NYT COVID Data" Then cell.Value = "[NYT COVID Data](https://github.com/nytimes/covid-19-data)"
        ElseIf cell.Value = "NOAA Data" Then cell.Value = "[NOAA Data](https://www1.ncdc.noaa.gov/pub/data/ghcn/daily/)"

    'End of second if statement
     End If

    'This remove the underline for the range of cell D3 to D40
     Range("D3:D40").Font.Underline = False

    'End of the second for loop
     Next cell

    'End of function
     End Sub`

The first for loop in this VBA code loops through the range of cells in column C from C3 to C40. There is an if statement that checks if there is a cell with a hyperlink attached first, then it can change that particular cell into the markdown link format in the range of cells at the beginning of the loop. Also, there is code that removes all underlining in of cells specified.

The second for loop in this VBA code loops through the range of cells in column D from D3 to D40. There is an if statement that checks if there is a cell with a hyperlink attached first, then it can change that particular cell into the markdown link format in the range of cells at the beginning of the loop. Also, there is code that removes all underlining in of cells specified. This loop does contain cell D18 HW 5 - ggplots & Regressions hyperlink because the teacher wants us to exclude the hyperlink attached to the text "HW 5 - ggplots & Regressions".


## This code is for removing text from a certain cell
    `Public Sub removetext()
    
       'Remove the Dead Fish Paper text from one cell
        If Range("D16").Value = "Dead Fish Paper" Then
        Range("D16").Value = ""
        End If
    
    End Sub`

The VBA code finds cell D16 in the excel sheet. It will search for the text "Dead Fish Paper" in that cell, then it can remove that text from the cell.

## This code is for removing a single hyperlink for one cell only
    `Public Sub removehyperlink()
        Range("D18").Hyperlinks.Delete
    End Sub`

The VBA code finds cell D18 in the excel sheet. It will remove the hyperlink attached to the text "HW 5 - ggplots & Regressions".

## This code changes the selected cells into a markdown table format.
    `Public Sub markdown()

        Dim cell As Range
        Dim selectedRange As Range

        Set selectedRange = Application.Selection

        Dim rowCounter As Integer
        Dim columnCounter As Integer
        Dim totalColumns As Integer
        Dim currentColumnWidth As Integer

        totalColumns = selectedRange.Columns.Count

        Dim ColumnWidth(40) As String

        '///
        '/// init lengths of columns
        '///

        For I = 0 To totalColumns
            ColumnWidth(I) = 0
        Next I

        '///
        '/// go through range to calculate maximum lengths of each column
        '///

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
            '/// go through range to add extra spaces and make create the markdown table format
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

        End Sub`

The first loop counts the number of columns in the selected range of rows the user has selected.

The second loop finds the maximum length for each column in the selected range of cells. We are comparing the current column width length to the text length of the next column. The text length of the next column is greater than the current column width length. It can now set that new length to the current column width. A counter counts the number of columns by one each time it loops.

The third loop uses the previous loop to change the selected range of column and cell into the markdown table format. A loop checks if it needs to add extra spaces to even up the table. This loop adds the signature symbol "|" of the markdown table at the beginning and the end of each cell. The for loop also checks if there is a header. The header part requires an if statement to check the current column width text length of the column first before its adds the signature symbol |, -, and the -|. 

<h1> User Guide to open macros </h1> 

## This is for those who do not have the developer ribbon in the excel ribbon

<h3>Step 1</h3>

<p>Open up a blank excel sheet. </p>

![image](https://user-images.githubusercontent.com/96843197/158244790-04de5029-bc98-43f3-87df-008d9b6a81db.png)

<h3>Step 2</h3>

<p>Right click the excel ribbon. A seperate pop up will come up.</p>

<img width="500" alt="image" src="https://user-images.githubusercontent.com/96843197/158247888-0796eace-f6af-47f9-8f34-ed6a6c5f31a1.png">

<h3>Step 3</h3>

<p>Click on the customize ribbon on the pop up then it will take you to a different window.<p>
    
![image](https://user-images.githubusercontent.com/96843197/158245377-ee924315-8dcc-4496-b6bc-5498f5ffeb81.png)
   
<h3>Step 4</h3>

<p>Once you are on The customize ribbon window you need to click on checkbox for developer ribbon and then click ok. </p>

 ![image](https://user-images.githubusercontent.com/96843197/158245051-b3b76e9b-cda2-4b53-b7c7-7dbfb75f7d68.png)

<h3>Step 5</h3> 

<p>After you click ok on the customized ribbon window the developer ribbon will appear on the excel ribbon at the top of the excel sheet. You must click on the developer tab first.</p>

![image](https://user-images.githubusercontent.com/96843197/158246766-af1c2149-fd28-4051-af0b-8dccef7e0429.png)
![image](https://user-images.githubusercontent.com/96843197/158246790-dfc1d6ed-893c-4e95-a373-702709e25ea3.png)

<h3>Step 6</h3>

<p>Once you open up the developer tab you will see in the first box of the tab. you need to click on the macros this will take you to window will you can name your macros function.</p>

![image](https://user-images.githubusercontent.com/96843197/158246914-e0540511-90c7-49e8-8490-ab46966f2ca2.png)
![image](https://user-images.githubusercontent.com/96843197/158247018-d67dd170-7ee2-458a-be79-f2755a7942db.png)

<h3>Step 7</h3>

<p>When you finished typing in the macro function name it will take you to the microsoft visual basic of application windows.</p>

<img width="700" alt="image" src="https://user-images.githubusercontent.com/96843197/158258612-33ef4b42-2f7b-4893-ba24-49b2fbff030b.png">

<h3>Step 8</h3>

<p>Type in the code in the module in the microsoft visual basic of application window</p>

<h2> This is for those who have the developer ribbon in the excel ribbon</h2>
    
<h3>Step 1</h3>

<p>Open up a blank excel sheet.</p>

<img width="960" alt="image" src="https://user-images.githubusercontent.com/96843197/158261779-51a45d6d-ccb5-4aab-90f7-d87ac053720d.png">

<h3>Step 2</h3>

<p>You must click on the developer tab first.</p>

![image](https://user-images.githubusercontent.com/96843197/158246790-dfc1d6ed-893c-4e95-a373-702709e25ea3.png)

<h3>Step 3</h3> 

<p>Once you open up the developer tab you will see in the first box of the tab. you need to click on the macros this will take you to window will you can name your macros function.</p>

![image](https://user-images.githubusercontent.com/96843197/158246914-e0540511-90c7-49e8-8490-ab46966f2ca2.png)
![image](https://user-images.githubusercontent.com/96843197/158247018-d67dd170-7ee2-458a-be79-f2755a7942db.png)

<h3>Step 4</h3>

<p>When you finished typing in the macro function name it will take you to the microsoft visual basic of application windows.</p>

<img width="700" alt="image" src="https://user-images.githubusercontent.com/96843197/158258612-33ef4b42-2f7b-4893-ba24-49b2fbff030b.png">

<h3>Step 5</h3>

<p>Type in the code in the module in the microsoft visual basic of application window</p>

<h1>This is the table without the changes</h1>

|            | Day           | Topic                                                                                                                                           | Due                                                                                                                                                                                                                                                             |
|------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|            |               |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 1/18/2021  | 1             | [What is Data Science](https://docs.google.com/document/d/1yhVB9DfddvJIiXitX2ZC1W0D3cJbcvib5fWmUlgqNO0/edit)                                    |                                                                                                                                                                                                                                                                 |
| 1/20/2021  | 2             | [VBA](https://docs.google.com/document/d/1ASoeI5CjFgyQTBm-HFPvmRC_94niTPx4s9crQEDVb10/edit)                                                     | [HW1 - Excel](https://docs.google.com/document/d/1g8eOYNe9sDmrstRgvFRZBskxjaIaD7Za4lFXSgPPkVw/edit)                                                                                                                                                               |
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
| 3/3/2021   | 13            | Logistic Regression                                                                                                                             | Dead Fish Paper                                                                                                                                                                                                                                                 |
| 3/8/2021   | 14            |                                                                                                                                                 | [P-Hacking](https://rss.onlinelibrary.wiley.com/doi/10.1111/1740-9713.01554)                                                                                                                                                                                    |
| 3/10/2021  | 15            | Work Day                                                                                                                                        | [HW 5 - ggplots & Regressions](https://docs.google.com/document/d/1TXkdIoYaQrT3uLCqSY_RbHr2jYbZPsTP4KwXppt2sN0/edit)                                                                                                                                            |
| 3/15/2021  | Spring Break  |                                                                                                                                                 |                                                                                                                                                                                                                                                                 |
| 3/17/2021  |               |                                                                                                                                                 | IRB What Data You Can Use                                                                                                                                                                                                                                       |
| 3/22/2021  | 16            | Data Annonymity                                                                                                                                 | [Reading Due - How to un annonymize data](https://www.theguardian.com/technology/2019/jul/23/anonymised-data-never-be-anonymous-enough-study-finds)                                                                                                             |
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



<h1> The result after the VBA code changes.</h1>

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
