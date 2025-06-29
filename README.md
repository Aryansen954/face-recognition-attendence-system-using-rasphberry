# 👁️‍🗨️ Face Recognition-Based Smart Attendance System 📋

This project is a **Raspberry Pi-based automatic attendance system** using **face recognition**. It identifies registered individuals using a webcam, displays a welcome message on an LCD, triggers a buzzer sound, and uploads the attendance data to **ThingSpeak** with the subject name and date.

---

## ✅ Features

- 🔍 **Face Recognition** using the `face_recognition` library
- 📷 Real-time webcam input using OpenCV
- 🧠 Marks attendance
Also use:

RPi.GPIO for GPIO pin control

ThingSpeak account and API Key

📁 Project Files
attendance.py – Main Python script

*.jpeg – Images of all known individuals for face training

README.md – Project documentation

📝 How It Works
The system loads stored face images and generates encodings.

It opens the camera and checks each frame for faces.

If a known face is found:

Attendance is marked via ThingSpeak API.

LCD displays “Welcome” + Name.

Buzzer beeps as feedback.

If an unknown face is detected, it is ignored.

You can stop the system by pressing q.

📡 ThingSpeak Integration
You must create a ThingSpeak channel and get your API Key. Replace the API key in the script here:

python
Copy
Edit
THINGSPEAK_API_KEY = "YOUR_API_KEY_HERE"
📷 Example Output
LCD shows:

nginx
Copy
Edit
Welcome
Akanksha Yadav
Terminal:

nginx
Copy
Edit
Attendance marked for Akanksha Yadav on ThingSpeak.
🔐 Face Image Naming Convention
Make sure to store clear, front-facing images of each person in the working directory, and use appropriate names like:

python-repl
Copy
Edit
akankshayadav.jpeg
ankita.jpeg
golu.jpeg
...
Ensure the known_faces dictionary in the script correctly maps names to images.

📌 To Run the System
bash
Copy
Edit
python3 attendance.py
Enter the subject name when prompted. The system will start recognizing faces.

🧹 Cleanup & Exit
Release camera resources

Close all OpenCV windows

Reset all GPIO pins

🙋‍♂️ Developed By
Aryan Sen
Electronics & Communication Engineering
Specializing in Embedded Systems and IoT Solutions

📝 License
This project is open-source and free to use under the MIT License.
