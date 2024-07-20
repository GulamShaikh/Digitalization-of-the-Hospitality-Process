# Digitalization of the Hospitality Process 

# Overview:
The “Digitalization of the Hospitality Process” web application streamlines group accommodation by allowing users to upload two CSV files: one containing group information and the other containing hostel details. The goal is to allocate rooms efficiently while ensuring that group members with the same ID stay together and adhere to gender-specific accommodations and hostel capacities.

# File Descriptions:
1. Group Information CSV (group_file):
- Contains data about groups with a common ID.
- Each row specifies the group ID, the number of members, and their gender (boys or girls).
- Example entries:
Group 101: 3 members (Boys)
Group 102: 4 members (Girls)
Group 103: 2 members (Boys)
Group 104: 5 members (Girls)
Group 105: 8 members (5 boys + 3 girls)

2. Hostel Information CSV (hostel_file):
Contains details about hostel rooms, including the hostel name, room number, capacity, and gender accommodation.
Example entries:
Boys Hostel A, Room 101: Capacity 3 (Boys)
Boys Hostel A, Room 102: Capacity 4 (Boys)
Girls Hostel B, Room 201: Capacity 2 (Girls)
Girls Hostel B, Room 202: Capacity 5 (Girls)

# Application Logic:
1. Upload CSV Files:
Users upload group information and hostel information CSV files via a web form.
2. Room Allocation:
The application reads both CSV files and parses the data.
It separates boys’ and girls’ hostels.
For each group, it allocates an appropriate hostel room based on group size and gender.
If a room can accommodate the group, it assigns the room and updates the remaining capacity.
This process continues until all groups are allocated rooms.
3. Output:
The application generates a CSV file with room allocation details, which users can download.

# Instructions to Run the Application:

1. Environment Setup:
Ensure Python is installed on your machine.
Install required Python packages using:
pip install flask pandas

2. Project Structure:
Digitalization of the Hospitality Process
├── web.py
├── index.html
├── style.css
└── uploads/ (directory to save uploaded files)

3. Create Directories:
Create an “uploads/” directory within your project folder to store uploaded files.

4. Add Files:
Place your “web.py” file in the root directory of the project.

5. Run the Application:
Navigate to the project directory in your terminal.
Start the Flask application with:
python web.py
Access the application in your web browser

7. Usage:
Upload the group information CSV file.
Upload the hostel information CSV file.
Click the “Upload (Allocate Rooms)” button to process the files.
Download the resulting CSV file with room allocation details.
