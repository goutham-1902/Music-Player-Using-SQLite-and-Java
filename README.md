MAD Music Player
Introduction
MAD Music Player is a desktop-based music player application built with Java, JavaFX, and SQLite. The application demonstrates the principles of a 3-tier architecture and emphasizes robust database management using SQLite — a lightweight, serverless relational database engine. It supports user authentication, media playback, and song library management, making it a well-rounded example of desktop application development with integrated data persistence.

The use of SQLite enables a portable and easily manageable solution for storing user credentials and audio file metadata without the need for an external database server. All data interactions are handled through standard SQL queries using JDBC.

Installation and Setup
Prerequisites
Ensure the following are installed on your system:

Java 17 SDK

JavaFX SDK (for GUI components)

Gradle (comes pre-wrapped in this project)

How to Build and Run
Clone this repository:

bash
Copy
Edit
git clone https://github.com/goutham-1902/Music-Player-Using-SQLite-and-Java.git
cd Music-Player-Using-SQLite-and-Java
Build the project using Gradle wrapper:

bash
Copy
Edit
./gradlew build
Run the application:

bash
Copy
Edit
java -cp build/libs/MAD_MusicPlayer-1.0.jar:sqlite-jdbc-3.49.1.0.jar Main
On Windows, replace : with ; in the classpath.

Architecture Overview
This project follows a 3-tier architecture:

Presentation Layer
Implemented using JavaFX (Swing fallback), this layer includes all UI components like LoginScreen, UserDashboard, and AdminPanel.

Business Logic Layer
This layer handles authentication, audio playback, and control logic. Classes such as AuthManager, AudioPlayer, and SongManager manage this functionality.

Data Access Layer
The core of this project, this layer includes:

DbManager: Initializes and connects to the SQLite database.

DbAssist: Handles basic SQL operations (insert, update, delete).

DbFinder: Handles search and retrieval queries.

All interactions with the database are managed through JDBC.

Database Design and Management
The application leverages SQLite for storing:

User credentials and roles (admin/user)

Song metadata (title, path, artist info, etc.)

The songs.db file acts as the local database, located in the data/ directory. The database is accessed via SQL through JDBC. Tables are created and initialized automatically on the first run if not found.

SQLite ensures that the application is self-contained, with no need for separate database server setups, making it ideal for lightweight desktop applications.

Future Work
Planned enhancements and areas of improvement include:

Multi-user support with session-based access

Cloud-based storage and synchronization for songs and user data

Enhanced user interfaces using JavaFX with animations and styling

Playlist creation and persistent customization features

Support for audio streaming and real-time song suggestions

Connect
If you’re interested in the project or want to connect professionally, feel free to reach out:

Connect with me on LinkedIn

