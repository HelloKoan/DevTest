# Welcome to the Koan DevTest


This is a developer test for new candidates at all levels and is designed to gauge overall levels of understanding for web development

###General

Create a work folder and clone the code in this repository. Create a new local branch for this repository for your work, and calling the branch your name and the date in the format yyyy-mm-dd

Complete the tasks below, committing your code at suitable intervals. 

You may wish to also edit the ignore file so that unnecessary code that does not need to be committed is not included.

At the end of the test commit your branch locally for review


###Fizz Buzz Test - Suggested time : 10 minutes
***

Task : Write an app which will print the numbers from 1 to 100. Complete as many of these as possible
* For multiples of three print "Fizz" instead of the number. 
* For the multiples of five print "Buzz" as well as the number. 
* For numbers which are multiples of both three and five print "FizzBuzz" instead of the number.
* For numbers which are a multiple of 10, introduce a half second pause before continuing
* Calculate and display the total execution time in seconds for the program executing

###MVC Test - Suggested Time : 30 minutes
***

####Task : The project is a basic web site, and a library but there are a few compilation errors and the program needs to be improved.
* Fix any issues and get the project compiling
* Make all controllers inherit from `MyControllerBase`. This base class contains a lot of methods which allow messages to be passed back to the view for the user - the Alerts

####Controller Test

* Add a message to the Index action of the Home controller to display the current time to the user. Use the code already included which is designed to report Alerts back to the view from controlller actions. You will need to
   1. Amend the Shared layout, and insert the line @Html.Alerts() above the @RenderBody
   2. In the ActionMethod for Home.Index, add the line AddInfoAlert("XXX"); where XXX is the current date and time
   3. (optional) Use the DateTime Extensions to display the date in 3 different time zones
   4. (optional) Write a HTMLHelper instead of writing directly to the view to display the date in 3 different time zones. There is a HTML Helper already in the project for reference
   
* Add a new Controller and associated view to the project. The name should be DaysOfTheWeekController. This is a simple controller test to list the days of the week on the URL /DaysOfWeek
   1. In the index view of that controller, print full name days for every day of the week (eg Monday, Tuesday, Wednesday)
   2. Add a get action to that controller which accepts a number and translates that to a named weekday, where 0 is Sunday, and 6 is Saturday. eg /DaysOfTheWeek/4 would output Thursday
   3. (Optional) Change the name of the route which this controller responds to without changing the controller name. The new route should be /Days

####ViewModel Test
This uses the HelloViewModel class, and the associated actions on the Home controller
* Create a link from the Homepage to the new action (/Home/Hello/)
* Make the Name property Mandatory, and with a maximum length of 30
* Write a post method for the Hello action which validates the posted view model and displays the information back to the user above the form

####Membership Test
Add new fields to the Acccount class, capture the first and last name. We already capture age as an integer. You will need to amend the ApplicationUser class
  1. Add First and Last names as public properties
  2. Add constraints to those fields - max string length (100)
  3. Amend the views models and the form for registration to ask for and capture First and Last name, as well as Age. 

Finally - think of any improvements we could make to this test to make it more challenging