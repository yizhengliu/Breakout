# COMP2013 Developing Maintainable Software - Breakout

<br>Name:YizhengLiu</br>

<br>Student_ID:20291679</br>

<br>Email:psyyl10@nottingham.ac.uk</br>

##To run the application

In order to run this application,
you first need to install a valid Java 17 version,
and set <code>JAVA_HOME</code> after that.
You then need to decompress the zip file,
then open the terminal and go to the directory
called <code>BreakoutJavaFX</code>.The project is managed by gradle
,so you only need to type <code>./gradlew run</code> to run the application.(For java version/swing one, you need to download from branch from gitlab called "Final_Java_Version",decompress it and use the same way to start the game)

##Javadoc file directory

In COMP2013LiuYizheng directory there is a file called javadoc, all javadocs are in that file.

##List of features that are implemented and are working properly

<ul>
    <li> An item (blue circle)that would make the ball become slow for 5 seconds </li>
    <li> Background music(free online) for the game that can be stopped or replayed using the check box in the menu</li>
    <li> Menu bar that contains quit, show help dialog and show high score list functions</li>
    <li> A permanent high score list</li>
    <li> A start screen with theme color chooser, quit button and start game button</li>
    <li> Images for ball, bricks and paddle</li>
    <li> Playable levels set upon to 6 levels and the last level will keep repeat if bricks in last level are all destroyed</li>
    <li> Scores and time show on the center of the screen</li>
    <li> Level chooser in the menu, player can choose which level they want to play</li>
    <li> After each level finished a score pop up will appear</li>
    <li> When game over a text input dialog for high score list will appear</li>
</ul>

##List of features that are implemented and are not working properly

<ul>
    <li> The ball may stuck in the paddle</li>
    <li> Bricks may be destroyed very quickly due to the collision operation</li>
</ul>

##A list of new java classes

<ul>
    <li> All classes in FXversion package:game implementation in Javafx, however it's similar to Javaversion one</li>
    <li> Constants: introduce all symbolic constants used in the game</li>
    <li> Score_list: read and write a high score list of the game, use singleton pattern to avoid read/write conflict</li>
    <li> StartMenuController: holds input from the user at the start screen</li>
    <li> BrickFactory: Factory pattern that will be used to generate types of bricks</li>
    <li> All classes in Controller package(Javaversion package): listening every possible input from player, send changes to models to process data and give feedback to view to upload changes for user</li>
    <li> All classes in Views package apart from the ones mentioned in modified code part(Javaversion package) : updates the game on to user's screen</li>
    <li> All classes in Models package(Javaversion package): called by controller, to process any data that the game(view updating) requires</li>
</ul>

##A list of java classes that I modified from the code base

<ul>
    <li>Basically the Javaversion package is where I refactored the original code, especially the classes in the MVC package that is where I split the responsibility of each classes</li>
    <li>GameBoard,GameFrame,StartGame,DebugConsole,DebugPanel classes into MVC pattern</li>
    <li>Wall: split the wall class into game view (GameBoard)and modify the original
    class only for generate a wall that contains bricks and information of those bricks</li>
    <li> Brick: split the inner class called Crack to other class to assign single responsibility</li>
    <li> most classes has been changed name, for example, the ball1 is renamed to RubberBall, make it more clear the relation of 
classes</li>
    <li> GameFrame class and some MVC classes are also been modified because new features are firstly implemented in 
    the Javaversion one, you can check the branch "Final_Java_Version" on the gitlab of the changes, git comments has stated them clearly</li>
</ul>