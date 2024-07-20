# Digitalization of the Hospitality Process 

# Application Overview:
This web application facilitates the digitalization of the hospitality process for group accommodation. It allows users to upload two CSV files containing group information and hostel information to efficiently allocate rooms in hostels while ensuring group members with the same ID stay together and adhere to hostel capacities and gender-specific accommodations.


# File Descriptions:
1. Group Information CSV (group_file):
- Contains information about groups with a common ID.
- Each row represents a group, specifying the group ID, the number of members, and the gender (boys or girls).
- Group ID| Members |Gender
     101,     3,     Boys
     102,     4,     Girls
     103,     2,     Boys
     104,     5,     Girls
    105,    8(5+3)   Boys+Girls

2. Hostel Information CSV (hostel_file)
- Contains information about the hostels and their room capacities.
- Each row represents a hostel room, specifying the hostel name, room number, room capacity, and gender accommodation (boys or girls).
- Hostel Name  | Room Number | Capacity | Gender
  Boys Hostel A,   101,          3,        Boys
  Boys Hostel A,   102,          4,        Boys
  Girls Hostel B,  201,          2,        Girls
  Girls Hostel B,  202,          5,        Girls

# Application Logic:
1. Upload CSV Files: Users upload the group information and hostel information CSV files through a web form.
2. Room Allocation:
- The application reads both CSV files and parses the data.
- It separates boys' and girls' hostels.
- It iterates through each group and tries to allocate them to an appropriate hostel room based on the group's size and gender.
- If a room can accommodate the group, it allocates the room and updates the remaining capacity of the room.
- This process continues until all groups are allocated rooms.
3. Output: The application generates a CSV file showing the allocation details, which users can download.

# Instructions to Run the Application:

1. Setup the Environment:

- Ensure you have Python installed on your machine.
- Install the required Python packages using the following command:
- pip install flask pandas

2. Project Structure:
Hospitality Process-Digitally
├── web.py
├── index.html
├── style.css
├── uploads/  (directory to save uploaded files)

3. Create Directories:
- Create an uploads/ directory inside your project directory to store uploaded files.

4. Add Files:
- Ensure your web.py file is in the root directory of the project.

5. Run the Application:
- Navigate to the project directory in your terminal.
- Start the Flask application with the following command:
python web.py
- Open a web browser and navigate to http://127.0.0.1:5000/ to access the application.

6. Usage:
- Upload the group information CSV file.
- Upload the hostel information CSV file.
- Click the "Upload(Allocate Rooms)" button to process the files.
- Download the resulting CSV file with the room allocation details.
