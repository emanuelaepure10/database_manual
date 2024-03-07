# Requirements



Having a Player class - an instance of this class with that can communicate with other Player(s) (other instances of this class)

The use case for this task is as bellow:

1. create 2 players
2. one of the players should send a message to second player (let's call this player "initiator")
3. when a player receives a message should send back a new message that contains 
the received message concatenated with the message counter that this player sent.
4. finalize the program (gracefully) after the initiator sent 10 messages and received back 10 messages (stop condition)
5. both players should run in the same java process (strong requirement)
6. document for every class the responsibilities it has.
7. opposite to 5: have every player in a separate JAVA process (different PID).

Please use pure Java as much as possible (no additional frameworks like spring, etc.)

Everything what is not clearly specified is to be decided by developer. Everything what is specified is a hard requirement.

Please focus on design and not on technology, the technology should be the simplest possible that is achieving the target.

The focus of the exercise is to deliver the cleanest and clearest design that you can achieve (and the system has to be functional).


# Classes description
1-5 requirements

### App.java
The main class of the application. Creates the queue and the 2 players.

The BlockingQueue has been chosen to support the operations between the 2 players. As the requirements don't specify that when designing the
application should have in mind the extension of it to multiplayers, the BlockingQueue is the simplest solutions for 2 players.
The BlockingQueue wait for space to become available when adding an element and after retrieving and element also removes it and than
waits for an element to become available.

The class starts as well the threads for the 2 players. As the requirements is to have one process, and a thread is a so called lightweight process,
has been chosen because can access shared data of other threads in the same process.

### util/Constants.java
This class contains the value constants used by the application.

### player/Player.java
The class Player receives a message and send back the same message concatenating the counter of the sender.

The get the right counter an atomic operaion has been chosen. Benefits of using Concurrency classes for atomic operation is that we don’t 
need to worry about synchronization. This improves code readability and chance of errors are reduced. Also atomic operation concurrency classes 
are assumed to be more efficient that synchronization which involves locking resources.

### player/InitialPlayer.java
This class extend the Player class. The class initiate the messaging between the 2 players and all the rest is done in the Player class.

# Compile and run
Open cmd terminal and move into the main folder of the application 360T
To compile the code run:
```
 mvn clean install
```


To run the code run: 
```
 java -jar target/360T-1.0-SNAPSHOT.jar
```



# Results
```
[Initiator] player send message [Initial message].
[Initiator] player send message [Initial message 0 0].
[Player] player send message [Initial message 0].
[Initiator] player send message [Initial message 0 0 1].
[Player] player send message [Initial message 0 0 1 1].
[Initiator] player send message [Initial message 0 0 1 1 2].
[Player] player send message [Initial message 0 0 1 1 2 2].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3 4].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3 3 4 4].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6 7].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6 7 7].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6 7 7 8].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6 7 7 8 8].
[Initiator] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6 7 7 8 8 9].
[Player] player send message [Initial message 0 0 1 1 2 2 3 3 4 4 5 5 6 6 7 7 8 8 9 9].
Finalizing the app after 10 send-receive messages.
```

# Solution of a multi player messaging
The same task could be solved using 2 BlockingQueue for the 2 players and for a easier extension.

I, sincerely, would have chosen another solution, more complex, if the requirements would have specify that the program should be extended for multiplayers.

A Message/Event Bus and Listener would have been my preferred choice.
