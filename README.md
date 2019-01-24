# Agile MVC Live Project --> Schedule-It

## TABLE OF CONTENTS
* [Technologies Used](#Technologies-Used)
* [Introduction](#Introduction)
* [Stories](#Stories)


## TECHNOLOGIES USED
  **Languages:** C#, T-SQL, JavaScript, HTML, CSS
  
  **Frameworks/Libraries:**  ASP.NET MVC, Entity Framework, jQuery, Bootstrap, FullCalendar, MomentJS
  
  **Version Control:** Git, GitHub, Team Foundation Server
  
  **Project Tools:** Visual Studio, SQL Server, Azure DevOps, Chrome Developer Tools, Edge Developer Tools


## INTRODUCTION



## STORIES
### FullCalendar Stories
* **3405 Implement CRUD Operations on TimeOffEvens**
  * 3413 Create a Details Modal
  * 3408 Create Delete Feature
  * 3409 Enable Reading and Loading of Events on Calendar
  * 3410 Implement an Events Creation Feature
  * 3411 Implement an Update Feature
  * 3412 Make Calendar Events Visually Responsive
* **3428 Add Features in TimeOffEvents/Create and Fix Runtime Errors**
  * 3437 Enable View Persistence on Calendar
  * 3433 Fix Runtime Errors
  * 3432 Implement Calendar Event Resizing Feature
  * 3429 Implement Calendar Events Drag and Drop Capabilities
  * 3434 Prevent Edit Modal From Closing Automatically If Save Is Unsuccessful
  * 3435 Prevent Users From Creating Events Shorter Than 15 Minutes
  * 3436 Found Event Start and End Times to the Nearest 15 Minute Increments
* **Additional Enhancements**
  * Update TimeOffEvent Approval Status From Database When DetailsModal Opens
### Other Minor Stories      
      
      
      
      
      
      
      
      
      
 
3405 Implement CRUD operations on TimeOffEvents:   
See 3408,  3409, 3410, 3411, 3412, 3413 
3413 Create a details modal:  When the user clicks on an existing event, create a modal that displays the event details in plain text.  Include an Edit button that opens an edit modal for making changes. 
3408 Create delete feature:  When the user clicks on an existing event, create a modal that displays the event details in plain text.  Include an Edit button that opens an edit modal for making changes. 
3409 Enable reading and loading of events on calendar:  Read entries from Events table pertaining to Time Off Events and populate the calendar 
3410 Implement an events creation feature:  When the user clicks a time slot on Calendar or selects a time range, open an edit modal with the corresponding start and end times pre-entered into time inputs 
3411 Implement an update feature:  When the user clicks on an existing event, open an edit modal with form inputs pre-populated with event data, and allow users to make changes, and a Save button to save and update that entry in the database.  Also include button to cancel the edit and to delete the event. 
3412 Make calendar events visually responsive:  When a user makes adjustments to the start/end times of either an existing event or a brand-new selection, cause the event to update visually on the calendar while the edit modal is displayed.  However, if the user does not save the event and exits the modal, visually restore the event to the original state (i.e. existing event returns to original state, and brand-new selection disappears) 
 
3428 Add features in TimeOffEvents/Create and fix runtime errors: 
See 3429, 3432, 3433, 3434, 3435, 3436, 3437 
3437 Enable view persistence on calendar:  Currently, whenever a change is made to the calendar, the view would return to the default, i.e. monthly view.  Implement a feature where if the user selects the weekly view, it will remain after changes are made to the calendar. 
3433 Fix runtime errors:   
-Occasionally the delete button would show for a brand-new selection. 
-Occasionally the times in the input fields would mismatch the onscreen event. 
3432 Implement calendar event resizing feature:  When the user resizes an existing event, display the edit modal with updated start and end times pre-populated 
3429 Implement calendar events drag and drop capabilities:  When the user drags an existing event to a new time, display the edit modal with updated start and end times pre-populated 
3434 Prevent edit modal from closing automatically if save is unsuccessful:  Allow users to continue editing if a save attempt is unsuccessful, until the user closes the modal manually 
3435 Prevent users from creating events shorter than 15 minutes 
3436 Round event start and end times to the nearest 15 minute increments: 
-Date pickers in browsers such as Edge do not restrict time values.  Therefore, when the user attempts to save an event, round the times to the nearest 15 minute increments.   
-For browsers that do support value control, such as Chrome, cause time to change 15 minutes at a time. 
