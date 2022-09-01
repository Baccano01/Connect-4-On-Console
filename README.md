<h1> Connect Four </h1>

<p> Author: Jofeth Abello</p>

<p>This project is about the vertical board game entitled Connect 4 or Four Up.
It lets two person to play Connect 4 on the console.</p> 

<p>The game is entirely written in Java 16. I used Java 16 to be able to use all the new API's available since Java 8, such as Lambda expressions and Generics in Java.</p>

<p>The purpose of this project is to learn to apply the concepts learned from the OOP paradigm,
such as Polymorphism, Abstraction, Encapsulation and Inheritance. Moreover to be able to use
the features of Java and be able to apply the SOLID Principle in software design.</p>

<p>In case you don't know what are the principal concepts of OOP, you can start with these
links: <a href = https://en.wikipedia.org/wiki/Object-oriented_programming> OOP Principles </a> and <a href = https://docs.oracle.com/javase/tutorial/java/concepts/index.html> Java OOP tutorials</a>.</p>

<h2><div id="table">Table of Contents</div></h2>
<ol>
<li><a href=#principles>SOLID Principles</a></li>
       <ol>
       <li><a href=#SRP>Single Responsibility Principle</a></li>
       <li><a href=#OCP>Open/Closed Principle</a></li>
       <li><a href=#LSP>Liskov Substitution Principle</a></li>
       <li><a href=#ISP>Interface Segregation Principle</a></li>
       <li><a href=#DIP>Dependency Inversion Principle</a></li>
       </ol>
<li><a href=#LEARNED>What I learned by doing this project</a></li> 
<li><a href=#Features>Game Features</a></li>
<li><a href=#use>How to use the Game</a></li>
       <ol>
       <li><a href=#run>Running the game</a></li>
              <ol>
              <li><a href=#jar>Jar file</a></li>
              <li><a href=#src>Main</a></li>
              </ol>
       <li><a href=#play>Playing a match</a></li>
       <li><a href=#pause>Pausing a match</a></li>
       <li><a href=#restart>Restarting a match</a></li>
       <li><a href=#save>Saving a match</a></li>
       <li><a href=#quit>Quiting a match</a></li>
       <li><a href=#prog>Normal match progression</a></li>
       <li><a href=#exit>Exit the Game</a></li>
       <li><a href=#load>Load a match</a></li>
       </ol>
<li><a href=#requirement>Game Requirements</a></li>
<li><a href=#license>License</a></li>
</ol>




<h2><div id="principles"> SOLID Principles </div> </h2><p><a href=#table>top</a></p>
<p>The SOLID Principles that I tried to apply in this projects are:</p>

<h3> <div id="SRP">Single Responsibility Principle </div> </h3><p><a href=#table>top</a></p>
<p>Single Responsibility Principle - states that classes or objects should have only one responsibility or one reason to change. It means that when creating a class, it should only have one job to do or one purpose. An example is when you want to create a class for printing the texts of the game, said class should be only be allowed to print texts and should only change when it regards to printing a text--in case the way to do the printing need to be changed--but not when--for example--the game may want to have the ability to be able to save a match. If a class needs to worry to do two or more things (unless its the client code) then other classes should be created for those surplus purposes. This promotes ease debugging and pluggability of objects
since if there is a bug, the bug can be easily traced, or the class that is responsible for something is easily replaceable when it is defective.</p>

<h3> <div id="OCP">Open/Closed Principle</div> </h3><p><a href=#table>top</a></p>
<p>Open/Closed Principle - states that a class should only be open to extension and closed to modification. It means that if you want to add some features to a class (the exception is when you need to fix some bugs) a class should only be extended but not modified to avoid creating more bugs and to not force other clients to implement the new extra features. This is why it is important and convenient to define interfaces or abstract classes (Abstraction), that provides all the necessary operations that represents the instances of a class, to be implemented/extended by concrete classes are used by the client. It improves the extensibility and the reusability of classes.</p>

<h3> <div id="LSP"> Liskov Substitution Principle </div> </h3><p><a href=#table>top</a></p>
<p>Liskov Substitution Principle - states that if class A is superclass of class B then objects of class B should be able to substitute objects of class A i.e. on parameters where objects of class A are expected, it should be possible to use objects of class B without altering the behaviour of the object that expected objects of class A. The substitutability of a superclass can be easily found when applying covariance return type to a method, i.e. the possibility to return a subclass object of the original class of the return type of a method. This substitutability can be obtained through Inheritance and Abstraction. Substitutability also implies that subclasses should follow the properties (constraints, invariants, purpose, exceptions, etc.) of the superclass and not only the behaviours it shows.</p>

<h3> <div id="ISP"> Interface Segregation Principle </div> </h3><p><a href=#table>top</a></p>
<p> Interface Segregation Principle - states that a general interface should be divided into smaller interfaces i.e. when creating an interface with more than one methods, the interface should be divided into smaller interfaces that contains, if possible, only one method. This makes the interfaces reusable since if a client wants to implement an interface because it has a particular method then it is not obligated to implemented the other unnecessary methods. This principle also promotes high coherence and loose coupling of components since the interfaces that are used are those that are really needed and the dependency of the client is limited only to the interfaces that it needs. </p>

<h3> <div id="DIP"> Dependency Inversion Principle </div> </h3><p><a href=#table>top</a></p>
<p> Dependency Inversion Principle - states that classes should depend on abstractions instead of concretions. For example if a client code wants the behaviours or properties of a class then it should not extend a concrete class but rather an abstract class possessing or interfaces that mandates such behaviours. It promotes loose coupling since some components of the program can be easily substituted by other objects that have inherited or implemented such abstractions making the program more fault tolerant, because it is possible to plug another implementation of the abstraction that the program depends on without breaking it, making it more maintainable.</p>

<h2> <div id="LEARNED"> What I learned by doing this project: </div> </h2><p><a href=#table>top</a></p>

<p>Creating this project help me understand the SOLID principles better and apply the concepts of OOP. In this project I used a lot of generics to make my hoping it would make my code more maintainable, since it helps the classes of my program to be less coupled. I found that applying generics can be complicated if the class that I want to be generic has to depend on other classes that are as well generic themselves, making the code lungher and more cumbersome and complicated than it really is. I also used some lambda expressions in the program to make some functionalities more concise, although I had the doubt that it would make my program less OOP coherent, after all lambda expressions come from functional programming, which I think are really useful, even if I found on some sites, debates between OOP purists and people that integrates some functional components to their programs.</p>

<p>I learned how to use Composition, as oppose to Inheritance for better code pluggability and maintainability. It makes the code less coupled, because I can easily substitute some behaviours of my classes by making the behaviours as inteface types on fields of the class. The class needs not to worry about these behaviours and so implementation are left to the implementing classes that have implemented this interface given behaviours as long as the behaviour is consistent to the behaviour that is expected, e.g. I want to save a match of the game, the <code>ConnectFourMatch</code> class is only interested that it is possible to preserve instances of itself for later use, since I made so that the save behaviour of the class is done by a component interface called <code>Saveable</code> the class <code>ConnectFourMatch</code> only needs to call the save method of the <code>Saveable</code> inside its definition, but the implementation is left to the <code>Saveable</code> component that was passed during instantiation. By doing as such the class can save instances of itself in different ways, but they are still semantically correct. Even if I knew the advantages of Composition I only used it sparingly, because the focus of this project is to use the main concepts of OOP, in particular the use Inheritance, which I used extensively with Abstraction when defining the classes that composed the game.

<p>I learned how to use ANSI ESCAPE CODES to add colours on String objects when printed on a console. I used it to colour the tokens of the players of the game to make it more nice and make the players distinguishable when playing a match and also to some parts of the game like the main menu. For more information about ANSI ESCAPE CODES you can start with <a href=https://en.wikipedia.org/wiki/ANSI_escape_code>ANSI CODE</a>.</p>

<p>I learned how to emulate extensibility of enums with the creation of an interface that must be implemented by the enums that I want to use. I applied it when creating the tokens of the players of the game so that I can potentially add more colours to the token that a player can choose when playing a match. The interface that I defined as such in this project is the <code>DroppableInVerticalBoardColouredToken</code> to make sure that tokens that are used in the game are droppable in a vertical board and are coloured.</p>

<p>Moreover, I learned to use generics, some with lambda expressions, like generic methods and generic classes to make my code more reusable and more compatible with implementations of an abstraction, making it more maintainable and less coupled with other classes. With lambda expressions and generics I created a lot of functional generic interfaces in my program to make them more readable and reusable. An example of this is the save method of the <code>Saveable</code> interface that is generic making it able to save not only a single <code>VerticalBoardMatch</code> object but also a <code>SaveMatches</code> that contains a group of <code> VerticalBoardMatch</code> objects. It enables the game to potentially save more than the matches themselves.I also learned how to serialize objects with a supporting file through simple serialization or through the GSONs API and serialization using byte arrays (without using a file for support). The serialization I ultimately used is the simple and direct without using GSON, because to serialize some classes of my program I needed to create type adapters which would make the development take longer and more complicated than it should really be, more so I didn't need to convert objects into JSON representation. I also used serialization to create deep copies of <code>ConnectFourMatch</code> objects when saving and loading them from a <code>SavedMatches</code> object--that serves as a little database using <code>AbstractMap</code>--to not affect the states of the matches if I want to continue playing the match.</p>

<h2> <div id="Features"> Game Features:</div> </h2><p><a href=#table>top</a></p>
<p>1. Play a Connect 4 match between two players.</p>
<p>2. Players possess coloured tokens or pieces that can be drop in the columns of a vertical board when displayed on the console.</p>
<p>3. The ability to load saved matches and have the information about their creation (players name, winner, date of creation).</p>
<p>4. The ability to save matches of the game.</p>
<p>5. The ability to override saved matches.</p>
<p>6. The ability to delete a saved match of the game.</p>
<p>7. The ability to pause a match of the game.</p>
<p>8. The ability to restart a match.</p>
<p>9. The ability to resume a paused match.</p>
<p>10. The ability to quit the match.
<p>11. The ability to cancel some operations regarding the matches.</p>
<p>12. The ability to serialize the saved matches of the game when exiting the game.</p>
<p>13. The ability of matches to end in a draw.</p>

<h2><div id="use">How to use the game:</div></h2><p><a href=#table>top</a></p>

<h3><div id="run">RUNNING THE GAME</div></h3>
<h4><div id="jar">--From the <code>Connect Four.jar</code> file:</div></h4>

<p>If you're using Windows 10 or above, to make sure that ANSI escape codes are activated, since Windows 10 do support
ANSI CODES, but are turned off by default, on PowerShell go to the directory where you have the <code>Connect Four.jar</code> file (use <code>cd</code> pathofdirectory) and type <code>java -jar "Connect Four.jar" | Out-Host</code>--the name of the jar file is between double quotes-- since there is a space in the file name. For more information about the activation of the ANSI ESCAPE CODES you can refer <a href=https://stackoverflow.com/questions/51680709/colored-text-output-in-powershell-console-using-ansi-vt100-codes>here</a>.</p>

<h4><div id="src">--From the <code>connecfour/src/App.java</code> file:</div></h4>

<p>To activate an instance of this class it is necessary to call<code> run()</code> method.
If during the instantiation of this class the file path where to serialize the matches is not passed
then the default file<code> savedMatches.ser</code> inside the current working directory (directory where the JVM was called)
will be used as a serialization and deserialization target for the saved matches of the game. If the file doesn't exist then a new file with the same path will be created. Otherwise if a file path is specified then said file would be searched to check if it exists, else a new file is created. The file must be unhidden. If the file exists and is not empty, then the<code> S extends SavedStates<String, V></code> object that would be used is the one that was deserialized when running the game from said file, instead of the object passed during instantiation. If you would like to use the one that is passed during the instantiation, then you would also need to provide the file where to serialize the saved matches or make sure that the default file is empty during instantiation of this class.</p>

A main menu screen will be displayed to the players with this format:
<pre>
__        __   _                            _           ____                            _     _  _    _   _   _ 
\ \      / /__| | ___ ___  _ __ ___   ___  | |_ ___    / ___|___  _ __  _ __   ___  ___| |_  | || |  | | | | | |
 \ \ /\ / / _ \ |/ __/ _ \| '_ ` _ \ / _ \ | __/ _ \  | |   / _ \| '_ \| '_ \ / _ \/ __| __| | || |_ | | | | | |
  \ V  V /  __/ | (_| (_) | | | | | |  __/ | || (_) | | |__| (_) | | | | | | |  __/ (__| |_  |__   _||_| |_| |_|
   \_/\_/ \___|_|\___\___/|_| |_| |_|\___|  \__\___/   \____\___/|_| |_|_| |_|\___|\___|\__|    |_|  (_) (_) (_)
----------------------------------------------------------------------------------------------------------------
                                                
                                                -> 1. Play a 2 players match

                                                -> 2. Load a match

                                                -> 3. Exit game

----------------------------------------------------------------------------------------------------------------
Please choose a whole number [1 - 3]:</pre>

<h3><div id="play">PLAYING A MATCH</div></h3><p><a href=#table>top</a></p>
The main menu shows you the possible options you can do when starting the game. The first option lets you 
play with another player a connect 4 match. After pressing 1, the players are asked to put their names and 
then select their token.</p>

<p>-The names of the players (or any kind of name that is requested) must atleast contain a non-digit 
character to be accepted. In particular name inputs must not be <code>double</code> nor <code>long</code>. The name
of the second player would be added with a suffix of "-second" if it entered the same name as the first player.</p>

<p>-The tokens that can be selected are enums that implement the <code>DroppableInVerticalBoardColouredToken</code> interface, an example of an enum class of this interface is the <code>PrimaryColouredToken</code> that 
gives you <code>RED</code>, <code>BLUE</code> and <code>YELLOW</code> as choices. When dropping this tokens in the vertical board, 
during a match, you will see <code>R</code>, <code>B</code> or <code>Y</code> with their respective colours; for more info please see 
<code>PrimaryColouredToken</code> for the implementation. During the process of choosing a token, each token is associated 
with a whole number.  The player must simply insert the number to choose a token. If the number choosen is out of the 
range or is invalid then an appropriate message will be printed and the game will continue asking the player to choose
a valid token, players must not have the same token, otherwise a player will need to choose another token. To
know more about the tokens please refer to <code> DroppableInVerticalBoardColouredToken</code> and <code> PrimaryColouredToken</code>.</p>

<p>After choosing the tokens of the players, a board is presented and the first player gets the first turn to insert 
a token. Instead of dropping a token a player can also choose to pause the game.</p> 

<h3><div id="pause">PAUSING A MATCH</div></h3><p><a href=#table>top</a></p>
<p>Pausing the match will make the match menu pop to the screen through which players can resume, restart, save or quit the match.
The match menu would be like this:</p>

<pre>--------Match Menu--------

-> 1. Resume match 

-> 2. Restart match

-> 3. Save match

-> 4. Quit match

--------------------------</pre>

<p>To pause the match a player during its turn must press -1 and then the match menu will pop out.
The turns of the players is not affected when pausing the match. If an invalid input is inserted then
an appropriate message will be shown and the players will be asked to insert a valid input.</p>

<h3><div id="restart">RESTARTING A MATCH</div></h3><p><a href=#table>top</a></p>
<p>Restarting the match will clear the board, therefore previously inserted tokens would be removed
and the turns between the players would return to the initial turn and the match would resume.
The implementation of this option is handled by the <code>VerticalBoardMatch</code> object that represents a match.</p>

<h3><div id="save">SAVING A MATCH</div></h3><p><a href=#table>top</a></p>
<p>Saving the match would put it into a<code> S extends SavedStates<String, V></code> object associated with a<code> String</code> key or identifier. When saving a match the saved matches that were saved inside the<code> S</code> object are serialized together by serializing said object on a file. The default file where the matches are serialized is called<code> savedMatches.ser</code>, it is located in the directory where the software (files of the whole project) is located. Otherwise<code> SavedStates</code> object is serialized into the file specified by the filename during the instatiation of an object of this class. To know more about game states serialization refer to <code> ObjectSerializerAndDeserializer</code> and <code>link SavedStates</code>. During the saving process the player needs to insert a name of the match or the key to associate the match with. The success of the save depends if the same key has already been associated with another match--if it is the case then the player will be asked to overwrite the previously saved match inside the<code> S</code> object, by replacing it with the current match, otherwise the player will need to provide another name that is not already taken or the player can just cancel saving
the current match--if not then the match would be saved successfully in the<code> S</code> object passed as an argument during the instantiation of an instance of this class. The<code> V</code> match object that would be saved effectively would be a deep copy of the original match depending on the implementation of the<code> S</code> passed during instantiation (This is particularly true if the<code> S</code> object is an instance of<code> SavedMatches</code>).</p>

<h3><div id="quit">QUITTING A MATCH</div></h3><p><a href=#table>top</a></p>
<p>Quitting the match would make the game run in an idle like state during which a player needs to press a key to continue
and return to the main menu.</p>

<h3><div id="prog">NORMAL MATCH PROGRESSION</div></h3><p><a href=#table>top</a></p>
<p>An example of playing the current match (on the console some parts may have colours
and are indented by 10):</p>
<pre>
       Jamie <YELLOW> vs Frank <RED>

        [ 0 ] [ 1 ] [ 2 ] [ 3 ] [ 4 ] [ 5 ] [ 6 ]
       |  -  |  -  |  -  |  -  |  -  |  -  |  -  |
       |  -  |  -  |  -  |  -  |  -  |  -  |  -  |
       |  -  |  -  |  -  |  -  |  -  |  -  |  -  |
       |  -  |  -  |  R  |  -  |  -  |  -  |  -  |
       |  -  |  Y  |  Y  |  -  |  -  |  -  |  -  |
       |  Y  |  R  |  R  |  -  |  -  |  -  |  -  |
       ===========================================

Frank's turn:
Press -1 to pause.
-> Please enter a whole number between [0 - 6]: 
</pre>

<p>If a match progresses normally then the players will need to drop a token on his/her turn until one of them manages
to connect atleast 4 of their own tokens, but if they fail to do so the match would end in a stalemate or draw (if the 
board gets completely full and neither sides managed to connect 4 of their tokens). Please see <code> Checker</code>
<code> ConnectBoardGameWinnerChecker</code> for more information.</p>

<h3><div id="exit">EXITING THE GAME</div></h3><p><a href=#table>top</a></p>
<p>Exiting the game causes the termination of the current JVM. When a player chooses to exit the game, the game will ask first for a confirmation, during which the player must enter an input for confirmation or cancellation.</p>

<h3><div id="load">LOADING A MATCH</div></h3><p><a href=#table>top</a></p>
<p>The saved matches of the players that are saved in a <code>S</code> object can be loaded and be played through the main menu by pressing 2. The player is presented with a list of saved matches associated with their names and then the player needs to select one of them by typing down the name of the match. The player can also cancel loading a match. If there are no saved matches then a message would pop up to the players to let them know that that the <code>S</code> object is empty. During the loading process a player can also delete a saved match. Whether a loaded match is a copy of the original match from the <code>S</code> object depends on the implementation of the <code>S</code> object. It also applies when saving a match of the game.</p>

<p>The visualization of the interfaces and the prompts and messages and the objects of the game is handled by a 
<code>GameVisualizer<?></code> instance. The parser of the inputs is an object of <code>InputParser<Scanner></code> although
the process of the parsing and the handling of the inputs is handled by this class.</p>

<h2><div id="requirements">Requirements:</div></h2><p><a href=#table>top</a></p>
<p>The program needs the <code>savedMatches.ser</code>--the file doesn't necessarily need to have an extension of <code>.ser</code> it can just be simply a <code>.txt</code> file-- as a default file (although you can change it) to be able to serialize the saved states, or rather the matches of the game and then deserialize them after instantiating an object of the <code>ConnectFour</code> class that represents the game as a whole. If you delete this file or any other file that you specified during instantiation then the saved data of the serialized <code>SavedState</code> or <code>SavedMatches</code> will be lost. If you want to clear the data then you can just delete this file (you can also use the delete functionality of the game when trying to load a saved match) and when instantiating an object from <code>ConnectFour</code>, another file of the same name as the file specified in the constructor parameter will be automatically created. The file <code>savedMatches.ser</code> is the default file where to serialize matches of the game. It is found inside directory of the project.</p>
