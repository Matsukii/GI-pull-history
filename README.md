# GI-pull-history
A pull history ouside of the game for Genshin impact



## Why?
The game have a history by pages of ~6 items and i need to open it to count and know how much pulls i did or what i took on each.

- For futre may be planned a version where you can just log in and upload a screenshot of the list and will be all added quickly and easy


## ! Warning
This is not a good solution if you do many pulls (like 20, 30 or more) at once.

## LICENSE: MIT


## How To Use
You will need a google account and a firebase project with realtime database and open read/write rules




## step-by-step
*This is a online database from google, if you prefer to not use online, there is the ["Firebase Emulator"](https://firebase.google.com/docs/emulator-suite) to use on your computer*

1. Have a Google account? login or create one
    - i'll be using one for example

2. Go to https://firebase.google.com
    - click on "Go to console" next to your profile picture and search bar
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/goToConsole.png"> <br>

3. If you never been here a blue screen show up,
click on "Create a project"

4. You will be guided to create it
    - Insert the name, read and accept the firebase terms
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/create1.png"> <br>
    
    - click on continue

5. You will be asked if want Analytics for the project
    - at the "Enable Google Analytics..." click to DISABLE
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/analytics.png"> <br>

6. Click on create a project and wait a bit
    - after finished, click on continue to be rediredted to your project overview

7. We want to add a web app, so click at the </> icon

    - <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/addWeb.png"><br>
    
    - Add the app name and click Register
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/appName.png"><br>

8. Done! project created and app added, the firebaseConfig will show up
    - copy the part from "var firebaseConfig..." up to "};" or just the project id, in my case it is "gi-pull-list-example", the name i gave
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/config.png"><br>
    
    - click on "Continue to console"

9. After goes back to overview, click on "Develop" to expand

    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/develop.png"><br>
    
    - click on "Realtime database"
    
    - After page change and load, click on "create database"
    
    - A popup asking about "Realtime Database security rules" will be showe, leave it in "locked" and click at "Activate"

10. Wait it all load, your database is created!

    - now click on "Rules"
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/rules0.png">
    <br>
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/rules1.png">
    <br>
    
    - Change both from "false" to "true" to allow any app read and write at the database
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/rules2.png">
    <br>
    
    - Click on publish to finish
    
    - A security warning will show up, don't worry, our app will not be shared with many other users and only you, with the project id will be able to access it as long you not share the project id or config.

11. Now we ae ready to use it! 
    - Download the [gi_pulls.html](https://github.com/Matsukii/GI-pull-history/blob/main/gi_pulls.html)

    - open it with a text editor (Visual Studio Code,Notepad, Notepad++ ...) to edit
        - prefer notepad if you don't have a code editor, office like editors are not recommended.

    - Go to arround line 428 or this portion:
   
   <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/edit.png"><br>

    - Change the projectId from "<id>" to your project id that you copied OR paste the firebaseConfig that you copied before below "// OR PASTE FIREBASE..."
    
    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/idAdded.png"><br>

    - Save the file as .html

    - Open the file with a double click our dragging and drop to your browser

12. Done! you finished, now you can add, remove and logg yur whishes!

    <img src="https://raw.githubusercontent.com/Matsukii/GI-pull-history/main/screenshots/finish.png"><br>
    
    - Insert the type, stars, name and date and click on add to send to database
    
    - Click on "x" on any item to remove, a 'notificatio' to undo will show up for 10 seconds
    
    - Click on "date", "stars  type" or "name" to sort the table by added date, stars or name


*pulls since, total, and primogems used is calculated by the number of entries*


## Thanks for the interest and have a nice game :)


