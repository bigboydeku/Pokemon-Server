# Pokemon-Server: Created by Oliver Drowzdowski and Denis Nadarevic
We wanted to recreate the core of Pokémon battles utilizing TCP sockets in Java. Players will connect to a server and take turns attacking until a Pokémon has fainted. Players can also choose from a selection of Pokémon. By doing this we hope to get a greater understanding of how TCP sockets, threads, Java, states, and client-server-client communication functions on a fundamental level. Note that we are just implementing the battling portion, as the rest of the game would be a massive undertaking. 

A substantial amount of planning was needed to understand what type of battle and network systems we needed, how we would organize the database of Pokémon and more. This project idea was decided to challenge not only our understanding of TCP sockets but our ability to program a modern game that is popular to this day. The Java programming language was chosen since both members understand the language. This report will explain the main features, tools, and techniques implemented to perform properly.

To execute the code, the programs must be executed through the terminal on the UWindsor server. It is preferred that the server is executed first, along with the players. To play the game, have two players connect to the server by submitting their names. Once the server accepts the names, both players will be asked to pick a Pokémon to battle with. Once both players pick a Pokémon, one player will be randomly selected to start first. The players will be given a list of moves that they can use, with each move doing different amounts of damage. Players will take turns dealing damage to each other until a player’s Pokémon faints. When one Pokémon’s HP reaches zero, the game ends.

Please type the following terminal commands to try this out, this was made for SSH servers:
```
git clone https://github.com/bigboydeku/Pokemon-Server.git
cd "Pokemon-Server/src"
cp ../pokemon.db .
javac -cp '.:sqlite-jdbc-3.27.2.1.jar' Server.java
java -cp '.:sqlite-jdbc-3.27.2.1.jar' Server
```

Before executing the server, please read and run the [Pokemon Client](https://github.com/bigboydeku/Pokemon-Client) to have players from different networks play against each other.

The application was originally created using the IntelliJ IDE, but it was switched over to the University of Windsor server for the presentation. A problem that we faced, when switching over, involved the database. The server did not allow us to compile the files without a reference to the database. The commands above solve this problem; it requires additional steps, such as compiling and running with a reference to the database, as well as moving the database to the src file.
