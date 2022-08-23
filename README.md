# Chess-Skill-Classifier
## Description
Train a neural network to guess the skill rating of chess players using only a snapshot of their game.  This repo includes the data used to train the model, as well as an analysis of the results of the project.

### Motivation
I'm an amateur chess player, and I have always been fascinated by the way people of different skill levels approach the game.  Watching a great player make decisions over the board and comparing them to a weak player, it's often clear who has the upper hand.  A weak player may lose a piece while gaining nothing in return, while an excellent player rarely makes such a mistake.  The quality of decision making is the essence of what separates a great player from a weak player.  I had always assumed that the only way to gauge the quality of a player would be to watch them making one of these decisions, but after studying hundreds of games over the years, I noticed something interesting.  When I look at a picture from a famous game between two chess grandmasters, the pieces are arranged in a way that I would never find in one of my own games.  Modern professionals have well guarded positions and carefully crafted pawn structures, while my games look like a barfight, with pieces scattered everywhere.  At a glance, even an amateur like myself can tell the difference.  This realization inspired me to build a neural net to guess a player's skill based off a single board position.  

### Overview of approach and results
Here, using a neural net, we estimate the skill rating ([ELO score](https://en.wikipedia.org/wiki/Elo_rating_system)) of two players by examining an isolated board position, plucked without context from the middle of their game.  With a single board position, we can get surprisingly close to estimating the skill rating of two players, with 50% of our guesses being within 200 ELO points of the true value.  The classifeier performs best on lower skill rated players games, with 50% of ELO predictions for this group landing within 50-150 ELO points.

This repo contains what you need to classify chess games based off player skill.  Everything from acquiring your own dataset to training your own network is included.  However, if you're only interested in examining the results of my own analysis, codes for this step alone are included as well.

Using a neural network, we are able to establish the approximate skill level of players based off a single board position.

### How to use the code in this repo

If you only want to explore the construction of the neural net and the results of the model, check out "Neural Net Classifier" and "Test Model on Data."  These contain everything you need to train your own model on the data I've collected, and explore the results.
<br \>
If you want to acquire your own dataset, head to the [Free Internet Chess Server](https://www.ficsgames.org/) and download games using their search tool.  For this project, I only used games in which both players were within 200 ELO of one another.  I also took care to ensure that an equal number of games were drawn from all ELO brackets.  Once you've downloaded your dataset, you can use "Extract PGN Data to CSV" and "Format CSV data for Neural Net" respectively to construct data ready to be used by the included neural net.
<br \>
The data I used to build this model is contained within the Data folder, while the test data is in the "Test Data" folder.  A curated set of test data (one which draws from high and low ELO games equally) is found in the "Test Data" folder as well.  Though you can download any given group of games from this site, in order to accurately gauge the quality of the classifier you should attempt to gather an equal number of games from each ELO bracket.
<br \>
