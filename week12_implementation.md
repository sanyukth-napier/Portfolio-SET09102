# Changes from last week
I am still sticking with the orginal user story "As an UNDAC Deputy Team Leader I want to view details of all team partners so that I can contact them immediately" but removing the ability to be able to add and edit
existing data. The reason for this being that I want to focus on the "Team leader" only viewing the data not modifying it as this makes the code more complex. Someone else(not the team leader) should be in charge of making 
changes to the database that contains the details of the team patners

# DoD 
- Create the ContactInformation button on main page ( and the OnClicked method) [ Time required - 20mins ]

- Create the ContactInformation main page [ Time required - 10mins ]

- Create a Database to store team patners and their contact information [ Time required - 2 hours ]

- Be able search for a team patner through a search bar [ Time required - 1 day ]

The DoD remains the same except the adding and editing functionality is removed, instead I'm changing the way the data is 'found'. Last week it was presented as a list, this week that is removed and now the user can look
for the specific team patner by searching their name. This was done beacuse when there are a lot of team patners it is hard to find a specific name quickly by manually looking through one and as the user story says "immediately",
I think the search fucntion would fullfill this by being a lot faster and more effecient.

# Screenshots

The blank page without anything entered in search bar
![search](images/searchC.jpg)

Search in action
![test1](images/t1.jpg)
![test2](images/t2.jpg)

When the name is clicked
![test3](images/t3.jpg)

# Refelction and things that should be improved

1) The function of my program is very straightforward, I tried to use the KISS principle here by keeping it starightforward and by not adding unnessary complexities. The program fulfills only the given user story and
   does it well.

2) Database not working - in this iteration, I could not get SQlite to work but this program should ideally get all its data from the database (that is maintained by the UNDAC) which would also remove its need to edit and add 
   details.

3) More contact information - I was debating whether or not I should add more details(email, 2nd phone number etc) but ended up adding only the one phone number. I think only showing one form of contact detail will make it easy
   for the team leader to quickly search and immediately contact the person but there are merits to having multiple contact details being shown as well.