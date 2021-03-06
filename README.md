# How to create a waitlist using Google Form

# Contents
- Select a method to set up a waitlist on Google Form:

|         | [**Spreadsheet Method**](spreadsheet-method) | [**Form Method**](form-method)  |
| ------------- |:-------------| :-----|
| *Uses add-on:* | [formRanger](https://chrome.google.com/webstore/detail/formranger/faepkjkcpnnghgdhiobglpppbfdnaehc?hl=en) | unverified add-on developed in-house |
| *Handles drop-outs and changes:* | - By editing the responses recorded in the form's linked spreadsheet.<br/> - Changes made in the form's **Reponses** tab will be ignored. | - By editing the responses in the form's **Reponses** tab.<br/> - Changes made in the form's linked spreadsheet will be ignored. |
| *Benefits:* | - Easy to change input parameters such as class limit, display text, original options etc.<br/> - Easy to display enrollment data such as current number of seats taken, revised waitlist options etc. | - More robust to accidental changes in spreadsheet.<br/> - Flexibility to develop custom features. |
| *Drawbacks:* | - Accidental changes in spreadsheet may break calculations.<br/> - Accidental changes to exported columns can undesirably cause formRanger to pick up additional options to display on form. | - Developing user-interface is time-consuming, may not be worth-it for one-time use.<br/> - If no user-interface, learning curve for form admin to change input parameters in the [Script editor](https://developers.google.com/apps-script/guides/bound).<br/> - Using unverified add-on requires copy/pasting code, difficult to maintain/distribute code changes.  Or hassle to go through [publishing process](https://developers.google.com/apps-script/add-ons/publish) involving verification and review by Google. |
 
 
- [Data Validation](data-validation): [demo](https://docs.google.com/forms/d/11O0dxNVd995oLX95Ix-tns1h9xJPSjglJPdBx0jVkoI/edit?usp=sharing) for validation of phone number, zip code, and email address.

- [Data Analysis](data-analysis): [demo](https://docs.google.com/spreadsheets/d/1yYc1ecmeawc0_VqBrXIaNytGSHoxWJghUWh-cW0o8iM/edit?usp=sharing) renders Google Form's data dump of responses into a more readable format -- wide form and long form -- in the form's linked spreadsheet.

- [Data Export](data-export): [demo](https://docs.google.com/spreadsheets/d/1WGlJ7q8yTo78v4WL7p6eJW-cHkKmsTrFZwVMtWkmwvU/edit?usp=sharing) uses the [IMPORTRANGE](https://support.google.com/docs/answer/3093340) function to copy out results (selected ranges) from the data analysis spreadsheet.

- [Embed Form on Website](embed-form): here's an [example](/embed.html).
