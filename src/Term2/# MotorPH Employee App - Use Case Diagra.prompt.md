# MotorPH Employee App - Use Case Diagram Plan

## System Overview

**Project**: MotorPH Employee Management System  
**Purpose**: Payroll and HR management for Philippine company (MotorPH)

---

## 1. Actors

### Primary Actors
- **HR Staff / Admin**
  - Role: Manages employee records, payroll, and leave requests
  - Login: admin@motorph.com / MotorPH2025
  
- **Employee**
  - Role: Views personal information, submits requests, accesses payroll data
  - Login: Individual employee credentials

### Excluded (Internal/System Logic)
- System Administrator (not a user-facing role)

---

## 2. User-Level Use Cases

### HR Staff Use Cases
- [ ] **Login** - Authenticate with credentials
- [ ] **Create Employee** - Add new employee record
- [ ] **View Employee** - Display employee list and details
- [ ] **Update Employee** - Edit employee information
- [ ] **Delete Employee** - Remove employee record
- [ ] **Process Payroll** - Calculate and generate payslips
- [ ] **View Payroll** - Access salary information by month
- [ ] **Approve Leave Request** - Process employee leave requests
- [ ] **Reject Leave Request** - Deny employee leave requests
- [ ] **View Tax Forms** - Access tax documentation
- [ ] **Track Attendance** - Monitor employee hours worked
- [ ] **Logout** - End session

### Employee Use Cases
- [ ] **Login** - Authenticate with credentials
- [ ] **View Own Information** - Access personal/employment details
- [ ] **Submit Leave Request** - Request time off with dates and type
- [ ] **View Leave Request Status** - Check request approval status
- [ ] **View Attendance Records** - Check logged hours
- [ ] **View Payroll Information** - Access salary data
- [ ] **Download Tax Form** - Generate/download tax documentation
- [ ] **Logout** - End session

---

## 3. Internal Logic to EXCLUDE

These are system implementation details, NOT use cases:
- [ ] ~~CSV Data Persistence~~
- [ ] ~~Load/Save Employees~~
- [ ] ~~Theme Management (Light/Dark Mode)~~
- [ ] ~~Keyboard Shortcuts Handling~~
- [ ] ~~Status Bar Updates~~
- [ ] ~~Animation Effects~~
- [ ] ~~Database Transactions~~
- [ ] ~~Salary Calculation Algorithm~~ (part of "Process Payroll" use case)

---

## 4. UCD Diagram Structure

```
System: MotorPH Employee Management

┌────────────────────────────────────────────────────────────────────┐
│                                                                    │
│  ┌──────────────────────────────────────────────────────────────┐ │
│  │                                                              │ │
│  │  [HR Staff] ──┐                                             │ │
│  │               │                                             │ │
│  │           ╭───┴────╮                                        │ │
│  │           │  Login  │                                       │ │
│  │           ╰────────╯                                        │ │
│  │               │                                             │ │
│  │         ╭─────┼─────╮                                       │ │
│  │         │     │     │                                       │ │
│  │     ╭───┴─╮ ╭─┴──╮ ╭┴──────╮                               │ │
│  │     │View │ │Create│View    │                             │ │
│  │     │Empl.│ │Empl. │Payroll │                             │ │
│  │     ╰──────╯ ╰──────╯ ╰────────╯                            │ │
│  │         │     │     │                                       │ │
│  │     ╭───┴─╮ ╭─┴──╮ ╭┴──────╮                               │ │
│  │     │Upd. │ │Del. │Approve │                              │ │
│  │     │Empl.│ │Empl.│ Leave  │                              │ │
│  │     ╰──────╯ ╰──────╯ ╰────────╯                            │ │
│  │                                                              │ │
│  │     ╭───────────╮    ╭──────────╮    ╭────────╮            │ │
│  │     │  Reject  │    │   Track  │    │ Logout │            │ │
│  │     │  Leave   │    │ Attendance│    │        │            │ │
│  │     ╰───────────╯    ╰──────────╯    ╰────────╯            │ │
│  │                                                              │ │
│  │  [Employee] ──┐                                            │ │
│  │               │                                             │ │
│  │           ╭───┴────╮                                        │ │
│  │           │  Login  │                                       │ │
│  │           ╰────────╯                                        │ │
│  │               │                                             │ │
│  │         ╭─────┼──────╮                                      │ │
│  │         │     │      │                                      │ │
│  │     ╭───┴──╮ ╭┴──────╮ ╭──────────╮                        │ │
│  │     │View  │ │Submit │ │View      │                       │ │
│  │     │Info  │ │ Leave │ │Payroll   │                       │ │
│  │     ╰──────╯ ╰───────╯ ╰──────────╯                        │ │
│  │         │     │      │                                      │ │
│  │     ╭───┴──╮ ╭┴───────╮ ╭────────────╮                     │ │
│  │     │Track │ │View    │ │  Download │                     │ │
│  │     │Hours │ │Leave   │ │   Tax     │                     │ │
│  │     ╰──────╯ ╰────────╯ ╰────────────╯                     │ │
│  │                                                              │ │
│  │             ╭────────╮                                      │ │
│  │             │ Logout │                                      │ │
│  │             ╰────────╯                                      │ │
│  │                                                              │ │
│  └──────────────────────────────────────────────────────────────┘ │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

---

## 5. Diagram Standards (UML)

- **Actors**: Stick figures or UML actor rectangles
- **Use Cases**: Ovals/ellipses
- **Associations**: Lines connecting actors to use cases
- **System Boundary**: Rectangle encompassing all use cases
- **Notation**: Clean, readable, standard UML format

---

## 6. Next Steps

1. [ ] Validate actors and use cases above
2. [ ] Remove/refine any items not matching user-level goals
3. [ ] Create diagram in draw.io or Lucidchart
4. [ ] Use standard UML notation
5. [ ] Ensure clean, readable layout
6. [ ] Export as PNG/JPG/PDF
7. [ ] Submit for review

---

## 7. Notes & Questions

- **Question 1**: Should we include separate use cases for "Approve" and "Reject" leave, or combine as one "Process Leave Request"?
- **Question 2**: Is "Track Attendance" a standalone use case, or should it be part of "View Reports"?
- **Question 3**: Do employees need a separate "View Payroll" use case, or is this combined with "View Personal Information"?

---
