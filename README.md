# AGILE FULLSTACK MVC LIVE PROJECT: Schedule-It 
### (...Page still under construction. Please check back for updates...)

<p align="center">
  <img src="/img/SI-header.png" alt="Live Project Header"/>
</p>

<br/>

___

## TABLE OF CONTENTS
1. **[TECHNOLOGIES USED](#Technologies-Used)**
2. **[OVERVIEW](#Overview)**
3. **[FULLCALENDAR STORIES](#FULLCALENDAR-STORIES)**
  * [3174-Add a one week fullCalendar to the tempSchedule/Create view][3174]
  * [3189-Make a few changes to the ScheduleTemplate / Create view. See Tasks][3189]
    * [3192-clicking on a day on the calendar should pop up a modal][3192]
    * [3191-Modify calendar to display one week view][3191]
    * [3190-Remove the notes input box and the create button][3190]
    * [3195-The modal should have a checkbox for "Day Off"][3195]
    * [3193-The modal should have an input for start and end time][3193]
    * [3194-Implement user-friendly time pickers][3194]
  * [3209-Implement a mouse hand cursor on hover over calendar][3209]
  * [3405-Implement CRUD Operations on TimeOffEvens][3405]
    * [3413-Create a Details Modal][3413]
    * [3408-Create Delete Feature][3408]
    * [3409-Enable Reading and Loading of Events on Calendar][3409]
    * [3410-Implement an Events Creation Feature][3410]
    * [3411-Implement an Update Feature][3411]
    * [3412-Make Calendar Events Visually Responsive][3412]
  * [3428-Add Features in TimeOffEvents/Create and Fix Runtime Errors][3428]
    * [3437-Enable View Persistence on Calendar][3437]
    * [3433-Fix Runtime Errors][3433]
    * [3432-Implement Calendar Event Resizing Feature][3432]
    * [3429-Implement Calendar Events Drag and Drop Capabilities][3429]
    * [3434-Prevent Edit Modal From Closing Automatically If Save Is Unsuccessful][3434]
    * [3435-Prevent Users From Creating Events Shorter Than 15 Minutes][3435]
    * [3436-Found Event Start and End Times to the Nearest 15 Minute Increments][3436]
  * [Additional Enhancements](#Additional-Enhancements)
    * [Update TimeOffEvent Approval Status From Database When DetailsModal Opens][A]
    * [Modify Test Entries in Seed Data To Begin Dynamically On Current Week][B]
    * [Modify calendar display preperties based on viewport size][C]
    * [Implement persistence of displayed time range across sessions][D]
4. **[OTHER STORIES](#OTHER-STORIES)**
  * [3108-Rename Model.ID][3108]
  * [3109-Redirect "Manage" button][3109]
  * [3111-Modify "Mail" button on the nav-bar][3111]
  * [3113-Change ScheduleId type][3113]
  * [3121-Add a PayPeriod controller with views][3121]
  * [3110-Remove TemplateID from Schedule model][3110]
  * [3126-Add "Request Time Off" to nav menu][3126]
  * [3127-Add Shift/Create to nav menu][3127]
  * [3131-Add TempSchedule/Index to nav menu][3131]
  * [3130-Change Schedule model UserId type][3130]
  * [3141-Modify "Pay Period Length" label][3141]
  * [3137-Fix the Schedule/Create bug][3137]
  * [3135-Remove Inputs boxes from TimeOffEvent/Create][3135]
  * [3134-Fix the Messages/Inbox bug][3134]
  * [3142-Set Message/Create DateSent to the current time][3142]
  * [3143-Fix the Message/Create bug][3143]
  * [3145-Rearrange and modify Home/Index view][3145]
  * [3157-Set TempSchedule/Create DateCreated to the current time][3157]
  * [3168-Remove the Payperiods/Details view][3168]
  * [3172-Implement Schedule/Create modal][3172]
  * [3178-Make Event model End property nullable][3178]
  * [3206-Revise the ScheduleTemplate model][3206]
  * [3176-Implement message-all feature in TimeOffEvent controller][3176]
  * [3213-Add 3 more admin users to the seed data][3213]

<br />

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) >*

<br/>

___

## TECHNOLOGIES USED
  **Languages:**&nbsp;&nbsp;C#, T-SQL, JavaScript, HTML, CSS
  
  **Frameworks/Libraries:**&nbsp;&nbsp;ASP.NET MVC, Entity Framework, jQuery, Bootstrap, FullCalendar, MomentJS
  
  **Version Control:**&nbsp;&nbsp;Git, Team Foundation Server
  
  **Project Tools:**&nbsp;&nbsp;Visual Studio, SQL Server, Azure DevOps, Chrome Developer Tools, Edge Developer Tools, Google Hangout, Slack  

<br />

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Technologies Used](#TECHNOLOGIES-USED) >*

<br/>

___

## OVERVIEW
This is an Agile/SCRUM live project that I participated in at the Tech Academy for a production clock-in software.  The overall project occurs over many months, but my personal participation was over a single 2-week sprint.  This Readme only lists the stories assigned to me.

**Overall Product Features:**  
<img align="right" src="/img/SI-DragDrop-Thumbnail.png" alt="Drag and Drop Thumbnail"/>
The ultimate scope of the end product was an employee clock-in fullstack MVC web application with the following features:
  * Users can clock-in their work time
  * Users can request time off and admins can view requests and approve
  * Users can create multi-purpose schedules and create schedule templates
  * Users can create temporary schedules to substitute long-term schedules
  * Users can view their pay over flexible windows of time
  * Users can message other users
  * Implement a visual calendar system
  * Implement user authentification
  * Various other features
  * See [Technologies Used](#Technologies-Used)

### **Project Format:**
This was a multiple-month SCRUM project.  At the time of my participation, there were around 15 members on the team, many of them remote.  We held daily stand-up meetings over Google Hangout discussing our progress from the previous day as well as upcoming tasks.  We also held occassional story-building sessions to discuss and brainstorm overall product features and design.  Team members sought and offered help from and to one another through Slack.  We used Microsoft's Azure DevOps online project management system to track each story through "New", "Active", "Resolved", and "Closed" phases. During the first half of my sprint we used Microsoft's Team Foundation Server version control system to make commits and merge every team member's work.  During the second half we migrated over to Git version control instead.  

The structure of the software is an ASP.NET MVC Application using Code-First Entity Framework to manage a SQL Server database.  We used Visual Studio Community for development with version control extensions. See [Technologies Used](#Technologies-Used).

### **My Role:**  
My role on the project was a 2-week-long sprint, and this readme details the stories assigned to me.  My most significant contribution was the creation of a fully functional visual Calendar. I created backend CRUD methods that utilized Entity Framework to access a database.  On the frontend I largely relied on jQuery, and utilized AJAX to communicate with the backend.  The features of my calendar system include the following:  

<img align="left" src="/img/SI-Day-Week-Thumbnail.png" alt="Agenda Week Thumbnail"/>

* Performs all CRUD operations
* Enables creation of event by selecting time range on calendar
* Enables mouse-based resizing and dragging and dropping to modify calendar events
* Provides edit modal where users can edit event details using form inputs
* Enables visually responsive calendar events that update based on changes to input times on edit modal
* Utilizes AJAX to only update relevant data when needed
* Provides monthly calendar view, and weekly agenda view
* Allows all day events as well as hourly events
* Permits dragging and dropping of events between all day and agenda sections
* Displays unapproved events in silver, and approved events in green
* Utilizes AJAX to occassionally check for event approval status
* Various other features

Initially I reloaded the calendar after each event update, as that was the most straightforward way to ensure the calendar precisely reflects the backend database.  This approach was not unreasonably slow.  However, in the interest of providing the best user experience, I decided to modify my program design so that the backend database and frontend calendar were updated separately.  My motivation for this was to optimize the program for potentially slow network connections and to operate as efficiently as possible for the end user.  

After my sprint concluded, I continued to make enhancements to the program on my own out of curiosity.  These changes are listed under [Additional Enhancements](#Additional-Enhancements).

For the highlights of my work on this live project I recommend you jump to the following sections:  
  * [3405-Implement CRUD Operations on TimeOffEvens][3405]
  * [3428-Add Features in TimeOffEvents/Create and Fix Runtime Errors][3428]
  * [Additional Enhancements](#Additional-Enhancements)

<br />

*Note: The 4-digit number in front of each story is the associated work item number from the version control systems.   I have listed the stories in the order in which I completed them or by context, so you will often notice the numbers being listed out of numeric order.*

*Note: Per request from end customer I will not be uploading source code files to my GitHub repository.  However, I have permission to include code snippets and screenshots in this readme file.*

<br />

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Overview](#OVERVIEW) >*

<br/>

___


# FULLCALENDAR STORIES:
This section includes stories relating to the operation of, and interactions with, calendars
  * [3174-Add a one week fullCalendar to the tempSchedule/Create view][3174]
  * [3189-Make a few changes to the ScheduleTemplate / Create view. See Tasks][3189]
    * [3192-clicking on a day on the calendar should pop up a modal][3192]
    * [3191-Modify calendar to display one week view][3191]
    * [3190-Remove the notes input box and the create button][3190]
    * [3195-The modal should have a checkbox for "Day Off"][3195]
    * [3193-The modal should have an input for start and end time][3193]
    * [3194-Implement user-friendly time pickers][3194]
  * [3209-Implement a mouse hand cursor on hover over calendar][3209]
  * [3405-Implement CRUD Operations on TimeOffEvens][3405]
    * [3413-Create a Details Modal][3413]
    * [3408-Create Delete Feature][3408]
    * [3409-Enable Reading and Loading of Events on Calendar][3409]
    * [3410-Implement an Events Creation Feature][3410]
    * [3411-Implement an Update Feature][3411]
    * [3412-Make Calendar Events Visually Responsive][3412]
  * [3428-Add Features in TimeOffEvents/Create and Fix Runtime Errors][3428]
    * [3437-Enable View Persistence on Calendar][3437]
    * [3433-Fix Runtime Errors][3433]
    * [3432-Implement Calendar Event Resizing Feature][3432]
    * [3429-Implement Calendar Events Drag and Drop Capabilities][3429]
    * [3434-Prevent Edit Modal From Closing Automatically If Save Is Unsuccessful][3434]
    * [3435-Prevent Users From Creating Events Shorter Than 15 Minutes][3435]
    * [3436-Found Event Start and End Times to the Nearest 15 Minute Increments][3436]
  * [Additional Enhancements](#Additional-Enhancements)
    * [Update TimeOffEvent Approval Status From Database When DetailsModal Opens][A]
    * [Modify Test Entries in Seed Data To Begin Dynamically On Current Week][B]
    * [Modify calendar display preperties based on viewport size][C]
    * [Implement persistence of displayed time range across sessions][D]


## 3174-Add a one week FullCalendar to the TempSchedule/Create view. 
> **Details:**
> Add a one week fullCalendar to the tempSchedule/Create view  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3189-Make a few changes to the ScheduleTemplate / Create view  
> **Details:**
> Parent story.  Please see [3192], [3191], [3190], [3195], [3193], [3194]  

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3192-clicking on a day on the calendar should pop up a modal
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3191-Modify calendar to display one week view
> **Details:**
> Make the calendar display as just a one week view. you may need to do some research on fullcalendar
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3190-Remove the notes input box and the create button
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3195-The modal should have a checkbox for "Day Off" 
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3193 the modal should have an input for start and end time 
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3194-Implement user-friendly time pickers
> **Details:**
> The start and end time inputs should be time pickers that are easy for a user to use. look at bootstrap time pickers  
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3209-Implement a mouse hand cursor on hover over calendar  
> **Details:**
> When the user hovers over any of the calendars, the cursor should change to reflect that the calendar is clickable.  
> This story is for all of the calendars.  This includes the schedule create view, the tempschedule create view, and the timeoffevent create view.  
### Solution: 
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3405-Implement CRUD operations on TimeOffEvents  
> **Details:**
> Parent story.  Please see [3408], [3409], [3410], [3411], [3412], [3413]  

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3413-Create a details modal  
> **Details:**
> When the user clicks on an existing event, create a modal that displays the event details in plain text.  Include an Edit button that opens an edit modal for making changes.  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3408-Create delete feature  
> **Details:**
> When the user clicks on an existing event, create a modal that displays the event details in plain text.  Include an Edit button that opens an edit modal for making changes.  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3409-Enable reading and loading of events on calendar  
> **Details:**
> Read entries from Events table pertaining to Time Off Events and populate the calendar  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3410-Implement an events creation feature  
> **Details:**
> When the user clicks a time slot on Calendar or selects a time range, open an edit modal with the corresponding start and end times pre-entered into time inputs  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3411-Implement an update feature  
> **Details:**
> When the user clicks on an existing event, open an edit modal with form inputs pre-populated with event data, and allow users to make changes, and a Save button to save and update that entry in the database.  Also include button to cancel the edit and to delete the event.  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3412-Make calendar events visually responsive  
> **Details:**
> When a user makes adjustments to the start/end times of either an existing event or a brand-new selection, cause the event to update visually on the calendar while the edit modal is displayed.  However, if the user does not save the event and exits the modal, visually restore the event to the original state (i.e. existing event returns to original state, and brand-new selection disappears) 
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3428-Add features in TimeOffEvents/Create and fix runtime errors  
> **Details:**
> Parent story.  Please see [3429], [3432], [3433], [3434], [3435], [3436], [3437]  

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3437-Enable view persistence on calendar  
> **Details:**
> Currently, whenever a change is made to the calendar, the view would return to the default, i.e. monthly view.  Implement a feature where if the user selects the weekly view, it will remain after changes are made to the calendar.  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3433-Fix runtime errors  
> **Details:**  
> &nbsp;&nbsp;\- Occasionally the delete button would show for a brand-new selection.  
> &nbsp;&nbsp;\- Occasionally the times in the input fields would mismatch the onscreen event.  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3432-Implement calendar event resizing feature  
> **Details:**
> When the user resizes an existing event, display the edit modal with updated start and end times pre-populated  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES)*
## 3429-Implement calendar events drag and drop capabilities  
> **Details:**
>When the user drags an existing event to a new time, display the edit modal with updated start and end times pre-populated  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3434-Prevent edit modal from closing automatically if save is unsuccessful  
> **Details:**
> Allow users to continue editing if a save attempt is unsuccessful, until the user closes the modal manually  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3435-Prevent users from creating events shorter than 15 minutes  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## 3436-Round event start and end times to the nearest 15 minute increments  
> **Details:**  
> &nbsp;&nbsp;\- Date pickers in browsers such as Edge do not restrict time values.  Therefore, when the user attempts to save an event, round the times to the nearest 15 minute increments.   
> &nbsp;&nbsp;\- For browsers that do support value control, such as Chrome, cause time to change 15 minutes at a time.  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## Additional Enhancements:
> **Details:**
> Parent story.  Please see the sub-stories below.
## Update TimeOffEvent Approval Status From Database When DetailsModal Opens  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## Modify Test Entries in Seed Data To Begin Dynamically On Current Week  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## Modify calendar display preperties based on viewport size  
### Solution:  

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*
## Implement persistence of displayed time range across sessions  
### Solution: 

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [FullCallendar Stories](#FULLCALENDAR-STORIES) >*

<br />

___


# OTHER STORIES
This section lists stories relating to other aspects of the project but unrelated to the usage of calendars
  * [3108-Rename Model.ID][3108]
  * [3109-Redirect "Manage" button][3109]
  * [3111-Modify "Mail" button on the nav-bar][3111]
  * [3113-Change ScheduleId type][3113]
  * [3121-Add a PayPeriod controller with views][3121]
  * [3110-Remove TemplateID from Schedule model][3110]
  * [3126-Add "Request Time Off" to nav menu][3126]
  * [3127-Add Shift/Create to nav menu][3127]
  * [3131-Add TempSchedule/Index to nav menu][3131]
  * [3130-Change Schedule model UserId type][3130]
  * [3141-Modify "Pay Period Length" label][3141]
  * [3137-Fix the Schedule/Create bug][3137]
  * [3135-Remove Inputs boxes from TimeOffEvent/Create][3135]
  * [3134-Fix the Messages/Inbox bug][3134]
  * [3142-Set Message/Create DateSent to the current time][3142]
  * [3143-Fix the Message/Create bug][3143]
  * [3145-Rearrange and modify Home/Index view][3145]
  * [3157-Set TempSchedule/Create DateCreated to the current time][3157]
  * [3168-Remove the Payperiods/Details view][3168]
  * [3172-Implement Schedule/Create modal][3172]
  * [3178-Make Event model End property nullable][3178]
  * [3206-Revise the ScheduleTemplate model][3206]
  * [3176-Implement message-all feature in TimeOffEvent controller][3176]
  * [3213-Add 3 more admin users to the seed data][3213]


## 3108-Rename Model.ID
> **Details:**
> Under Views\Schedule\Create.cshtml change Model.ID to Model.Id  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3109-Redirect "Manage" button
> **Details:**
> "Manage" button under the navigation button should bring you to the manage index view, not the schedule index view  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3111-Modify "Mail" button on the nav-bar
> **Details:**
> Remove the text from the mail button on the nav-bar. It should just be an icon  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3113-Change ScheduleId type
> **Details:**
> On the ScheduledWorkPeriod model, change the ScheduleId to be a Guid type  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3121-Add a PayPeriod controller with views
> **Details:**
> Add a PayPeriod controller with views for Index, Create, Delete, Edit etc  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3110-Remove TemplateID from Schedule model
> **Details:**
> Remove TemplateID from schedule model.  This change will require a migration  

### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3126-Add "Request Time Off" to nav menu
> **Details:**
> Add a link to the navigation drop-down titled "Request Time Off" that takes the user to the TimeOffEvent / Create page  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3127-Add Shift/Create to nav menu
> **Details:**
> Add a button to the navigation drop down to shift/create  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3131-Add TempSchedule/Index to nav menu
> **Details:**
> Add a link to the navigation dropdown leading to the TempSchedule / Index page  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3130-Change Schedule model UserId type
> **Details:**
> On the Schedule model, change the UserId from a string to a Guid. This will require a migration  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3141-Modify "Pay Period Length" label
> **Details:**
> On the PayPeriods / Create view, add some text to the "Pay Period Length" label so that is says "Pay Period Length (Days)"  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3137-Fix the Schedule/Create bug  
### Solution:
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3135-Remove Inputs boxes from TimeOffEvent/Create
> **Details:**
> On the TimeOffEvent Create view, remove the input boxes from the top  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3134-Fix the Messages/Inbox bug
### Solution:
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3142-Set Message/Create DateSent to the current time
> **Details:**
> On the Message controller, change the create method so that DateSent is set to the current time.  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3143-Fix the Message/Create bug
### Solution:
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3145-Rearrange and modify Home/Index view
> **Details:**
> On the index/home view, Remove the clock out button and make the clock in button say simply "Clock".  Then center all content on home/index view  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3157-Set TempSchedule/Create DateCreated to the current time
> **Details:**
> On the TempSchedule controller, change the Create function so that the DateCreated property gets set to the current time  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3168-Remove the Payperiods/Details view
> **Details:**
> Remove the Payperiods / Details view. Dont forget to include your .csproj file with your changes  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3172-Implement Schedule/Create modal
> **Details:**
> Implement the modal found in the TimeOff/Create view into the Schedule/Create view  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*

## 3178-Make Event model End property nullable
> **Details:**
> On the Event model, make the End property nullable. This will require a migration  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3206-Revise the ScheduleTemplate model
> **Details:**
> Properties should look somewhat like the schedule model. 
> [key] guid Id 
> string Title 
> List<ScheduledWorkPeriod> ScheduledWorkPeriods 
> dont forget migration  
### Solution:
  
*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3176-Implement message-all feature in TimeOffEvent controller
> **Details:**
> On the TimeOffEvent controller, create a function that will generate a message for every admin in the user table. Only define the function, do not call it just yet.  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*
## 3213-Add 3 more admin users to the seed data
> **Details:**
> Add 3 admin users to the seed data. Look at migrations > configuration  
### Solution:

*Jump to:&nbsp;&nbsp;[Table of Contents](#TABLE-OF-CONTENTS) > [Other Stories](#OTHER-STORIES) >*








[3174]:#3174-add-a-one-week-fullcalendar-to-the-tempschedulecreate-view
[3189]:#3189-make-a-few-changes-to-the-scheduletemplate--create-view
[3192]:#3192-clicking-on-a-day-on-the-calendar-should-pop-up-a-modal
[3191]:#3191-Modify-calendar-to-display-one-week-view
[3190]:#3190-remove-the-notes-input-box-and-the-create-button
[3195]:#3195-the-modal-should-have-a-checkbox-for-day-off
[3193]:#3193-the-modal-should-have-an-input-for-start-and-end-time
[3194]:#3194-Implement-user-friendly-time-pickers
[3209]:#3209-implement-a-mouse-hand-cursor-on-hover-over-calendar
[3405]:#3405-implement-crud-operations-on-timeoffevents
[3413]:#3413-create-a-details-modal
[3408]:#3408-create-delete-feature
[3409]:#3409-enable-reading-and-loading-of-events-on-calendar
[3410]:#3410-implement-an-events-creation-feature
[3411]:#3411-implement-an-update-feature
[3412]:#3412-make-calendar-events-visually-responsive
[3432]:#3432-implement-calendar-event-resizing-feature
[3428]:#3428-add-features-in-timeoffeventscreate-and-fix-runtime-errors
[3437]:#3437-enable-view-persistence-on-calendar
[3433]:#3433-fix-runtime-errors
[3432]:#3432-implement-calendar-event-resizing-feature
[3429]:#3429-implement-calendar-events-drag-and-drop-capabilities
[3434]:#3434-prevent-edit-modal-from-closing-automatically-if-save-is-unsuccessful
[3435]:#3435-prevent-users-from-creating-events-shorter-than-15-minutes
[3436]:#3436-round-event-start-and-end-times-to-the-nearest-15-minute-increments
[A]:#update-timeoffevent-approval-status-from-database-when-detailsmodal-opens
[B]:#modify-test-entries-in-seed-data-to-begin-dynamically-on-current-week
[C]:#modify-calendar-display-preperties-based-on-viewport-size
[D]:#implement-persistence-of-displayed-time-range-across-sessions

[3108]:#3108-rename-modelid
[3109]:#3109-redirect-manage-button
[3111]:#3111-modify-mail-button-on-the-nav-bar
[3113]:#3113-change-scheduleid-type
[3121]:#3121-add-a-payperiod-controller-with-views
[3110]:#3110-remove-templateid-from-schedule-model
[3126]:#3126-add-request-time-off-to-nav-menu
[3127]:#3127-add-shiftcreate-to-nav-menu
[3131]:#3131-add-tempscheduleindex-to-nav-menu
[3130]:#3130-change-schedule-model-userid-type
[3141]:#3141-modify-pay-period-length-label
[3137]:#3137-fix-the-schedulecreate-bug
[3135]:#3135-remove-inputs-boxes-from-timeoffeventcreate
[3134]:#3134-fix-the-messagesinbox-bug
[3142]:#3142-set-messagecreate-datesent-to-the-current-time
[3143]:#3143-fix-the-messagecreate-bug
[3145]:#3145-rearrange-and-modify-homeindex-view
[3157]:#3157-set-tempschedulecreate-datecreated-to-the-current-time
[3168]:#3168-remove-the-payperiodsdetails-view
[3172]:#3172-implement-schedulecreate-modal
[3178]:#3178-make-event-model-end-property-nullable
[3206]:#3206-revise-the-scheduletemplate-model
[3176]:#3176-implement-message-all-feature-in-timeoffevent-controller
[3213]:#3213-add-3-more-admin-users-to-the-seed-data






