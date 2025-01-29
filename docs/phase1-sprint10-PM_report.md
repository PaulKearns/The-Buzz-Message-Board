# Phase 2' Sprint 10 - PM Report Template
Use this form to provide your project manager report for Phase 2' (Prime).  Please give detailed answers.
In addition to uploading to coursesite, version control this in the `master` branch under the `docs` folder.

## Team Information [10 points]

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


## Beginning of Phase 2' [20 points]
Report out on the Phase 2 backlog and any technical debt accrued during Phase 2.

1. What required Phase 2 functionality was not implemented and why? 
    * All functionality was implemented other than mobile login, profiles, ability to post comments, and fully complete authentication. Saik had difficulty with these, and although I checked in frequently, I didn't realize how little progress was being made. We still need unit tests for mobile and web.
1. What technical debt did the team accrue during Phase 2?
    * The primary technical debt is the mobile functionality described in the previous question. We also still have not figured out how to get the front-ends to connect to the backend now that https is enabled, or merged the web front-end into dokku (which seems pointless given it does not currently work with dokku with https). Other than that, unit tests for mobile must be added.

Screenshot of Trello board (at the beginning of phase 2'):
(should match/support list of backlog and tech debt items)
https://drive.google.com/file/d/1Nk4bVNkubvnXUP6InQirAGApJ56RTU1b/view?usp=sharing

## End of Phase 2' [20 points]
Report out on the Phase 2' backlog.

1. What required Phase 2 functionality still has not been implemented or is not operating properly and why?
    * We have still not gotten Oauth for mobile working properly, as well as profile pages. We have not been able to get our front-ends to connect to dokku with https. We believe meeting with Prof. Urban on Tuesday will help with this.
1. What technical debt remains?
    * We still must finish mobile functionality as listed above, add mobile unit tests, and get front-ends working with https. We also must merge web into backend-dokku once we get web working with https.
    
Screenshot of Trello board (at the close of phase 2'):
(should match/support list of backlog and tech debt items)
https://drive.google.com/file/d/1Nk4bVNkubvnXUP6InQirAGApJ56RTU1b/view?usp=sharing

## Role reporting [50 points total, 10 points each (teams of 4 get 10 free points)]
Report-out on each team members' activity, from the PM perspective (you may seek input where appropriate, but this is primarily a PM related activity).

1. If there was any remaining Phase 2 functionality that needed to be implemented in Phase 2', what did the PM do to assist in the effort of getting this functionality implemented and operating properly?
    * For remaining functionality, only backlog from mobile remained. I checked in with Saik frequently through slack, and met with him and Ethan on Friday and Sunday to try to complete any remaining mobile functionality. In retrospect, I should have had him be more specific with progress, because I was under the impression that more was completed.

### Back-end

1. What did the back-end developer do during Phase 2'?
    * Ethan refactored his code so it is easier to understand, updated comments and javadocs, and pair-programmed with Saik to help make mobile function
1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Ethan engaged effectively with the team and was very helpful. He was responsive on track and completed his trello tasks. Assignments were again created from sprint requirements, and was verified through using his code for the frontends, as well as unit tests and the code review. He participated in every meeting and helped other roles.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * The backend is fully complete for this phase. All requirements, logic, and documentation are functional and complete.
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
    * The backend code is good quality, fully functional, and seems to be scalable and understandable as well.
1. Describe the code review process you employed for the back-end
    * All funcitonal implementation was completed last sprint, so this wasn't very difficult. Ethan submitted a pull request, which I evaluated and then merged and tested.
1. What was the biggest issue that came up in code review of the back-end server?
    * There were no real issues with this code review. It was odd that some material from web was considered part of this, which Ethan pulled for testing, but this was pulled from Carlos' code and caused no issues in the PR.
1. Is the back-end code appropriately organized into files / classes / packages?
    * Yes, the backend code does have appropriate organization of files, classes, and packages.
1. Are the dependencies in the pom.xml file appropriate? Were there any unexpected dependencies added to the program?
    * There were no dependencies added this sprint.
1. Evaluate the quantity and quality of the unit tests for the back-end
    * The backend unit tests are plentiful and effective. Ethan actually used test-driven development, and it is useful to see whether the tests passed when running mvn package to see if there are any issues automatically.
1. Describe any technical debt you see in the back-end, if any
    * There is no tech debt for backend.
### Admin

1. What did the admin front-end developer do during Phase 2'?
    * Josie completed documentation through javadocs and updating comments during this phase.
1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Josie communicated effectively through trello and slack. She attended all meetings relevant to her. The only real task was documentation, from sprint requirements, which I looked over during the code review.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * Admin is complete so far, and there are no backlog items.
1. Describe the tables created by the admin app
    * Admin creates four tables, tblMessages, tblComments, tblUsers, and tblLikes. Users stores user-given info, messages stores message information with a foreign key of user, comments has a foreign key of message, and likes also has a foreign key of message.
1. Assess the quality of the admin code
    * The admin code is good quality and seems to be scalable and understandable overall.
1. Describe the code review process you employed for the admin app
    * Josie submitted a pull request, which I looked over and approved. After testing in premaster, I merged to master.
1. What was the biggest issue that came up in code review of the admin app?
    * No real issues came up with this code review.
1. Is the admin app code appropriately organized into files / classes / packages?
    * The admin code is organized into logical files, classes, and packages based on functionality. I don't think any structural changes are necessary.
1. Are the dependencies in the pom.xml file appropriate? Were there any unexpected dependencies added to the program?
    * All dependencies are appropriate and haven't changed since last sprint.
1. Evaluate the quantity and quality of the unit tests for the admin app
    * Admin has four unit tests, and I feel that they are useful and sufficient. There could be more tests implemented for remaining features, but I believe these are good quality.
1. Describe any technical debt you see in the admin app, if any
    * I see no significant tech debt.

### Web

1. What did the web front-end developer do during Phase 2'?
    * Carlos made a slight edit to viewing other users' profiles, attempted unit tests, and created documentation.
1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Carlos engaged effectively with the team, attended meetings relevant to him, was active on slack and trello, and completed his tasks of documentation and fixing profile viewing, which were created using sprint requirements. This was verified by me in the pre-master branch after the pull request.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * The unit tests for web could be improved. I don't think there is any other backlog.
1. Describe the different models and other templates used to provide the web front-end's user interface
    * Carlos essentially reformatted previous code from the web branch to fit new tasks, like making comments from previous messages. He added new functions for oauth tasks, and also created a login page and the ability to view and edit your profile using new forms. Comments can be viewed from messages with the toggle of a button, also using a new comment form.
1. Assess the quality of the Web front-end code
    * I think the web front-end is a bit hard to understand but good quality overall and meets all functional requirements.
1. Describe the code review process you employed for the Web front-end
    * I had already seen the updated web functionality in person, so Carlos just submitted a PR, which I reviewed. I tested web in premaster before merging to master.
1. What was the biggest issue that came up in code review of the Web front-end?
    * Carlos accidentally left his git log in web, so I just asked him to remove it.
1. Is the Web front-end code appropriately organized into files / classes / packages?
    * The web front-end is effectively organized using files, classes, and packages.
1. Are the dependencies in the package.json file appropriate? Were there any unexpected dependencies added to the program?
    * Dependencies haven't changed and none are unexpected or inappropriate.
1. Evaluate the quantity and quality of the unit tests for the Web front-end
    * There are 8 unit tests for web, including multiple new tests for this sprint, but they are not yet fully functional. These should be improved, and a few more could be added.
1. Describe any technical debt you see in the Web front-end, if any
    * The only tech debt is adding a few unit tests to make them more useful.

### Mobile

1. What did the mobile front-end developer do during Phase 2'?
    * Saik completed the login page, made progress on Oauth though it is not fully working, and created widgets for comments and the ability to toggle them. He did update dartdocs.
1. Describe the engagement of this component's developer with the team (How effective was the process? How was communication with the team - use of Slack and Trello, attendance and participation in meetings, etc. How were tasks created? How was completion of tasks verified?)
    * Saik was decent but could have done better with communication. He was somewhat active on slack and trello, but I got the impression he was making more progress than he was. He attended all meetings. Tasks were created from sprint requirements, and verified by him showing me progress.
1. Assess the completeness of this component (list remaining backlog item(s), if any)
    * We still need to finish authentication, create the ability to post comments, and create profile functionality.
1. Describe the activities that comprise the Mobile app
    * There is a log in screen but it is not fully functional. There is a log in file, a loading screen, message board and message card files, a comment widget, and an add mesasge card.
1. Assess the quality of the Mobile code
    * The mobile quality that exists is good quality, but it lacks much functionality, as explained above.
1. Describe the code review process you employed for the Mobile front-end
    * Saik, Ethan, and I met shortly before the PR to get some progress done. After this, he submitted a PR, which I checked and tested before merging.
1. What was the biggest issue that came up in code review of the Mobile front-end?
    * There were no significant issues. There was slight difficulty due to the PR being relatively late.
1. Is the Mobile front-end code appropriately organized into files / classes / packages?
    * The mobile code is organized appropriated into files, classes, and packages, with widgets for each compenenet such as comments, and cards for messages and adding messages.
1. Are the dependencies in the pubspec.yaml (or build.gradle) file appropriate? Were there any unexpected dependencies added to the program?
    * Dependencies are appropriate. None were uenexpected to me.
1. Evaluate the quantity and quality of the unit tests for the Mobile front-end here
    * The unit tests that exist are good quality, but new ones must be implemented for this phase's requirements.
1. Describe any technical debt you see in the Mobile front-end, if any
    * Mobile still needs to get Oauth fully functional, add the ability to post comments, implement all profile funcitonality, and add unit tests.

### Project Management
Self-evaluation of PM performance

1. When did your team meet with your mentor, and for how long?
    * We met with Hua on Thursday night for an hour.
1. Describe how the team worked together in Phase 2'. Were all members engaged? Was the work started early in the week or was there significant procrastination?
    * All members were engaged. Work was done early for all except mobile. In retrospect I should have done better to keep Saik accountable for his work.
1. Describe your use of Trello.  Did you have too much detail?  Too little?  Just enough? Did you implement policies around its use (if so, what were they?)?
    * I think my detail in trello was reasonable. I opted to use checklists for functionality that applied to all. I did not have any specific policies regarding its use.
1. How did you conduct team meetings?  How did your team interact outside of these meetings?
    * I conducted team meetings by first judging the need for one, then using slack or in-person discussion to determine when to meet and who would/should attend.
1. What techniques (daily check-ins/scrums, team programming, timelines, Trello use, group design exercises) did you use to mitigate risk?
    * I used frequent check ins via slack, and held three meetings this week. I should have been more specific knowing what functionality is implemented with mobile.
1. Describe any difficulties you faced in managing the interactions among your teammates? Were there any team issues that arose?
    * There were difficulties with getting all mobile requirements completed. I was under the impression that more was done, and should do better to ask for more specifity in what has been completed. I do feel like I was available to help and sent frequent messages checking in and asking if a meeting would help.
1. How well did you estimate time during the early part of the phase?  How did your time estimates change as the phase progressed?
    * We estimated time fairly well for most tasks, but mobile took more time than anticipated. Time estimates for mobile were pushed back as the deadline approached.
1. What aspects of the project would cause concern for your customer right now, if any?
    * The customer would be concerned about the lack of functionality in the mobile app, particularly Oauth and profiles.
1. Describe any concerns you may have about the prospects for success moving forward? What steps can the team take to reduce your concern?
    * I am concerned about web and mobile having to learn caching for next phase, and mobile having to make up tech debt for this phase first if Saik isn't able to complete it.
1. Describe the most significant obstacle or difficulty your team faced.
    * The most significant obstacle was subpar communication regarding how much implementation remained in mobile. I feel like I was available, but should have asked for more specifity in what was completed. I will try to be more specific and do better with accountability in the future.