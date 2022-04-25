# Starter code - OpenClassrooms WPS | P3

This repository contains the work that has been done so far on the chess tournament program.

### Data files

There are data files provided:
- JSON files for the chess clubs of Springfield and Cornville
- JSON files for two tournaments: one completed, and one in progress

### Models

This package contains the models already defined by the application:
* `Player` is a class that represents a chess player
* `Club` is a class that represents a chess club (including `Player`s)
* `ClubManager` is a manager class that allows to manage all clubs (and create new ones)

### Screens

This package contains classes that are used by the application to display information from the models on the screen.
Each screen returns a Command instance (= the action to be carried on).

### Commands

This package contains "commands" - instances of classes that are used to perform operations from the program.
Commands follow a *template pattern*. They **must** define the `execute` method.
When executed, a command returns a context.

### Main application

The main application is controlled by `manage_clubs.py`. Based on the current Context instance, it instantiates the screens and run them. The command returned by the screen is then executed to obtain the next context.

The main application is an infinite loop and stops when a context has the attribute `run` set to False.
