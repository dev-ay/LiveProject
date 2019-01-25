# AGILE MVC LIVE PROJECT: Schedule-It (..under construction...)

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
### FullCalendar Stories:
* **3174 Add a one week fullCalendar to the tempSchedule/Create view**
* **3189 Make a few changes to the ScheduleTemplate / Create view. See Tasks**
  * 3192 clicking on a day on the calendar should pop up a modal
  * 3191 make the calendar display as just a one week view. you may need to do some research on fullcalendar
  * 3190 Remove the notes input box and the create button
  * 3195 The modal should have a checkbox for "Day Off"
  * 3193 the modal should have an input for start and end time
  * 3194 The start and end time inputs should be time pickers that are easy for a user to use. look at bootstrap time pickers
* **3209 Implement a mouse hand cursor on hover over calendar**
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
### Other Minor Stories:
* 3108 Rename Model.ID 
* 3109 Redirect "Manage" button 
* 3111 Modify "Mail" button on the nav-bar 
* 3113 Change ScheduleId type 
* 3121 Add a PayPeriod controller with views
* 3110 Remove TemplateID from Schedule model
* 3126 Add "Request Time Off" to nav menu 
* 3127 Add a button to the navigation drop down to shift/create
* 3131 Add a link to the navigation dropdown leading to the TempSchedule / Index page
* 3130 On the Schedule model, change the UserId from a string to a Guid. This will require a migration
* 3141 On the PayPeriods / Create view, add some text to the "Pay Period Length" label so that is says "Pay Period Length (Days)"
* 3137 Fix the Schedule / Create bug
* 3135 On the TimeOffEvent Create view, remove the input boxes from the top
* 3134 Fix the Messages / Inbox bug
* 3142 On the Message controller, change the create method so that DateSent is set to the current time
* 3143 Fix the Message / Create bug
* 3145 On the index/home view, Remove the clock out button and make the clock in button say simply "Clock".  Then center all content on home/index view
* 3157 On the TempSchedule controller, change the Create function so that the DateCreated property gets set to the current time
* 3168 Remove the Payperiods / Details view. Dont forget to include your .csproj file with your changes
* 3172 Implement the modal found in the TimeOff/Create view into the Schedule/Create view

* 3178 On the Event model, make the End property nullable. This will require a migration
* 3206 Revise the ScheduleTemplate model

* 3176 On the TimeOffEvent controller, create a function that will generate a message for every admin in the user table. Only define the function, do not call it just yet
* 3213 Add 3 admin users to the seed data. look at migrations > configuration


      
      
      
      
      
      
      
      
# FullCalendar Stories:
## 3189 Make a few changes to the ScheduleTemplate / Create view  
> **Details:**
> Parent story.  Please see 3192, 3191, 3190, 3195, 3193, 3194  
    ### Solution:  
## 3192 clicking on a day on the calendar should pop up a modal
    ### Solution: 
## 3191 make the calendar display as just a one week view. you may need to do some research on fullcalendar
    ### Solution: 
## 3190 Remove the notes input box and the create button
    ### Solution: 
## 3195 The modal should have a checkbox for "Day Off" 
    ### Solution: 
## 3193 the modal should have an input for start and end time 
    ### Solution: 
## 3194 The start and end time inputs should be time pickers that are easy for a user to use. look at bootstrap time pickers 
    ### Solution: 
## 3209 Implement a mouse hand cursor on hover over calendar
> When the user hovers over any of the calendars, the cursor should change to reflect that the calendar is clickable.  
> This story is for all of the calendars.  This includes the schedule create view, the tempschedule create view, and the timeoffevent create view.  
    ### Solution: 
## 3405 Implement CRUD operations on TimeOffEvents  
> **Details:**  
> Parent story.  See 3408, 3409, 3410, 3411, 3412, 3413  
## 3413 Create a details modal  
> **Details:**  
> When the user clicks on an existing event, create a modal that displays the event details in plain text.  Include an Edit button that opens an edit modal for making changes.  
    ### Solution: 
## 3408 Create delete feature  
> **Details:**  
> When the user clicks on an existing event, create a modal that displays the event details in plain text.  Include an Edit button that opens an edit modal for making changes.  
    ### Solution: 
## 3409 Enable reading and loading of events on calendar  
> **Details:**  
> Read entries from Events table pertaining to Time Off Events and populate the calendar  
    ### Solution: 
## 3410 Implement an events creation feature  
> **Details:**  
> When the user clicks a time slot on Calendar or selects a time range, open an edit modal with the corresponding start and end times pre-entered into time inputs  
    ### Solution: 
## 3411 Implement an update feature  
> **Details:**  
> When the user clicks on an existing event, open an edit modal with form inputs pre-populated with event data, and allow users to make changes, and a Save button to save and update that entry in the database.  Also include button to cancel the edit and to delete the event.  
    ### Solution: 
## 3412 Make calendar events visually responsive  
> **Details:**  
> When a user makes adjustments to the start/end times of either an existing event or a brand-new selection, cause the event to update visually on the calendar while the edit modal is displayed.  However, if the user does not save the event and exits the modal, visually restore the event to the original state (i.e. existing event returns to original state, and brand-new selection disappears) 
    ### Solution: 
## 3428 Add features in TimeOffEvents/Create and fix runtime errors  
> **Details:**  
> Parent story.  See 3429, 3432, 3433, 3434, 3435, 3436, 3437  
## 3437 Enable view persistence on calendar  
> **Details:**  
> Currently, whenever a change is made to the calendar, the view would return to the default, i.e. monthly view.  Implement a feature where if the user selects the weekly view, it will remain after changes are made to the calendar.  
    ### Solution: 
## 3433 Fix runtime errors  
> **Details:**  
> &nbsp;&nbsp;\- Occasionally the delete button would show for a brand-new selection.  
> &nbsp;&nbsp;\- Occasionally the times in the input fields would mismatch the onscreen event.  
    ### Solution: 
## 3432 Implement calendar event resizing feature  
> **Details:**  
> When the user resizes an existing event, display the edit modal with updated start and end times pre-populated  
    ### Solution: 
## 3429 Implement calendar events drag and drop capabilities  
> **Details:**  
>When the user drags an existing event to a new time, display the edit modal with updated start and end times pre-populated  
    ### Solution: 
## 3434 Prevent edit modal from closing automatically if save is unsuccessful  
> **Details:**  
> Allow users to continue editing if a save attempt is unsuccessful, until the user closes the modal manually  
    ### Solution: 
## 3435 Prevent users from creating events shorter than 15 minutes  
    ### Solution: 
## 3436 Round event start and end times to the nearest 15 minute increments  
> **Details:**  
> &nbsp;&nbsp;\- Date pickers in browsers such as Edge do not restrict time values.  Therefore, when the user attempts to save an event, round the times to the nearest 15 minute increments.   
> &nbsp;&nbsp;\- For browsers that do support value control, such as Chrome, cause time to change 15 minutes at a time.  
    ### Solution: 











# Other Minor Stories
## 3108 Under Views\Schedule\Create.cshtml change Model.ID to Model.Id
## 3109 "Manage" button under the navigation button should bring you to the manage index view, not the schedule index view
## 3111 Remove the text from the mail button on the nav-bar. It should just be an icon
## 3113 On the ScheduledWorkPeriod model, change the ScheduleId to be a Guid type
## 3121 Add a PayPeriod controller with views for Index, Create, Delete, Edit etc
## 3110 Remove TemplateID from schedule model.  This change will require a migration
## 3126 Add a link to the navigation drop-down titled "Request Time Off" that takes the user to the TimeOffEvent / Create page
## 3127 Add a button to the navigation drop down to shift/create
## 3131 Add a link to the navigation dropdown leading to the TempSchedule / Index page
## 3130 On the Schedule model, change the UserId from a string to a Guid. This will require a migration
## 3141 On the PayPeriods / Create view, add some text to the "Pay Period Length" label so that is says "Pay Period Length (Days)"
## 3137 Fix the Schedule / Create bug
## 3135 On the TimeOffEvent Create view, remove the input boxes from the top
## 3134 Fix the Messages / Inbox bug
## 3142 On the Message controller, change the create method so that DateSent is set to the current time.
## 3143 Fix the Message / Create bug
## 3145 On the index/home view, Remove the clock out button and make the clock in button say simply "Clock".  Then center all content on home/index view
## 3157 On the TempSchedule controller, change the Create function so that the DateCreated property gets set to the current time
## 3168 Remove the Payperiods / Details view. Dont forget to include your .csproj file with your changes
## 3172 Implement the modal found in the TimeOff/Create view into the Schedule/Create view
## 3174 Add a one week fullCalendar to the tempSchedule/Create view
## 3178 On the Event model, make the End property nullable. This will require a migration
## 3206 Revise the ScheduleTemplate model
> **Details:**
> Properties should look somewhat like the schedule model. 
> [key] guid Id 
> string Title 
> List<ScheduledWorkPeriod> ScheduledWorkPeriods 
> dont forget migration  

## 3176 On the TimeOffEvent controller, create a function that will generate a message for every admin in the user table. Only define the function, do not call it just yet. 
## 3213 Add 3 admin users to the seed data. look at migrations > configuration 





