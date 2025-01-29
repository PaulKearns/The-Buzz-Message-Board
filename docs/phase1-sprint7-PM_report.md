## Team Information [10 points]

Team Information:

* Number: 5
* Name: SoftServe Engineering
* Mentor: Hua Chen, hjc324@lehigh.edu

Team Roles:

* Project Manager: Josie Koelsch, jck423@lehigh.edu
* Backend developer: Carlos Garro, cag224@lehigh.edu
* Admin developer: Saik Jalal, saj325@lehigh.edu
* Web developer: Paul Kearns, pdk226@lehigh.edu
* Mobile developer: Ethan Lavi, esl225@lehigh.edu

Essential links for this project:

* Team's Dokku URL(s) (live web front-end link)
  * [http://2023sp-softserve.dokku.cse.lehigh.edu/](http://2023sp-softserve.dokku.cse.lehigh.edu/)
* Team's software repo (bitbucket)
  * [https://bitbucket.org/saj325/cse216team05/src/master/](https://bitbucket.org/saj325/cse216team05/src/master/)
* Team's Trello board
  * [https://trello.com/b/ETt94AqH/softserve-engineering](https://trello.com/b/ETt94AqH/softserve-engineering)

## Beginning of Phase 1' [20 points]

Report out on the Phase 1 backlog and any technical debt accrued during Phase 1.

1. What required Phase 1 functionality was not implemented and why?
    * This should be a list of items from the Phase 1 backlog that were not "checked off".
    * These high-priority items are to be added to the Phase 1' backlog that appears on your Trello board.
        * The missing functionality from Phase 1 was connecting the mobile to the real backend (not just a local data store) and adding liking/removing a like functionality to the admin app. These were not completed because they were not specified directly on the sprint requirements documents, but working with our mentor we understood the requirements better and were able to complete them this week.
1. What technical debt did the team accrue during Phase 1?
    * List this based on a unit-by-unit basis, as appropriate.
    * These items are to be added to the Phase 1' backlog that appears on your Trello board.
        * The technical debt included: a partial transition to React for our web front-end and creating a database that can be used for testing.

## End of Phase 1' [20 points]

Report out on the Phase 1' backlog.

1. What required Phase 1 functionality still has not been implemented or is not operating properly and why?
    All required Phase 1 functionality has been implemented and is functioning properly.
1. What technical debt remains?
    The technical debt that remains is a full transition to React (a partial attempt has been made by Paul) and moving our front-end code onto dokku so our front-end UI can be visible on the URL as well as using it for our backend.

## Role reporting [50 points]

Report-out on each team members' activity, from the PM perspective (you may seek input where appropriate, but this is primarily a PM related activity).

1. If there was any remaining Phase 1 functionality that needed to be implemented in Phase 1', what did the PM do to assist in the effort of getting this functionality implemented and operating properly?

Josie was able to assist Saik with completing the like/remove like functionality for the admin app by working synchronously with him in person during a group meeting time and checking that the database updates in real time. He then finished documentation asynchonrously and Josie followed up. Josie was able to assist Ethan in the mobile connection to backend by pulling his changes onto her end and identifying inconsistencies that he was able to fix and push again until it functioned.

### Back-end

What did the back-end developer do during Phase 1'?

Carlos focused mainly on documentation during Phase 1' since the functionality existed already, but he also updated the backend SELECT ALL calls in SQL to include an ORDER BY qualifier, which helped maintain the order of messages. We had previously had problems with likes causing a reorder in the messages. He uploaded the javadocs onto bitbucket. He also added a maven test for testing the connection to the database.

### Admin

What did the admin front-end developer do during Phase 1'?

Saik added the like/remove like functionality to the admin app and added documentation through javadocs. This addressed the missing functionality from Phase 1. Like Carlos, he also added a maven test for testing the connection to the database.

### Web

What did the web front-end developer do during Phase 1'?

Paul further researched and practiced React to prepare for a transition, and was able to complete the skeleton UI but not the connection to the database. However, he was able to complete the javascript documentation.

### Mobile

What did the mobile front-end developer do during Phase 1'?

Ethan was able to connect the mobile app to the database and also addded the delete functionality for individual messages. He added a red background and garbage can UI element that appears when you swipe to delete a message. He was also able to generate the dart docs.

### Project Management

Self-evaluation of team performance

1. When did your team meet with your mentor, and for how long?

    We met with our mentor on Thursday for our hour long weekly meeting, and we met again on Sunday for a grading/help session, for about 30-45 minutes.

1. Describe how the team worked together in Phase 1'. Were all members engaged? Was the work started early in the week or was there significant procrastination?

    All members were engaged, and the functionality progress was mostly done earlier in the week, but the documentation was procrastinated until mostly the day it was due, which meant pull requests were being approved right before, during, and after the grading session with our mentor.

1. Describe any concerns you have about the prospects for success moving forward? What steps can the team take to reduce your concern?

    My main concern is that the members have just gotten comfortable in their respective branches, and now we are switching roles. I am concerned about the catch-up time it will take for the new programmers to understand their new assignment. What would help reduce this concern is early and thorough meetings between the members who are passing roles to each other so they can explain and answer questions not addressed in their documentation.