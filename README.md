# Python Activity-Based Learning

Python solutions for 10 case studies, each with a problem statement, objectives, assumptions, flowchart, algorithm, pseudocode, source code, test cases, output screenshots and conclusion.

## Student Details

| Field | Details |
|---|---|
| Name | BOPPUDI KARTHIK |
| Roll No. | 26000451 |
| Branch | CSE |
| Section | 1 |

## Complete Record

The full practical record, including all flowcharts, algorithms and pseudocode: [Python_Practical_Record_10_Problems.pdf](Python_Practical_Record_10_Problems.pdf)

## Syllabus Used

Computational thinking, algorithms, flowcharts, pseudocode, variables, data types, operators, conditional statements, loops, strings, pattern generation, lists, nested lists, tuples, tuple operations and unpacking.

## List of Programs

| No. | Case Study | Title | Main Concept | Code |
|---|---|---|---|---|
| 1 | 4 | Employee Payroll and Deduction Analysis | Variables, data types, arithmetic, if/elif/else | [p01_payroll.py](programs/p01_payroll.py) |
| 2 | 39 | Multi-Stage Examination Eligibility System | Compound conditions, independent if statements, lists | [p02_eligibility.py](programs/p02_eligibility.py) |
| 3 | 12 | Attendance Recovery Computation | for loop over a tuple, nested while loop | [p03_attendance.py](programs/p03_attendance.py) |
| 4 | 13 | ATM Transaction Sequence Simulation | Counted loop, if/elif ladder, accumulators | [p04_atm.py](programs/p04_atm.py) |
| 5 | 29 | Password Policy Validation Engine | String traversal, indexing and string methods | [p05_password.py](programs/p05_password.py) |
| 6 | 35 | Text Compression Using Character Runs | Run-length encoding, string building | [p06_compression.py](programs/p06_compression.py) |
| 7 | 37 | Nested Loop Calendar Generator | Nested loops and formatted pattern output | [p07_calendar.py](programs/p07_calendar.py) |
| 8 | 42 | Student Marks Matrix Analysis | Nested lists, row-wise and column-wise processing | [p08_marks.py](programs/p08_marks.py) |
| 9 | 51 | Bus Passenger Occupancy Simulation | List history, running count, searching a list | [p09_bus.py](programs/p09_bus.py) |
| 10 | 49 | Tuple-Based Product Catalogue Audit | Tuples, tuple unpacking and lists | [p10_catalogue.py](programs/p10_catalogue.py) |

## How to Run

Requires Python 3.6 or later. No external libraries are needed.

```bash
cd programs
python3 p01_payroll.py
```

On Windows, use `python` in place of `python3`. Type each value when prompted and press Enter. Enter numbers where numbers are asked; non-numeric text in a numeric field is not handled.

## Repository Structure

```text
Python-Activity-Based-Learning/
├── README.md
├── Python_Practical_Record_10_Problems.pdf
├── programs/
│   ├── p01_payroll.py
│   ├── p02_eligibility.py
│   ├── p03_attendance.py
│   ├── p04_atm.py
│   ├── p05_password.py
│   ├── p06_compression.py
│   ├── p07_calendar.py
│   ├── p08_marks.py
│   ├── p09_bus.py
│   └── p10_catalogue.py
└── screenshots/            (2 output screenshots per program)
```

## Program Details

### 1. Employee Payroll and Deduction Analysis

A company wishes to generate a monthly salary statement for an employee. Write a Python program that reads the employee name, basic pay, overtime hours and incentive amount. The program must compute House Rent Allowance (HRA) at 20% of basic pay, Dearness Allowance (DA) at 10% of basic pay and overtime pay at Rs. 200 per hour, and add these with the basic pay and incentive to obtain the gross salary. Tax is deducted progressively on the gross salary: nil on the first Rs. 30,000, 5% on the portion from Rs. 30,000 to Rs. 60,000, and 10% on the portion above Rs. 60,000. Provident Fund (PF) is deducted at 12% of basic pay. The program must display a formatted salary statement ending with the net salary, and reject invalid input.

**Source code:** [programs/p01_payroll.py](programs/p01_payroll.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `Asha / 40000 / 10 / 3000` | Gross 57000.00; Tax 1350.00; PF 4800.00; Net 50850.00 | Pass |
| Boundary (gross = 60000) | `Ravi / 40000 / 0 / 8000` | Gross 60000.00; Tax 1500.00; Net 53700.00 | Pass |
| Special (top slab) | `Meena / 60000 / 20 / 5000` | Gross 87000.00; Tax 4200.00; Net 75600.00 | Pass |
| Invalid | `Kiran / -5000 / 2 / 0` | Invalid input message | Pass |

**Output screenshots**

<img src="screenshots/p01_payroll_output1.png" alt="Employee Payroll and Deduction Analysis: Normal" width="560">

<img src="screenshots/p01_payroll_output2.png" alt="Employee Payroll and Deduction Analysis: Special (top slab)" width="560">

### 2. Multi-Stage Examination Eligibility System

A college permits a student to write the final examination only if all of the following hold: attendance of at least 75%, all 10 laboratory experiments completed, at least 20 internal marks out of 50, and fees cleared. Write a Python program that reads the attendance percentage, number of experiments completed, internal marks and fee status (Y/N). The program must declare the student eligible or not eligible and, when not eligible, list every unmet requirement, not only the first one.

**Source code:** [programs/p02_eligibility.py](programs/p02_eligibility.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal (eligible) | `82 / 10 / 35 / Y` | ELIGIBLE | Pass |
| Boundary | `75 / 10 / 20 / y` | ELIGIBLE | Pass |
| All conditions fail | `68.5 / 8 / 15 / N` | NOT ELIGIBLE with 4 reasons | Pass |
| Invalid | `105 / 10 / 30 / Y` | Invalid input message | Pass |

**Output screenshots**

<img src="screenshots/p02_eligibility_output1.png" alt="Multi-Stage Examination Eligibility System: Normal (eligible)" width="560">

<img src="screenshots/p02_eligibility_output2.png" alt="Multi-Stage Examination Eligibility System: All conditions fail" width="560">

### 3. Attendance Recovery Computation

A student wants to know how many consecutive classes must be attended to reach the required attendance percentage. Write a Python program that reads the number of classes conducted, the number attended and the required percentage. It must display the current percentage and then, for three scenarios in which the student first misses 0, 3 or 5 further classes, find the minimum number of consecutive classes to be attended afterwards to reach the requirement, along with the resulting percentage.

**Source code:** [programs/p03_attendance.py](programs/p03_attendance.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `40 / 26 / 75` | 65.00%; attend 16, 25, 31 | Pass |
| Boundary (exactly 75%) | `40 / 30 / 75` | 75.00%; attend 0, 9, 15 | Pass |
| Special (none attended) | `10 / 0 / 50` | 0.00%; attend 10, 13, 15 | Pass |
| Invalid | `30 / 35 / 75` | Invalid input message | Pass |

**Output screenshots**

<img src="screenshots/p03_attendance_output1.png" alt="Attendance Recovery Computation: Normal" width="560">

<img src="screenshots/p03_attendance_output2.png" alt="Attendance Recovery Computation: Special (none attended)" width="560">

### 4. ATM Transaction Sequence Simulation

Simulate a sequence of ATM transactions. The program reads an opening balance and the number of transactions. For each transaction it reads the type (D for deposit, W for withdrawal) and the amount. An amount must be a positive multiple of Rs. 100; a single withdrawal must not exceed Rs. 10,000; and a minimum balance of Rs. 500 must remain. Invalid transactions must be rejected with a reason. Finally, display the total deposited, total withdrawn, number of rejected transactions and final balance.

**Source code:** [programs/p04_atm.py](programs/p04_atm.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `5000 / 3 / D / 2000 / W / 1500 / W / 700` | Final balance 4800; 0 rejected | Pass |
| Boundary (min balance) | `1500 / 2 / W / 1000 / W / 100` | 1st accepted, 2nd rejected; balance 500 | Pass |
| Rejection rules | `20000 / 4 / X / 500 / D / 250 / W / 10100 / W / 10000` | 3 rejected; balance 10000 | Pass |
| Invalid | `300` | Invalid opening balance message | Pass |

**Output screenshots**

<img src="screenshots/p04_atm_output1.png" alt="ATM Transaction Sequence Simulation: Normal" width="560">

<img src="screenshots/p04_atm_output2.png" alt="ATM Transaction Sequence Simulation: Rejection rules" width="560">

### 5. Password Policy Validation Engine

Write a Python program that validates a password against the following policy: at least 8 characters; at least one uppercase letter, one lowercase letter, one digit and one special character; no spaces; no character repeated three times in a row; and it must not contain the substring "password" (in any letter case) or "123". The program must accept the password or reject it, explaining each failed condition.

**Source code:** [programs/p05_password.py](programs/p05_password.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal (strong) | `Sky@Blue47` | Accepted | Pass |
| Boundary (8 chars) | `Ab#4efgh` | Accepted | Pass |
| Several failures | `password123` | Rejected: uppercase, special, substring | Pass |
| Space and repetition | `Aaa 111` | Rejected: length, special, space, repetition | Pass |

**Output screenshots**

<img src="screenshots/p05_password_output1.png" alt="Password Policy Validation Engine: Normal (strong)" width="560">

<img src="screenshots/p05_password_output2.png" alt="Password Policy Validation Engine: Several failures" width="560">

### 6. Text Compression Using Character Runs

Write a Python program that compresses a text by replacing every group of consecutive identical characters with the character followed by the size of the group (for example, aaaabb becomes a4b2). Display the encoded text, the original and encoded lengths, and state whether the encoding is beneficial, gives no benefit, or makes the text longer. Empty text and text containing digits must be rejected, since digits would make the encoded form ambiguous.

**Source code:** [programs/p06_compression.py](programs/p06_compression.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `aaaabbbcccccc` | a4b3c6; 13 to 6; saves 7 | Pass |
| Boundary (same length) | `aabb` | a2b2; no benefit | Pass |
| Not beneficial | `abcd` | a1b1c1d1; 4 extra | Pass |
| Invalid | `ab12` | Invalid input message | Pass |

**Output screenshots**

<img src="screenshots/p06_compression_output1.png" alt="Text Compression Using Character Runs: Normal" width="560">

<img src="screenshots/p06_compression_output2.png" alt="Text Compression Using Character Runs: Not beneficial" width="560">

### 7. Nested Loop Calendar Generator

Write a Python program that prints the calendar of one month. The user supplies the number of days in the month (28 to 31) and the weekday on which day 1 falls (0 for Monday to 6 for Sunday). The dates must be printed week by week, correctly aligned under the weekday headings, using nested loops.

**Source code:** [programs/p07_calendar.py](programs/p07_calendar.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `30 / 6` | 30 days, 1st on Sunday | Pass |
| Boundary (28 days, Mon) | `28 / 0` | Exactly 4 full weeks | Pass |
| Special (31 days, Sat) | `31 / 5` | Six week rows | Pass |
| Invalid | `32 / 2` | Invalid input message | Pass |

**Output screenshots**

<img src="screenshots/p07_calendar_output1.png" alt="Nested Loop Calendar Generator: Normal" width="560">

<img src="screenshots/p07_calendar_output2.png" alt="Nested Loop Calendar Generator: Special (31 days, Sat)" width="560">

### 8. Student Marks Matrix Analysis

Write a Python program that stores the marks of up to 10 students in three subjects (Maths, Physics and Python) as a matrix. For each student, display the total and average. Identify the top performer or performers (including ties), compute each subject's average, and mark a subject as LOW if its average is below 50. Marks must be re-entered until exactly three values between 0 and 100 are given.

**Source code:** [programs/p08_marks.py](programs/p08_marks.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `3 / Anu / 78 85 90 / Bala / 45 38 62 / Charu / 88 40 75` | Anu tops (253); Physics 54.33 OK | Pass |
| Tie and weak subject | `2 / Dev / 60 30 90 / Esha / 90 40 50` | Two toppers (180); Physics LOW | Pass |
| Re-entry of bad marks | `1 / Farah / 105 60 70 / 50 50 50` | Prompt repeats; average 50.00 OK | Pass |
| Invalid | `0` | Invalid number message | Pass |

**Output screenshots**

<img src="screenshots/p08_marks_output1.png" alt="Student Marks Matrix Analysis: Normal" width="560">

<img src="screenshots/p08_marks_output2.png" alt="Student Marks Matrix Analysis: Tie and weak subject" width="560">

### 9. Bus Passenger Occupancy Simulation

Write a Python program that tracks the number of passengers on a bus. The user enters the bus capacity and number of stops and, at each stop, the number of passengers alighting and boarding. Passengers alight before others board. A record with a negative value, or with more passengers alighting than are on board, must be ignored. The program must flag each stop where capacity is exceeded and finally report occupancy by stop, the peak load and all violating stops.

**Source code:** [programs/p09_bus.py](programs/p09_bus.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `40 / 3 / 0 / 25 / 5 / 12 / 32 / 0` | Loads [25, 32, 0]; no violation | Pass |
| Over capacity | `30 / 3 / 0 / 28 / 2 / 10 / 6 / 0` | Loads [28, 36, 30]; violation at stop 2 | Pass |
| Bad record | `20 / 2 / 0 / 10 / 15 / 3` | Stop 2 ignored; loads [10, 10] | Pass |
| Invalid | `0 / 4` | Invalid capacity message | Pass |

**Output screenshots**

<img src="screenshots/p09_bus_output1.png" alt="Bus Passenger Occupancy Simulation: Normal" width="560">

<img src="screenshots/p09_bus_output2.png" alt="Bus Passenger Occupancy Simulation: Over capacity" width="560">

### 10. Tuple-Based Product Catalogue Audit

Write a Python program that audits a product catalogue. The user enters the number of records, a replenishment level and, for each record, a product ID, price and stock quantity. Store each record as a tuple and the catalogue as a tuple of tuples. A record is invalid if its ID repeats an earlier valid record, its price is not positive, or its stock is negative. For valid records display the inventory value (price x stock), then show the total value and the items whose stock is below the level, with the quantity needed to reach it.

**Source code:** [programs/p10_catalogue.py](programs/p10_catalogue.py)

**Test cases** (inputs are separated by `/` in the order typed)

| Test Case | Input | Expected Output | Status |
|---|---|---|---|
| Normal | `3 / 10 / P101 45.50 20 / P102 120 4 / P103 15 50` | Total 2140.00; P102 order 6 | Pass |
| Boundary (stock = level) | `1 / 5 / A1 10 5` | Value 50.00; no replenishment | Pass |
| Bad records | `4 / 5 / B1 20 0 / b1 20 8 / B2 -4 3 / B3 10 -1` | 3 invalid; B1 order 5 | Pass |
| Invalid | `0 / 5` | Invalid number message | Pass |

**Output screenshots**

<img src="screenshots/p10_catalogue_output1.png" alt="Tuple-Based Product Catalogue Audit: Normal" width="560">

<img src="screenshots/p10_catalogue_output2.png" alt="Tuple-Based Product Catalogue Audit: Bad records" width="560">
