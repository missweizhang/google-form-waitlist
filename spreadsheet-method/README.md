# Spreadsheet Method
The method gathers responses collected in the form's linked Google Sheet, stored in the 'Form Responses 1' tab, to compute number of responses (seats taken) for each option of a multiple choice question (Checkbox, Multiple Choice, or Dropdown).  Given a limit for the maximum number of responses allowed for each option, and other paramters specified in the 'waitlist' tab of the linked spreadsheet, we can then compute waitlist positions and replacement text for the options on the form.  The revised options are exported into the 'waitlist options' tab, which the formRanger add-on reads and uses to populate the original Google Form.  Below are the step-by-step instructions on how to set this up.

   ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) ***IMPORTANT NOTE!** changes options will not appear on the Google Form until **Auto-repopulate questions: Every hour** is toggled **ON** then **OFF** in the [formRanger add-on](https://chrome.google.com/webstore/detail/formranger/faepkjkcpnnghgdhiobglpppbfdnaehc?hl=en), or until the next form submission.  If any of the waitlist settings are changed in the Spreadsheet, such as class limit, display text, original options, these changes will also not be reflected on the Google Form until **Auto-repopulate questions: Every hour** is toggled **ON** then **OFF**, or until the next form submission.*

## Contents
   [Link Form to Spreadsheet](#link-form-to-spreadsheet) 
   
   [Configure Waitlist](#configure-waitlist) 
   
   [Import Waitlist Options](#import-waitlist-options) 
   
   [Install and set up FormRanger](#install-and-set-up-formranger) 
   
   

## Link Form to Spreadsheet
*Tip: If you want to keep columns for certain questions (such as Q1, Q3, Q5) together on the spreadsheet, even though these questions are not adjacent on the form (such as Q1, Q2, Q3, Q4, Q5), you can try adding certain questions (such as Q2, Q4) after linking to the spreadsheet.  Then columns for the questions added later (Q2 and Q4) might go to the far right of the 'Form Responses 1' sheet, keeping the initial columns (Q1, Q3, Q5) adjacent.*

*For the Camptoons form, this means adding the checkbox questions for extended care after linking to spreadsheet.*

1. On **Google Form**, add all questions except the ones whose columns you want to go to the far right of the spreadsheet.

2. Link to spreadsheet: go to the **Responses** tab, and click on the green spreadsheet icon ![alt-text](https://lh3.googleusercontent.com/R7OAlMl_8iPpOQOsaMX-MWd9_Vvrsqc7nQ6Aidts68Mdof-jkuHR_QV5GGo4Ky8JJbfZ=w18).  You might be directed to **Select response destination** if your form is not already linked.

3. Open your destination spreadsheet in **Google Sheets**.  Its name might be *CampToons Reg form (Responses)*.  Make sure that submitted responses go to the tab named 'Form Responses 1'.  If not, rename the destination tab to  'Form Responses 1' .

4. If the form has changed since linking, re-link by clicking the green spreadsheet icon ![alt-text](https://lh3.googleusercontent.com/R7OAlMl_8iPpOQOsaMX-MWd9_Vvrsqc7nQ6Aidts68Mdof-jkuHR_QV5GGo4Ky8JJbfZ=w18) on the form's **Responses** tab, and make sure added/edited question titles appear in the order desired on row 1 of the 'Form Responses 1' tab in the spreadsheet.  This might take a minute or two.



## Configure Waitlist
1. From the [demo spreadsheet](https://docs.google.com/spreadsheets/d/1r9sEmRzMkriqzULdU5QX76499oI-KrlleShLuFsjFxs/edit?usp=sharing), right click on the 'waitlist' tab, select **Copy to...**, and select your form's destination spreadsheet (such as *CampToons Reg form (Responses)*).  **Select** and **OK**.

2. Open your destination spreadsheet, right click on the 'Copy of waitlist' tab, select **Rename...** and rename it to 'waitlist'.

3. Fix the **Invalid** error (red triangles in cell's top-right corner) appearing in row 22's question titles.
   ![alt-text](../img/invalid_error.png)

   Use the drop-down menu to select the appropriate question titles for each cell in row 22, until all errors disappear from rows 22, 24 and 25.  The drop-down menu contains all the question titles listed in the header row (row 1) of the 'Form Responses 1' tab.

   ![alt-text](../img/select_question_title.png)
   
   ![#1589F0](https://placehold.it/15/1589F0/000000?text=+) ***NOTE**: [formRanger](https://chrome.google.com/webstore/detail/formranger/faepkjkcpnnghgdhiobglpppbfdnaehc?hl=en) only works with question types that support choices, i.e. Multiple Choice, Checkbox, or Dropdown.  Contact [narrow.wei@gmail.com] if you need to use question types that support grid, i.e. Multiple choice grid, or Checkbox grid.*

   ![#1589F0](https://placehold.it/15/1589F0/000000?text=+) ***NOTE**: You can ignore the data-item-id if you are using [formRanger](https://chrome.google.com/webstore/detail/formranger/faepkjkcpnnghgdhiobglpppbfdnaehc?hl=en).*
   
4. Set enrollment limit for each class in rows 2-7 of the 'waitlist' tab.  This is the number of seats available before reaching the waitlist.

5. Set text to display in rows 17 and 19 for before and after reaching the waitlist, using replacement text ${Option}, ${Remaining}, ${Limit}, and ${Position}.  Be sure to NOT use commas in the display text, as we Google form records responses containing multiple selections as comma separated values, and so we will separate them using the comma delimiter.

6. Set text for the original set of multiple choice options in cells A26:A31.  The table should automatically populate with revised options for each question, depending on the number of seats taken (rows 9-15) as calculated from the 'Form Responses 1' tab.

   ![#1589F0](https://placehold.it/15/1589F0/000000?text=+) ***NOTE**:: If you need to use different sets of original options, create separate tables, one for each set of original options.*
 


## Import Waitlist Options
1. From the [demo spreadsheet](https://docs.google.com/spreadsheets/d/1r9sEmRzMkriqzULdU5QX76499oI-KrlleShLuFsjFxs/edit?usp=sharing), right click on the 'waitlist options' tab, select **Copy to...**, and select your form's destination spreadsheet (such as *CampToons Reg form (Responses)*).  **Select** and **OK**.

2. Open your destination spreadsheet, right click on the 'Copy of waitlist options' tab, select **Rename...** and rename it to 'waitlist options'.

3. Make sure that rows beneath the imported table of revised options are empty, or formRanger will pick these up as additional options.  It is highly recommended that the 'waitlist options' tab is locked to give collaborators read-only access.  To lock this tab, go to **Data -> Protected sheets and ranges...**.  In the sidebar, click **Add a sheet or range**, click on **Sheet**, select the sheet 'waitlist options', click **Set permissions**.  In the dialog, select **Restrict who can edit this range** and choose who can edit.   

   ![alt-text](../img/formranger_options.png)
   ![alt-text](../img/protect_sheet_only_you_can_edit.png)
   ![alt-text](../img/protect_sheet.png)



## Install and set up FormRanger
1. Install the [formRanger add-on](https://chrome.google.com/webstore/detail/formranger/faepkjkcpnnghgdhiobglpppbfdnaehc?hl=en) from the webstore.

2. In **Google Form**, click on the add-on icon, and click on **formRanger**, from the menu click **Start**.

   ![alt-text](../img/formranger_addon.png)
   In the formRanger sidebar, the **Question list** will show all the questions in your form that support choice, i.e. Multiple Choice, Checkbox, or Dropdown questions.

3. Select the question to replace options with waitlist options, check the box for **Populate from range**, and click the *+* icon to select a **New range**.

   ![alt-text](../img/formranger_sidebar.png)

4. In the **Add new range** window's **Select sheet** tab, choose the destination spreadsheet, **Select**.  In the **Select range** tab, choose 'waitlist options' under **Sheet name**, and choose the appropriate question title under **Column header**.  You may choose to enter a name if you like.  
   Repeat for each question whose options are to be replaced with the waitlist options.

5. In the formRanger sidebar, turn **ON** the switch for **Auto-repopulate questions: On form submit**.

   ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) ***IMPORTANT NOTE!** changes options will not appear on the Google Form until **Auto-repopulate questions: Every hour** is toggled **ON** then **OFF**, or until the next form submission.  If any of the waitlist settings are changed in the Spreadsheet, such as class limit, display text, original options, these changes will also not be reflected on the Google Form until **Auto-repopulate questions: Every hour** is toggled **ON** then **OFF**, or until the next form submission.*
   
   ![#1589F0](https://placehold.it/15/1589F0/000000?text=+) ***NOTE**: To restore original options to a question, repeat steps 3 and 4, and when formRanger asks for **Column header** choose column A "Question Title".*
   
## Alternate Methods
[Form Method](../form-method) 
