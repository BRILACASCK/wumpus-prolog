# The Wumpus World in Prolog
The Wumpus world problem deals with an AI robot navigating its way through a 4x4 puzzle to try and find gold. The robot must safely navigate its way around bottomless pits of death and evil Wumpus creatures to locate the gold hidden on the board. After it has successfully found the gold, it must safely navigate its way back to the starting point. The robot must use its light sensors and the signals sent to it at each square to determine which way to properly navigate to reach its goal.

However, we change the dynamic of the world a little bit. The world is rectangular grid which is in the close space and which has width x length number of rooms. there is an exits in some of these rooms which is guarded and the only way for the agent to use these exit is to answer a question about the world to the gaurd, otherwise he will lost the game. The goal of the agent is to go to outside using one of these exits. There is a flashlight or a light bulb in some of the rooms and agent can not enter any room that there is no light in it (whether by turning on the light bulb or by holding the flash light in his hand).The agent also has some energy (power) which is going to be consume after each step that he will take and this energy consumption is related to wheather his hand is empty or not,But there is food in some rooms which agent can eat to increase his energy.For making the world harder for the agent,there is a giant in some of the rooms and the agent can only defeat the giant when he has a weapon. The sound of giant shout can be heard from adjacent rooms so when the agent will hear the shout, it means that there is giant in one of the adjadcent rooms. Here is a picture of the world : 

![wumpus](http://i63.tinypic.com/9tenvd.jpg)

This code is implemented in prolog. [Prolog](https://en.wikipedia.org/wiki/Prolog) is a general-purpose logic programming language associated with artificial intelligence and computational linguistics. There are many different versions of prolog but the one that we used is [swi-prolog](http://www.swi-prolog.org/).

## Dependency
SWI-Prolog is available in diffrent platforms. you could find and download the version that you want from [here](http://www.swi-prolog.org/download/stable).

but for ubuntu you can use the PPA as follow:

```
sudo add-apt-repository ppa:swi-prolog/stable
sudo apt-get update
sudo apt-get install swi-prolog
```
and for executing the code. Open a terminal and change the current directory t0 the directory in which there are is the source file (the code also needs the data.db file for configuration). Then run the swipl command to start SWI-Proglog and then for compiling and running the code you should enter the following : 

```
['wumpus.pl'].
start.
```


