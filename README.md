# CampusClubFairRelations:
A data base documenting the relationships between campus clubs, students, events, and the club fair. Extension adds rewards and points for attendance.
# Group Name:
Group B7
# Group Description:
Enoch Faminu, Group leader

Riya Jegajeevan, Conceptual modeler

Justin Wu, SQL Writer

Samandar Farkho, Database designer and Data Wrangler
# Case Description:
Our project was on the functionality of the Campus Club Fair(CCF) at Peachtree State University. They needed a database to manage their clubs, memberships, students, events, funding, and their annual club fair. The central entity in our model are the Clubs. Each club operates on campus across different categories such as robotics, gaming, cultural groups, or debate. These clubs operate off of students who join as members. Clubs host many events throughout the year such as meetings, workshops, and volunteer events. To extend our case, we introduced a Student Reward System that tracks each student's attendance points, and organizes the cumulative amount into tiers. The students can then redeem their points for reward items, which are logged as a transaction. Our task was to display these relationships in a data model, generate various types of fictitious sample data, and store it in a database. We then used this to create queries from this data in order to gain insight on club operations and overall student engagement at Peachtree State University. 
# Data Model Description:
<img width="349" height="299" alt="image" src="https://github.com/user-attachments/assets/46c07df4-d293-486e-b0f9-b6b71a1acb63" />

Our data model is based on the Campus Club Fair at Peachtree State University. The main entity in our model is Club, which represents every student organization that is registered at the Campus Club Fair. Clubs are connected to our ‘students’ entity through membership as well as officer roles. The Officer Roles entity holds role names(President, Vice President, Treasurer, etc), start dates, and end dates. Since a club can have many students and a student can join many clubs, there is an associative entity named Membership. This stores each student's join date and status. 

Clubs are also connected to Events through the host table. Since an event can be hosted by multiple clubs, and a club can host many events throughout the year, there is a many to many relationship with a third entity labeled Host, which also records if the club is the primary or secondary host. The attendance of these events is documented in the Attendance entity, which is the associative entity between Student and Events. 

Each club can also have multiple budget records, and submit many Funding requests for purchases. Every funding request needs to be assigned to a reviewer from the Funding_Reviewer table, and possibly also a backup reviewer. If the funding request is approved, it creates records in the Purchases table. During the annual club fair, each club can reserve a booth, which is captured by the entity in between Club and Club_Fair.

Lastly, our extension that we decided on was to create a reward system for students to incentivize them to come to events. Every student gets one entity labeled student_points, which tracks their cumulative points. This is then linked to the Student_Reward_Tiers, which has 3 different tiers (Bronze, Silver, Gold) based on their points. Students can then redeem points for various items in the Reward_Items entity, with each separate transaction recorded in Points_Record.

# Data Dictionary:
<img width="476" height="236" alt="image" src="https://github.com/user-attachments/assets/5974cbb7-ac3f-4cd6-ad26-f8681f082a27" />

<img width="482" height="191" alt="image" src="https://github.com/user-attachments/assets/219e5e45-65c2-477d-b18f-48c8eff35d90" />

<img width="480" height="314" alt="image" src="https://github.com/user-attachments/assets/acaf0dcc-0d19-47a5-a1d7-b14785cdd09c" />

<img width="481" height="245" alt="image" src="https://github.com/user-attachments/assets/2922917f-f224-49f9-8dbe-3dcd7375b47d" />

<img width="480" height="215" alt="image" src="https://github.com/user-attachments/assets/7de14853-7170-448e-9f13-5738b78d1fde" />

<img width="469" height="260" alt="image" src="https://github.com/user-attachments/assets/4dfae1a2-deaf-4fe5-81c0-ce756e0fc9c7" />

<img width="362" height="330" alt="image" src="https://github.com/user-attachments/assets/2d3afc70-5a79-4ced-a321-54e5666f1be2" />

<img width="440" height="213" alt="image" src="https://github.com/user-attachments/assets/1f598749-a0ce-4e94-a70f-dc6da8d0c983" />

<img width="438" height="151" alt="image" src="https://github.com/user-attachments/assets/868ecfdd-688a-4004-aea0-cdb878a29cdb" />

<img width="446" height="212" alt="image" src="https://github.com/user-attachments/assets/e19406e1-4b02-4985-aa93-62474200ab75" />

<img width="433" height="296" alt="image" src="https://github.com/user-attachments/assets/598361e0-1c86-4a96-a1f2-278ed5ba56e2" />

<img width="435" height="246" alt="image" src="https://github.com/user-attachments/assets/19a503bc-8468-4926-9893-240008bac48b" />

<img width="431" height="244" alt="image" src="https://github.com/user-attachments/assets/e5812462-88de-4c64-9108-fb9b57b4d052" />

<img width="431" height="246" alt="image" src="https://github.com/user-attachments/assets/b3c8291a-a27a-48bb-9042-00e5eb7b7580" />

<img width="440" height="247" alt="image" src="https://github.com/user-attachments/assets/6027d15c-7589-4c4e-a2a1-f6873c3a7b43" />

<img width="443" height="301" alt="image" src="https://github.com/user-attachments/assets/2f9c7312-584d-4278-914b-aba3847e3c51" />

<img width="445" height="143" alt="image" src="https://github.com/user-attachments/assets/502a5e9f-c16b-47d6-8ac4-3e2dd4c11644" />

# Queries

<img width="437" height="251" alt="image" src="https://github.com/user-attachments/assets/e8cd02f8-ec32-4225-bb34-a0f5d19e83f5" />

1. Clubs that hosted the most events this semester
<img width="725" height="435" alt="image" src="https://github.com/user-attachments/assets/76b1aa1e-aec6-4582-87bc-60deda78d4ea" />

2. Events co-hosted by more than one club
<img width="650" height="327" alt="image" src="https://github.com/user-attachments/assets/115227ab-2b1c-494b-9fba-e8be5cf706e1" />

3. Student who attended the most events
<img width="903" height="511" alt="image" src="https://github.com/user-attachments/assets/aef17213-e720-40a9-92b3-452c47481008" />

4. List all clubs
<img width="361" height="421" alt="image" src="https://github.com/user-attachments/assets/0436b315-5579-446b-ace0-e16ff6f8d3b7" />

5. Events with the highest attendance
<img width="711" height="438" alt="image" src="https://github.com/user-attachments/assets/707766d7-88d7-4a1d-a36d-9df069ed198a" />

6. List all events ordered by date
<img width="520" height="486" alt="image" src="https://github.com/user-attachments/assets/33c8d13d-a052-4195-88f7-78f40f6bc441" />

7. Find students who have never attended any event
<img width="585" height="345" alt="image" src="https://github.com/user-attachments/assets/01668d73-b637-476b-a0b7-76ddb9bb6971" />

8. List all active memberships with student names
<img width="559" height="520" alt="image" src="https://github.com/user-attachments/assets/2ca111b3-b646-469c-99ff-4bd3dcce5eba" />

9. Most popular reward item
<img width="628" height="386" alt="image" src="https://github.com/user-attachments/assets/6823b2d0-a7a9-4abd-8bea-6066884c4b19" />

10. Students who first name start with A
<img width="408" height="338" alt="image" src="https://github.com/user-attachments/assets/41c989d5-3d45-4dbc-ac60-94062efa61c3" />

# Database Information
Name of Database: Mb_b7

Additional info: All queries are bookmarked as stored procedures

