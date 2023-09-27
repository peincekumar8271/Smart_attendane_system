# Smart Attendance System with Python

This is a simple smart attendance system developed using Python. The system leverages face recognition technology to capture and recognize faces from a webcam feed, and then stores attendance records in a local database. The system can be used to automate the attendance marking process in various settings, such as classrooms or workplaces.

* **Requirements**
> 1. Python 3.x
> 2. OpenCV
> 3. face-recognition
> 4. openCV

* **Installation**
1. Ensure you have Python 3.x installed on your system.
2. Install the required libraries by running the following commands in your terminal or command prompt:
  > - pip install opencv-python
  > - pip install opencv-python-headless
  > - pip install numpy
  > - pip install face-recognition
  > - pip install sqlite3

* **Setup**
1. Create a new database file named attendance.ex.
2. Create a table named faces with columns for name (text) and encoding (text). The encoding column will store the face encodings of known individuals.

* **Usage**
1. Load the known face encodings and names from the faces table in the attendance.db database.
2. Run the Python script smart_attendance.py using the command:
   > - python smart_attendance.py
   
  A. The system will access the webcam and start recognizing faces. <br>
  B. When a known face is detected, the system will display the name on the video feed and mark attendance for that individual by adding their name and the current date to the attendance table in the attendance.db database.

* **Customization**
1. To add new individuals to the attendance system, you can manually encode their faces using the face_recognition.face_encodings() function and store the encodings along with their names in the faces table.
2. Modify the recognition parameters and display settings in the smart_attendance.py script to suit your requirements.

* **Important Notes**
1. is is a basic demonstration of a smart attendance system and may not be suitable for large-scale production use without further enhancements.
2. Ensure the privacy and consent of individuals whose faces are being recorded and stored in the system.
3. For a more secure and scalable solution, consider using a cloud-based database and implementing user authentication.

* **Acknowledgments**
1. The face recognition functionality is based on the face_recognition library by **Adam Geitgey**.
2. This project was inspired by the need to automate attendance marking in various environments.
