# Hostel-Mgmt Project Planning Document
1. Problem Statement
Many hostels and PG accommodations still rely on manual registers and paper-based processes for managing student activities. Entry/exit records, mess attendance, visitor logs, and complaint management are maintained using books and handwritten records, which can lead to inefficiencies, data loss, inaccurate reporting, and increased administrative workload.

HostelFlow aims to digitize hostel operations by providing a centralized platform where students and hostel administrators can manage daily activities efficiently. The system will automate attendance tracking, entry/exit logging, complaint management, and administrative reporting, reducing manual effort and improving transparency.

Objectives

* Eliminate manual record keeping.
* Reduce administrative workload.
* Improve data accuracy.
* Provide real-time hostel activity monitoring.
* Generate reports automatically.

2. Features

Student Features

Authentication
* Student Login
* Logout
Entry / Exit Management
* Mark Entry
* Mark Exit
* View Entry/Exit History
Mess Attendance
* Mark Breakfast
* Mark Lunch
* Mark Dinner
* View Meal History
Complaint Management
* Raise Complaint
* Track Complaint Status
* View Previous Complaints
Profile
* View Personal Details
* View Room Information

Admin Features

Dashboard
* Total Students
* Students Currently Inside Hostel
* Students Currently Outside Hostel
* Today's Meal Count
* Open Complaints Count
Student Management
* Add Student
* Edit Student Details
* Delete Student
* Assign Rooms
Entry/Exit Monitoring
* View Live Entry Logs
* View Exit Logs
* Search Student Records
Mess Management
* View Daily Meal Attendance
* Generate Meal Reports
Complaint Management
* View Complaints
* Update Complaint Status
* Resolve Complaints
Reports
* Daily Reports
* Weekly Reports
* Monthly Reports

3. Database Tables
Students Table

```text
students
------------------------
student_id (PK)
name
email
phone
room_no
password
created_at
```

Purpose:
Stores student information.

---

Entry Logs Table

```text
entry_logs
------------------------
log_id (PK)
student_id (FK)
entry_time
exit_time
date
```

Purpose:
Tracks hostel movement.

---

Meal Attendance Table

```text
meal_attendance
------------------------
meal_id (PK)
student_id (FK)
meal_type
date
timestamp
```

meal_type:

```text
Breakfast
Lunch
Dinner
```

Purpose:
Tracks mess attendance.

---

Complaints Table

```text
complaints
------------------------
complaint_id (PK)
student_id (FK)
title
description
status
created_at
resolved_at
```

status:

```text
Open
In Progress
Resolved
```

Purpose:
Stores hostel complaints.

---

Admin Table

```text
admins
------------------------
admin_id (PK)
name
email
password
role
```

Purpose:
Stores administrator accounts.

---

4. Screens (UI Pages)

Screen 1: Login Page

```text
----------------------------------
          HOSTELFLOW

Email

Password

[ Login ]
----------------------------------
```

---

Screen 2: Student Dashboard

```text
----------------------------------
Welcome, Devamanya

[ Mark Entry ]

[ Mark Exit ]

[ Mark Breakfast ]

[ Mark Lunch ]

[ Mark Dinner ]

[ Raise Complaint ]

----------------------------------
```

---

Screen 3: Complaint Form

```text
----------------------------------
Complaint Title

Description

[ Submit Complaint ]
----------------------------------
```

---

Screen 4: Entry/Exit History

```text
----------------------------------
Date

Entry Time

Exit Time

----------------------------------
```

---

Screen 5: Meal History

```text
----------------------------------
Date

Meal Type

Time

----------------------------------
```

---

Screen 6: Admin Dashboard

```text
----------------------------------
HOSTELFLOW ADMIN

Total Students: 250

Inside Hostel: 180

Outside Hostel: 70

Today's Meals: 420

Open Complaints: 12

----------------------------------
```

---

Screen 7: Student Management

```text
----------------------------------
Student List

Search Student

Add Student

Edit Student

Delete Student
----------------------------------
```

---

Screen 8: Complaint Management

```text
----------------------------------
Complaint ID

Student Name

Status

Update Status

Resolve Complaint
----------------------------------
```

---
