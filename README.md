# sikuliSpotify

# Project description:
This project was created to test the Spotify Radio functionality in the desktop version downloaded from:  https://www.spotify.com/download
The project uses the following set of artifacts and their respective versions as defined in the build.gradle:
1.	JUnit having version 4.12.
2.	sikuli-api having version 1.2.0.
3.	sikulixapi having version 1.1.0.
4.	java having version 1.7 or more

The project was created using the IntelliJ IDEA Community Edition 2018.2 and Gradle as dependency management.

# Decision about how to handle test data
Due to this known bug: https://community.spotify.com/t5/Desktop-Windows/Remember-Me-option-is-always-selected-by-default/td-p/4534717
I had to guarantee that once the application is opened the username/Email is going to be deleted. This is attended in the method: “enterUserCredentials()”.
To handle the test data I decided to use Environment variables in gradle task.

# How to execute the project:
Option 1: In gradle Task “test” edit the arguments like follow: 
-Dspotify_appPath=C://Users//ttassin//AppData//Roaming//Spotify//Spotify.exe
-Dspotify_username=tatianetassinari85@gmail.com
-Dspotify_password=spotify2018
And then click on Run button in the right top of IDEA.
Option 2: Download the project, open the Terminal and send the command line:
gradlew clean test -Dspotify_appPath=C://Users//ttassin//AppData//Roaming//Spotify//Spotify.exe -Dspotify_username=tatianetassinari85@gmail.com -Dspotify_password=spotify2018

# Test Case that was automated
I added a Test case around "New Radio Station Creation" in the test script testCreateStation.java.
It logs in the application, go to Radio page, create a New Station to the artist radiohead, play, pause and logout.
Project Author: Tatiane Tassinari (tatianetassinari85@gmail.com)

