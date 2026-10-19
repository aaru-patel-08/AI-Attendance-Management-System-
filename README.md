
📸 AI-Attendance-Management-System-

> A web-based attendance management application that uses face recognition and computer vision to help identify registered people and manage attendance records.

AI-Attendance-Management-System is built with Python and Flask, with HTML templates and static CSS/JavaScript files powering the web interface.
The application uses a local folder for registered face images and
stores attendance records locally. It is designed as a practical project
for learning and demonstrating face-recognition-based attendance
workflows.

✨ Features

  Feature                             Description
   -----------------------------------
  📷 **Camera-Based Scanning**        Uses the camera through the web
                                      application for face-scanning
                                      workflows.

  🧠 **Face Recognition**             Uses the project's Python
                                      face-recognition and
                                      computer-vision dependencies to
                                      work with registered faces.

  👤 **Local Face Profiles**          Registered face images are loaded
                                      from the local `known_faces/`
                                      folder.

  🗓️ **Attendance Records**           Attendance data is managed  locally   
                                      by the application.

  🖥️ **Web Interface**                Flask serves the pages using HTML
                                      templates, CSS, and JavaScript.

  📊 **Attendance File Support**      The project uses Python
                                      data-handling packages for local
                                      attendance-file workflows.

  🔒 **Local Personal Data**          Face images and attendance
                                      spreadsheets can remain on the
                                      user's computer instead of being
                                      published in the repository.
  -----------------------------------------------------------------------

> Feature availability depends on the current application code and local configuration. This README describes the Flask-based project structure, not the older React/FastAPI version.

------------------------------------------------------------------------

## 🏗️ System Architecture

The application uses a Flask-based web architecture:

┌─────────────────────────────────────────────────────┐
│                  Web Browser                        │
│         HTML templates + CSS + JavaScript           │
└──────────────────────────┬──────────────────────────┘
                           │ HTTP requests
                           ▼
┌─────────────────────────────────────────────────────┐
│                   Flask App                         │
│                     app.py                           │
│       Application routes and attendance logic       │
└──────────────────────────┬──────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────┐
│        Computer Vision & Local Data Files           │
│  Face-recognition dependencies, known_faces/,       │
│              attendance_records/                    │
└─────────────────────────────────────────────────────┘

------------------------------------------------------------------------

🛠️ Tech Stack

  ----------------------------------------------------------------------
  Area                    Technology              Purpose
  ----------------------- ----------------------- 
  Frontend**            HTML5, CSS3, JavaScript   Builds the web pages
                                                  and client-side
                                                  interactions

  Backend / Web         Python, Flask             Runs the web
  Framework**                                     application and handles requests
      
  Computer Vision**     OpenCV                    Image and camera
                                                  processing

  Face Recognition**    `face_recognition`        Face-recognition
                                                  functionality, as used
                                                  by the project

  Data Handling**       Pandas, OpenPyXL          Supports local
                                                  attendance spreadsheet
                                                  workflows

  
  ---------------------------------------------------------------------

📁 Project Structure

SmartFace-Attendance-System/
├── app.py                       # Flask application
├── requirements.txt             # Python dependencies
├── .gitignore                   # Excludes private/local files from Git
├── known_faces/
│   └── .gitkeep                 # Keeps the empty folder in Git
├── attendance_records/          # Local attendance files (not committed)
├── static/
│   ├── css/
│   │   └── styles.css           # Application styles
│   └── js/
│       ├── dashboard.js         # Dashboard interactions
│       └── script.js            # Client-side application logic
└── templates/
    ├── dashboard.html           # Dashboard page
    └── index.html               # Main page

The `known_faces/` and `attendance_records/` directories may be empty or
need to be created after cloning because private data files are
intentionally not included in the public repository.

------------------------------------------------------------------------
🚀 Getting Started

Prerequisites

  Tool                 Purpose
  -------------------- ------------------------------------
  **Python**           Runs the Flask application
  **pip**              Installs Python packages
  **Git**              Clones the repository
  **Webcam**           Required for camera-based scanning
  **Modern browser**   Opens the web interface

Face-recognition packages can have operating-system and Python-version
requirements. Use a Python version compatible with the packages listed
in `requirements.txt`.

1. Clone the repository

git clone https://github.com/aaru-patel-08/AI-Attendance-Management-System-.git
cd AI-Attendance-Management-System-

2. Create a virtual environment

**Windows PowerShell:**

``` powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

``` bash
python3 -m venv .venv
source .venv/bin/activate
```
3. Install dependencies

``` bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If installation fails for a computer-vision or face-recognition
dependency, read the complete error output and follow that package's
installation instructions for your operating system.

4. Prepare local data folders

Create the folders if they are not already present:

``` text
known_faces/
attendance_records/
```
Add the face images you are authorized to use to `known_faces/`. Follow
the naming format expected by `app.py`. Do not upload real face images
or attendance spreadsheets to a public repository.

The application may create or update attendance files in
`attendance_records/` during use.

5. Run the application

``` bash
python app.py
```

Open the local address shown in the terminal. If the application uses
Flask's default local address, it is commonly:

``` text
http://127.0.0.1:5000/
```

Allow camera access in the browser if the application requests it.

------------------------------------------------------------------------

🔐 Privacy and Security

Face images and attendance records can contain sensitive personal
information.

-   Keep real registered face images out of the public repository.
-   Keep attendance spreadsheets and other personal records private.
-   Keep `.env` files, passwords, API keys, and credentials out of Git.
-   Check `.gitignore` before every upload.
-   Obtain appropriate permission before collecting or processing
    anyone's face image.
-   Use this project locally for development and demonstration. Do not
    expose Flask's development server directly to the public internet
    for production use.

The `.gitignore` should exclude local face images and attendance
spreadsheets, for example:

``` gitignore
known_faces/*
!known_faces/.gitkeep
attendance_records/*.xlsx
__pycache__/
*.pyc
.venv/
venv/
.env
```

------------------------------------------------------------------------

🧰 Troubleshooting

The camera does not start

-   Confirm the webcam is connected and not being used by another
    application.
-   Allow camera access in the browser and operating-system settings.
-   Check the terminal for application errors.

A face is not recognized

-   Confirm that the registered image is in `known_faces/`.
-   Check the image filename format expected by the code.
-   Try a clear, well-lit image and check the terminal output.

Python packages fail to install

-   Confirm that your virtual environment is active.
-   Check your Python version against the dependencies in
    `requirements.txt`.
-   Some computer-vision packages may require additional native build
    tools.

Attendance records are not saved

-   Confirm that `attendance_records/` exists and is writable.
-   Check the terminal output for errors related to file access or
    spreadsheet handling.

------------------------------------------------------------------------

📌 Notes

-   This repository documents the Flask-based SmartFace Attendance
    System.
-   Personal face images and generated attendance files are local
    runtime data and are not required to be committed to GitHub.
-   A new user should register or provide their own authorized test face
    images before trying face-recognition functionality.

👩‍💻 Author

Aarju Dholariya

------------------------------------------------------------------------

🙏 Acknowledgements

-   [Python](https://www.python.org/) --- Programming language
-   [Flask](https://flask.palletsprojects.com/) --- Web framework
-   [OpenCV](https://opencv.org/) --- Computer vision library
-   [face_recognition](https://github.com/ageitgey/face_recognition) ---
    Face-recognition library
-   [Pandas](https://pandas.pydata.org/) --- Data analysis and
    manipulation
-   [OpenPyXL](https://openpyxl.readthedocs.io/) --- Excel file handling
