# Project 1: Search in Pacman

In this project, your Pacman agent will find paths through his maze world, both to reach a particular location and to collect food efficiently. You will build general search algorithms and apply them to Pacman scenarios.

## Files edited:
<strong>search.py</strong> :	Where all search algorithms will reside.<br> 
<strong>searchAgents.py</strong> :	Where all of search-based agents will reside.

## Other Files:
<strong>pacman.py</strong>	: The main file that runs Pacman games. This file describes a Pacman GameState type, which you use in this project.<br>
<strong>game.py</strong>	: The logic behind how the Pacman world works. This file describes several supporting types like AgentState, Agent, Direction, and Grid.<br> 
<strong>util.py</strong>	: Useful data structures for implementing search algorithms.<br>
<strong>graphicsDisplay.py</strong>	: Graphics for Pacman <br>
<strong>graphicsUtils.py</strong>	: Support for Pacman graphics <br>
<strong>textDisplay.py</strong>	: ASCII graphics for Pacman <br>
<strong>ghostAgents.py</strong>	: Agents to control ghosts <br>
<strong>keyboardAgents.py</strong>	: Keyboard interfaces to control Pacman <br>
<strong>layout.py</strong>	: Code for reading layout files and storing their contents <br>


## Welcome to Pacman
After changing to the project1/ directory in your SVN repo, you should be able to play a game of Pacman by typing the following at the command line: <br>
python pacman.py 
<br><br>
Pacman lives in a shiny blue world of twisting corridors and tasty round treats. Navigating this world efficiently will be Pacman's first step in mastering his domain.<br>

The simplest agent in searchAgents.py is called the GoWestAgent, which always goes West (a trivial reflex agent). This agent can occasionally win:<br>
python pacman.py --layout testMaze --pacman GoWestAgent
<br><br>
But things get ugly for this agent when turning is required: <br>
python pacman.py --layout tinyMaze --pacman GoWestAgent
<br><br>
If pacman gets stuck, you can exit the game by typing CTRL-c into your terminal.
<br>
<br>
Soon, your agent will solve not only tinyMaze, but any maze you want.
<br><br>
Note that pacman.py supports a number of options that can each be expressed in a long way (e.g., --layout) or a short way (e.g., -l). You can see the list of all options and their default values via:
<br>
python pacman.py -h
<br><br>
Also, all of the commands that appear in this project also appear in commands.txt, for easy copying and pasting. In UNIX/OS X, you can even run all these commands in order with bash commands.txt.
<br>

## Objectiecs
First, test that the SearchAgent is working correctly by running:
<br>
python pacman.py -l tinyMaze -p SearchAgent -a fn=tinyMazeSearch
<br><br>
