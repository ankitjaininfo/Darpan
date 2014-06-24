Darpan
======
Darpan (mirror in Hindi) is a proposal to build a Nodejs/MongoDB stack based project to help organizations maintain people directory and facilitate HR.

### Objective
The objective is to build a web software to help an organization’s HR in managing and organizing people. HR should be able to manage contact information, reporting hierarchy, classify people, birthday and anniversary calendar, attendance/leave management, reports, etc. (Payroll is not the objective of this project yet)

### Requirements
The proposal is to support following use-cases in MVP:

1. At the time of installation HR shall be able to configure a domain so that only users with specific email address can register.
2. HR shall be able to configure company details like name, logo, admin email addresses, departments.
3. Self service: Users with email addresses (matching domain) should be able to register and complete their profiles.
4. Users shall be able to search by name and results will be displayed in card design. This way they can discover people and their contact information.
5. Users should be able to browse other users by department, should be able to create attendance sheet, etc.
6. HR shall be able to export this data in CSV or Excel format so that data can be consumed with other information systems.
7. User shall be able to register their plans for upcoming leaves.

**What is it not**

1. Payroll management
2. Dynamic schema for user’s information. For any additional user fields, code changes are required.


### Implementation Plan

Plan is to start with [sahat/hackathon-starter] template and build on frameworks like: Express4, MongoDB/Mongoose, Bootstrap, FontAwesome, Moment, etc. Focus will in on incremental build where reach milestone delivers concrete set of features. No plan for data migration scripts until a stable release (~1.0).  

#### Milestone 0.1 (Kick-off)

1. Project structure
2. Decide what profile fields to add support for.
3. User login / session management.
4. User profile's CRUD operations.
5. User profile pic upload
6. Login domain restriction.
7. Admin role assignment.
8. Report: List all users (all in one page, no paging)

#### Milestone 0.2 

1. User search by name. (MongoDB's latest text index)
2. Search results in business cards design (UX)
3. Organization departments: CRUD operations for managing departments. User profile edits to have departments.
4. Reports: Listing users by department
6. Reports: Birthday calendar, anniversary calendar.
7. Reports: Attendance sheet.
8. Export data visible in any screen into CSV/JSON/Excel. This will be part of every screen design.

#### Milestone 0.3 

1. Badges: HR can define badges in system and can award users these badges. They can be anything for achieving within organization. Examples are attending training or certification, person of the month, milestone on years completion, etc. 
2. Leave and attendance management. Leave approval by manager, etc. Email notifications
3. Company level leave allotment and restrictions.
4. Reports: People on leave today. 
