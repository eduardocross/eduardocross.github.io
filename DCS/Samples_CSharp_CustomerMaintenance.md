---
title: C# Customer Maintenance Sample

Id: Samples_CSharp_CustomerMaintenance
TocParent: Samples_CSharp_Main
TocOrder: 3

keywords: customer maintenance, C# sample [DCS 16.0]
keywords: examples, DCS for Visual Studio 2019
keywords: examples [DCS 16.0 customer maintenance
keywords: samples, DCS for Visual Studio 2019
keywords: DCS for Visual Studio 2019, C# customer maintenance sample
keywords: DCS for Visual Studio 2019, C# samples
keywords: positioning to the first record [DCS 16.0 C# sample
keywords: positioning to the last record [DCS 16.0 C# sample
keywords: positioning to the next record [DCS 16.0 C# sample
keywords: positioning to the previous record [DCS 16.0 C# sample

---

The **Customer Maintenance** C# Windows program uses ASNA DCS for Visual Studio 2019 to Read, position, Update, Delete Records from an iSeries type database. It illustrates how you can readily gain access to record level information on an iSeries computer. 

**To run this sample** 

1. Copy the **Customer_Maintenance**  example folder from the **C#** 
						language folder to your local application working folder.  The folder can 
						be found at the following location - **C:\Program Files\ASNA\Examples\DCS 
						11.2\C#.**
2. Select **File - Open Solution** 
					in Visual Studio 2019.
3. Open the solution called **Customer Maintenance** , which is 
						located in the **Customer_Maintenance** 
					folder in the location you specified in step 1.
4. **Build** 
					the solution by selecting Build - Build Solution (Ctrl+Shift+B).
5. Press **F5**  to run the program. 

Remarks

<dl><dt>This example uses DCS to:
			</dt><dt /></dl>
**Position to the First Record in a file.** 

Event fires when user presses the first record button – "|&lt;".

**Position to the Previous Record in a file.** 

Event fires when user presses the previous record button – "&lt;".

**Position to the Next Record in a file.** 

Event fires when user presses the next record button – "&gt;".

**Position to the Last Record in a file.** 

Event fires when user presses the last record button – "&gt;|".

**Position to a specific record (Randon Read) in a file.** 

Event fires when user enters an Customer Number (100 – 100000) and presses the get customer record button.

**Add a new record to the file.** 

Event fires when user fills in the necessary data and presses the Add record button.

**Update the current Record of the file.** 

Event fires when user changes a field and presses the update record button.

**Delete the current Record of the file.** 

Event fires when user presses the delete record button.

***Error Handling*** has been added to show more meaningful messages for 

a) End-of-File

b) File Not Found

c) Customer Not Found

See Also

[Samples](Samples_Main.html) 
