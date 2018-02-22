# Download Questions Metadata
Use the [Download Questions Webapp](https://script.google.com/macros/s/AKfycbwPSEBYoJvjEKiPN2SnNsvPg2rpA747xuGHYs-wc6NdfemAB_Q/exec) to get the `data-item-id` for each question on your form.

Find the form id from the Google Form's edit URL.  For example, if the form's edit URL is `https://docs.google.com/forms/d/1234567890abcdefghijklmnopqrstuvwxyz_a1b2c3/edit`, its form id is `1234567890abcdefghijklmnopqrstuvwxyz_a1b2c3`.  For more information click [here](https://developers.google.com/apps-script/reference/forms/form-app#openbyidid). 

*Note: you may need to review permissions and allow this app to run on your Google Drive.*

*Note: if you get this error message: `No item with the given ID could be found, or you do not have permission to access it. (line 53, file "Code", project "Download Questions")`, check that you can to open the form with edit permissions at URL `https://docs.google.com/forms/d/<YOUR_FORM_ID>/edit`.*
