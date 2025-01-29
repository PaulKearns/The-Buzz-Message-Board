# Phase 2 Sprint 9 - PM Report Template

## Team Information [25 points]

Team Information:
* Number: 5
* Name: Softserve Engineering
* Mentor: Hua Chen, hjc324@lehigh.edu

Team Roles:

* Project Manger: Paul Kearns, pdk226@lehigh.edu
* Backend developer: Ethan Lavi, esl225@lehigh.edu
* Admin developer: Josie Koelsch, jck423@lehigh.edu
* Web developer: Carlos Garro, cag224@lehigh.edu
* Mobile developer: Saik Jalal, saj325@lehigh.edu

Essential links for this project:

* Team's Dokku URL(s) (live web front-end link)
    * http://2023sp-softserve.dokku.cse.lehigh.edu/
* Team's software repo (bitbucket)
    * https://bitbucket.org/saj325/cse216team05/src/master/
* Team's Trello board
    * https://trello.com/b/ETt94AqH/softserve-engineering


Screenshot of Trello board:
https://drive.google.com/file/d/1tP2KbcSKy3aYiXSMpRVDQV_m5s058RVq/view?usp=sharing

## Role reporting [75 points total, 15 points each (teams of 4 get 15 free points)]
Report-out on each role, from the PM perspective.
You may seek input where appropriate, but this is primarily a PM related activity.

### Back-end

1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
   * Ethan communicated well with the team, and engaged regularly in salck and trello. He attended each meeting and offered help using knowledge of other roles. Tasks were created based on sprint and phase requirements and verified by functionality, including feedback from other rules.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * The only backlog is refactoring/making code more readable, and documentation.
1. List your back-end's REST API endpoints
    * POST to authenticate and get the session id: /session_authenticate  
    * GET to retrieve all messages: /messages
    * GET to retrieve a single message: /messages/:message_id
    * POST for adding a message: /messages
    * PUT for updating a message: /messages/:message_id
    * DELETE for removing a message: /messages/:message_id
    * PUT for liking a message: /messages/l/:message_id
    * PUT for disliking a message: /messages/d/:message_id
    * POST for adding a comment: /comment
    * PUT for editing a comment: /comment/:comment_id
    * DELETE for removing a comment: /comment/:comment_id
    * GET for getting another user's profile: /profile/:user_id
    * PUT for updating your own profile: /profile
1. Assess the quality of the back-end code
    * The backend code is good quality, thorough, and meets all functional requirements. Ethan also made dummy data from the routes before finishing implementation, which helped other roles.
1. Describe the code review process you employed for the back-end
    * Ethan showed me that his code worked, then sent a pull request. Unfortunately, Prof. Urban made some changes to dokku that make CORS with our app no longer work, so I can't tell if backend works with the other roles. Hopefully this issue is fixed tomorrow for us to test. 
1. What was the biggest issue that came up in code review of the back-end server?
    * The biggst issue was the one mentioned in the previous question, but I also encountered many odd merge conflicts that I still don't understand.
1. Is the back-end code appropriately organized into files / classes / packages?
    * The backend code is organized properly with different files containing classes as part of the package for each overall component of the backend code. Some files are a bit long and could be refactored for better understanding.
1. Are the dependencies in the pom.xml file appropriate? Were there any unexpected dependencies added to the program?
    * They are all appropriate, and none were unexpected. The main change was adding a dependency for google oauth.
1. Evaluate the quantity and quality of the unit tests for the back-end
    * The unit tests for backend are plentiful and of good quality. Ethan made them before finishing implementation, demonstrating test driven development.
1. Describe any technical debt you see in the back-end, if any
    * The only tech debt is documentation and refactoring for readability and understanding.

### Admin

1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Josie worked effectively with the team and showed up to every meeting. She was responsive on slack and tracked her progress on trello. I made tasks using the sprint requirements, and verified them by her showing me functionality. She checked them off when complete.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * The backlog for admin is to improve unit tests and add documentation.
1. Describe the tables created by the admin app
    * Admin creates four tables, tblMessages, tblComments, tblUsers, and tblLikes. Users stores user-given info, messages stores message information with a foreign key of user, comments has a foreign key of message, and likes also has a foreign key of message.
1. Assess the quality of the admin code
    * The admin code is good quality overall and meets implementation requirements. Despite some files being long, it is overall understandable.
1. Describe the code review process you employed for the admin app
    * Josie submitted a pull request, and after checking over the code, I checked it in premaster.
1. What was the biggest issue that came up in code review of the admin app?
    * There were no significant issues. Josie's first PR was accidentally set to master, so I just asked her to recreate it to premaster.
1. Is the admin app code appropriately organized into files / classes / packages?
    * The admin code is organized appropriately into files and classes that make sense, similar to backend. The database file is a bit long but still makes sense.
1. Are the dependencies in the pom.xml file appropriate? Were there any unexpected dependencies added to the program?
    * The dependencies are appropriate, and none were really unexpected.
1. Evaluate the quantity and quality of the unit tests for the admin app
    * Josie made unit tests for invalidating messages, deleting tables, creating tables, and getting a database connection. We could make more for some other feature, but I believe this is a good start.
1. Describe any technical debt you see in the admin app, if any
    * The only tech debt is documentation/refactoring, and maybe adding more unit tests.

### Web

1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Carlos engaged effectively with the team and asked for help when necessary. He was responsive on slack and updated his trello tasks, which I made from sprint and phase reqs. He also attended most meetings.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * Web is mostly complete, with all funcitonality except viewing other users' profiles working, as well as some additional unit tests.
1. Describe the different models and other templates used to provide the web front-end's user interface
    * Carlos essentially reformatted previous code from the web branch to fit new tasks, like making comments from previous messages. He added new functions for oauth tasks, and also created a login page and the ability to view and edit your profile using new forms. Comments can be viewed from messages with the toggle of a button, also using a new comment form.
1. Assess the quality of the Web front-end code
    * The web frontend code is good quality overall, and meets nearly all requirements. It is somewhat hard to understand as most of it is in a 1200 line file, so reformatting this could be useful during refactoring.
1. Describe the code review process you employed for the Web front-end
    * After showing me what he had implemented, Carlos made a pull request that I reviewed and accepted.
1. What was the biggest issue that came up in code review of the Web front-end?
    * Since CORS wasnt working due to changes with dokku today, I couldnt test the web interface with our backend, and we werent able to get the local backend working either. Hopefully this is fixed by Thursday so we can test it.
1. Is the Web front-end code appropriately organized into files / classes / packages?
    * The web frontend code is appropriately organized into files with different classes, although the primary file is very large and should likely be split up.
1. Are the dependencies in the package.json file appropriate? Were there any unexpected dependencies added to the program?
    * The dependencies are appropriate, and none are really unexpected.
1. Evaluate the quantity and quality of the unit tests for the Web front-end 
    * Unit tests are present but somewhat limited so far, and we will work on adding more for new functionality.
1. Describe any technical debt you see in the Web front-end, if any
    * We mainly need to refactor, allow viewing of other users' profiles, and add more unit tests.

### Mobile

1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Saik worked well with the team overall, and was generally quick to respond on slack. He used Trello to an extent, and I changed the status of tasks that he did not. He was able to make it to most meetings. Tasks were made from sprint reqs and verified by him showing me their functionality.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * The items that are complete are post and comment implementation, vote implementation, as well as a loading screen and login screen. We still have not gotten Oauth working fully, and also must implement profiles as specified by the requirements.
1. Describe the activities that comprise the Mobile app
    * Currently, there is a log in screen, but oauth is not fully working so the log in is not implemented. A list of posts with votes is displayed, and a button can be pressed to toggle comments.
1. Assess the quality of the Mobile code
    * The mobile code is decent quality overall. Saik has had some trouble with the transition to flutter, and we still need to implement multiple features.
1. Describe the code review process you employed for the Mobile front-end
    * Saik showed me what he had and submitted a pull request. Due to CORS not working today, I was not able to test mobile as it is integrated.
1. What was the biggest issue that came up in code review of the Mobile front-end?
    * The biggest issue was the change to CORS today that prevents our front ends from interacting with the back end through dokku.
1. Is the Mobile front-end code appropriately organized into files / classes / packages?
    * The mobile front end is appropriately organized into various files and classes, with files for various sub-components of the app.
1. Are the dependencies in the pubspec.yaml (or build.gradle) file appropriate? Were there any unexpected dependencies added to the program?
    * The dependencies are appropriate, with no unexpected dependencies added. The primary addition relates to authentication.
1. Evaluate the quantity and quality of the unit tests for the Mobile front-end here
    * There are mobile tests, but we must add new ones for the new funcitonality.
1. Describe any technical debt you see in the Mobile front-end, if any
    * Tech debt includes making authentication work, implementing profiles, and adding unit tests.

### Project Management
Self-evaluation of PM performance

1. When did your team meet with your mentor, and for how long?
    * We met with Hua for an hour on Thursday at 7.
1. Describe your use of Trello.  Did you have too much detail?  Too little?  Just enough? Did you implement policies around its use (if so, what were they?)?
    * In retrospect, I could have used slightly more detail on Trello regarding subjective phase requirements, but overall I think it was adequate and everyone understood their tasks. With regard to policies, I just asked members to update their tasks and checklist as completed. Sometimes I updated these instead, which is completely fine.
1. How did you conduct team meetings?  How did your team interact outside of these meetings?
    * We conducted team meetings by scheduling either in person or slack and negotiating around our schedules. Outside of these meetings, we use slack and occasionally text messages.
1. What techniques (daily check-ins/scrums, team programming, timelines, Trello use, group design exercises) did you use to mitigate risk?
    * I checked in with each member almost daily, kept tasks updated on Trello, and we held multiple meetings. It would have been helpful to meet or discuss more over the weekend, but this was difficult given Easter and Passover.
1. Describe any difficulties you faced in managing the interactions among your teammates? Were there any team issues that arose?
    * There were few overall difficulties. Sometimes teammates missed slack notifications, and I feel like some should have been more open to help and attended meetings for this. Overall, there were no significant team issues.
1. How well did you estimate time during the early part of the phase?  How did your time estimates change as the phase progressed?
    * We estimated time fairly well. We actually completed more than I expected to, although it would have been useful to have more time for pull requests, especially given the CORS issue. Additionally, I had an issue where I completed most of this PM report without saving it on bitbucket, and when I attempted to commit, all progress was lost. This is causing me great emotional anguish and made this take much longer than expected.
1. What aspects of the project would cause concern for your customer right now, if any?
    * I would be most concerned about making the mobile app functional for customers according to the latest sprint requirements.
1. What is your biggest concern as you think ahead to the next phase of the project?
    * My biggest concern is the web and mobile roles having to learn js/flutter and learn to implement caching, a new concept, in a limited time.
1. Describe the most significant obstacle or difficulty your team faced.
    * The biggest obstace we faced was time management, with one member being unable to finish all tasks. We hope to complete these by live grading on Thursday. The CORS issue today also caused difficulty because we could not use our last day to add functionality that we could test with the backend.