Music Player
================

Introduction
------------

**MAD Music Player** is a desktop-based music player application built with Java, JavaFX, and SQLite. The application demonstrates the principles of a **3-tier architecture** and emphasizes robust database management using SQLite — a lightweight, serverless relational database engine. It supports user authentication, media playback, and song library management, making it a well-rounded example of desktop application development with integrated data persistence.

The use of SQLite enables a portable and easily manageable solution for storing user credentials and audio file metadata without the need for an external database server. All data interactions are handled through standard SQL queries using JDBC.

Installation and Setup
----------------------

### Prerequisites

Ensure the following are installed on your system:

*   Java 17 SDK
    
*   JavaFX SDK (for GUI components)
    
*   Gradle (comes pre-wrapped in this project)
    

### How to Build and Run

1.  _git clone_ [_https://github.com/goutham-1902/Music-Player-Using-SQLite-and-Java.git_](https://github.com/goutham-1902/Music-Player-Using-SQLite-and-Java.git)_cd Music-Player-Using-SQLite-and-Java_
    
2.  _./gradlew build_
    
3.  _java -cp build/libs/MAD\_MusicPlayer-1.0.jar:sqlite-jdbc-3.49.1.0.jar Main_On Windows, replace _:_ with _;_ in the classpath.
    

Architecture Overview
---------------------

This project follows a **3-tier architecture**:

### Presentation Layer

Implemented using JavaFX (with a Swing fallback), this layer includes all UI components:

*   _LoginScreen_
    
*   _UserDashboard_
    
*   _AdminPanel_
    

### Business Logic Layer

Handles authentication, audio playback, and control logic. Core classes:

*   _AuthManager_
    
*   _AudioPlayer_
    
*   _SongManager_
    

### Data Access Layer

Responsible for database interactions:

*   _DbManager_: Initializes and connects to the SQLite database
    
*   _DbAssist_: Handles basic SQL operations (insert, update, delete)
    
*   _DbFinder_: Handles search and retrieval queries
    

All interactions are managed via **JDBC**.

Database Design and Management
------------------------------

The application uses SQLite to store:

*   User credentials and roles (admin/user)
    
*   Song metadata (title, path, artist info, etc.)
    

The _songs.db_ file is located in the _data/_ directory and is automatically created and initialized on the first run if not found.

SQLite ensures the application is **self-contained**, making it ideal for lightweight desktop applications.

Future Work
-----------

Planned enhancements include:

*   Multi-user support with session-based access
    
*   Cloud-based storage and synchronization for songs and user data
    
*   Enhanced user interfaces using JavaFX with animations and styling
    
*   Playlist creation and persistent customization features
    
*   Support for audio streaming and real-time song suggestions
    

Connect
-------

If you’re interested in the project or want to connect professionally, feel free to reach out:

[Connect with me on LinkedIn](https://www.linkedin.com/in/your-link-here)
