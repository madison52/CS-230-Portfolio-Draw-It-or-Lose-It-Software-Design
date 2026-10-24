# CS 230 Portfolio: Draw It or Lose It Software Design Document

This repository holds the software design document I wrote for The Gaming Room in CS 230 (`CS230_Software_Design_Document_Final.docx`). Below are my answers to the Module Eight journal questions.

## Who was the client, and what did they want?

The client was The Gaming Room, a company with an Android game called Draw It or Lose It. The game is loosely based on the TV show Win, Lose or Draw. Teams try to guess a puzzle from stock drawings that appear at a steady rate over four one minute rounds. The Gaming Room wanted a web based version that works on multiple platforms, and I worked on it as a technology consultant for Creative Technology Solutions.

Their software requirements were:

- A game has one or more teams, and each team has multiple players.
- Game and team names must be unique, so users can check whether a name is taken.
- Only one instance of the game service can exist in memory at a time, using unique identifiers for each game, team, and player.

## What did I do particularly well?

I kept the document clear and aimed at the client. The executive summary explains the problem and the solution in plain language, and each recommendation ties back to what the game actually needs, like steady image timing and many games running at once. I also explained the UML diagram in a way that someone who hasn't read the code could follow, showing how Entity, Game, Team, Player, and GameService fit together.

## What about the design document process helped when developing the code?

Working out the domain model first made the code easier to write. Once I saw Entity as the base class, it was obvious that id and name belong in one place and that Game, Team, and Player should inherit from it. The design also pointed me to the right patterns before I started coding: a singleton for GameService and an iterator to check for duplicate names before adding a game, team, or player.

## What one part would I revise, and how?

I'd revise the evaluation table. My answers are accurate, but they're general. I'd add real cost figures and clearer trade-offs for each platform. I'd also add a simple architecture diagram showing the clients, the server, the database, and the image storage, so a reader can see the whole system at a glance.

## How did I interpret the user's needs, and why does it matter?

I turned each requirement into a design decision. Unique names became iterator checks before anything gets added. Only one instance in memory became a singleton. Playing on many devices became a browser based client server design on Linux. I also thought about the players' experience, since images need to reveal at a steady rate, which led to my memory and caching recommendations.

Considering the user's needs matters because software that doesn't fit how people will use it gets built wrong, costs rework, and loses users.

## How did I approach designing the software, and what would I do in the future?

I started with the requirements, then the domain model, then the constraints, and finally the platform choices. For a similar project, I'd list the requirements and constraints first, sketch the UML early, choose patterns that match specific problems, and think through memory, storage, networking, and security before settling on a platform. I'd also build a small prototype to test my assumptions and ask the client questions early instead of guessing.
