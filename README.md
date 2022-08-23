# Chess-Skill-Classifier

### Motivation
I'm an amateur chess player, and I have always been fascinated by the way people of different skill levels approach the game.  Watching a great player make decisions over the board and comparing them to a weak player, it's often clear who has the upper hand.  A weak player may lose a piece while gaining nothing in return, while an excellent player rarely makes such a mistake.  The quality of decision making is the essence of what separates a great player from a weak player.  I had always assumed that the only way to gauge the quality of a player would be to watch them making one of these decisions, but after studying hundreds of games over the years, I noticed something interesting.  When I look at a picture from a famous game between two chess grandmasters, the pieces are arranged in a way that I would never find in one of my own games.  Modern professionals have well guarded positions and carefully crafted pawn structures, while my games look like a barfight, with pieces scattered everywhere.  At a glance, even an amateur like myself can tell the difference.  This realization inspired me to build a neural net to guess a player's skill based off a single board position.  

### Overview of approach and results
Here, using a neural net, we estimate the skill rating ([ELO score](https://en.wikipedia.org/wiki/Elo_rating_system)) of two players by examining an isolated board position, plucked without context from the middle of their game.  With a single board position, we can get surprisingly close to estimating the skill rating of two players, with 50% of our guesses being within 200 ELO points of the true value.  The classifeier performs best on lower skill rated players games, with 50% of ELO predictions for this group landing within 50-150 ELO points.

This repo contains what you need to classify chess games based off player skill.  Everything from acquiring your own dataset to training your own network is included.  However, if you're only interested in examining the results of my own analysis, codes for this step alone are included as well.

Using a neural network, we are able to establish the approximate skill level of players based off a single board position.



<br />
<br />

