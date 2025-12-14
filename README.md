# Court Filing System (Python CLI)

A menu-driven Python command-line application for managing court case records.  
The system allows users to add, search, view, and analyze case files such as pending, ongoing, completed, and juvenile cases.

---

## Features

- Input new court cases
- Search cases by suspect name
- Find similar cases by case type
- View verdicts of cases
- View full archive and simplified archive
- Delete wrongly entered (misinput) cases
- Display random Supreme Court judge information
- View statistics:
  - Total cases
  - Completed cases
  - Pending cases
  - Ongoing cases
  - Juvenile cases
- Displays total execution time on exit

---

## Technologies Used

- Python 3
- MySQL Connector (imported, database connection initialized)
- Standard Python libraries:
  - `random`
  - `os`
  - `time`

---

## Project Structure

- Case records are stored in a **list of dictionaries**
- Each case contains:
  - `name`
  - `age`
  - `gender`
  - `case`
  - `status`
  - `verdict`

---

## Menu Options

```
0   - Show menu
1   - Input new case
2   - Find file of a case by name
3   - Find similar cases
4   - View verdict of a case
5   - View full archive
6   - View simplified archive
7   - Delete a misinput case
8   - About judge (randomly selected)
9   - Total cases
10  - Completed cases
11  - Pending cases
12  - Ongoing cases
13  - Juvenile cases
99  - Exit program
clear - Clear screen
```

---

## How to Run

1. Ensure **Python 3** is installed.
2. Install MySQL connector if required:
   ```
   pip install mysql-connector-python
   ```
3. Make sure MySQL is running and a database named `courtfill` exists.
4. Run the program:
   ```
   python court_filing.py
   ```

---

## Notes

- The MySQL connection is initialized but the current version stores data **in memory only**.
- All entered cases are lost once the program exits.
- Juvenile cases are identified as suspects with age **below 18**.
- Gender input accepts:
  - `M` → Male
  - `F` → Female
  - `0` → Not specified

---

## Sample Case Entry

```
Name    : Jai
Age     : 16
Gender  : Male
Case    : Under age driving
Status  : Pending
Verdict : To be written
```

---

## Exit Information

On exiting the program, total time spent is displayed:
```
Time Used: XX seconds
Thank you for using me!
```

---

## Future Improvements

- Persistent database storage (CRUD with MySQL)
- Authentication system
- Role-based access (Clerk / Judge / Admin)
- Case ID generation
- Export cases to PDF or CSV
- Improved error handling

---

## Author

Pranav Kumar  
B.Tech Computer Science (AIML)  
Manipal Institute of Technology
