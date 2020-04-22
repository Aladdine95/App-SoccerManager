# Football (Soccer Manager)

A full Java Swing football management game, built with Quitterie Pilon and Laura Fustinoni during my second year of a Computer Science degree at UCP (Université de Cergy-Pontoise).

## How it works

You pick a team out of five (France, Brazil, Germany, Tunisia, England — loaded from CSV, flags and all), set your tactics and starting eleven against the substitutes, then face off against a CPU-controlled opponent. The match runs round by round: each player's position updates through a simple vision-and-movement AI that tracks the ball and follows the chosen tactic, and at some point during the game one of five superpowers (Corruption, Dodge, ForceField, Magnet, SuperSpeed) gets randomly triggered on a player, shaking things up. The whole match plays out on a rendered pitch with a live chronometer and score, wrapping up on an end screen once the final whistle blows.

## Project structure

```
football/src/
├── gui/elements/     # MainMenu, KickOffMenu (team/tactics/roster), MatchScreen, GraphicalField, EndscreenPanel...
├── dataplayer/        # player positions and the five superpowers, sharing an abstract base
├── datafield/, databall/, datateam/   # pitch, ball and team data models
├── process/
│   ├── management/    # Match (the round-by-round engine), CreaTeam/RecupTeam, tactics & positioning
│   ├── movement/       # MovementPlayer / MovementBall / Vision
│   └── scores/          # chronometer and score tracking
├── ressources/         # team flags, ball/UI images, teams.csv, strategies.csv
└── test/                # JUnit suite + a CLI mode (CLIgame) for running matches without the GUI
```

## Stack

Java, Swing, JUnit.

## Status

Finished as a working, playable university group project in 2020 — pick a team, set your tactics, play a full match against the CPU with the superpower twist.
