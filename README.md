# ATP-Tennis-Analysis
The dataset prepared by Jeff Sackmann contains information on every single match played since 1968. In this project the data that will be used is starting from 2000.
Data is an important part of the sports industry for players, coaches, management, sports medicine workers and fans. Not only can data analytics help teams win games, these statistics can also help improve player performance. 
The main idea for the project is to think of how can I help the player to increase his chances to win a game. 
This will be done bt the following steps :
# EDA 
- For exploring the attributes for the top ranked players and what is special about them. Is there any common attributes ? 
# clustering 
- Does the top ranked players are cluster in one group and mid rank in one group..
- Grouping the players can help to form a strategy for the game, understand the playing style for the opponent 
- use it to improve the result of the prediction
# Prediction
- Now the player knows his opponent and have a plan for the game. The next step will be trying to predict the result of the game.
- For the classification : Logistic Reg., SVM classification, Random forest 
one important note here is that usually the information I used for this classification are generated after the end of the match so there is no real life effect of the mofe however by regression we can do live prediction for the match.
- For regression (can we predict the other sets results based on the first set stats ?) : Linear, SVM, Random forest.

possible future work

# Game simulation
 The value for the players can be shown as :
- Match strategy, tactics, and analysis 
- Training regimens and focus
- Match outcome and tournament table prediction

A successful outcome for the
project would be the creation of both a classification model capable of predicting a
future game’s outcome, and a regression model capable of predicting a future game’s
score.


### Get the data here
The data comes from [ATP-Tennis Data Set](https://github.com/JeffSackmann/tennis_atp). 

### Data Dictionary
Note that if the Attribute start with l this means that the field is for the loser and w is for the winner 
| Attribute      | Description                                                                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tourney_id     | - a unique identifier for each tournament, such as 2020-888. The exact formats are borrowed from several different sources, so while the first four characters are always the year, the rest of the ID doesn't follow a predictable structure.               |
| tourney_name   | Tournament name                                                                                                                                                                                                                                              |
| surface        | Hard, clay, grass..                                                                                                                                                                                                                                          |
| draw_size      | - number of players in the draw, often rounded up to the nearest power of 2. (For instance, a tournament with 28 players may be shown as 32.)                                                                                                                |
| tourney_level  | - For men: 'G' = Grand Slams, 'M' = Masters 1000s, 'A' = other tour-level events, 'C' = Challengers, 'S' = Satellites/ITFs, 'F' = Tour finals and other season-ending events, and 'D' = Davis Cup                                                            |
| tourney_date   | - eight digits, YYYYMMDD, usually the Monday of the tournament week.                                                                                                                                                                                         |
| match_num      | - a match-specific identifier. Often starting from 1, sometimes counting down from 300, and sometimes arbitrary.                                                                                                                                             |
| winner_id      | - the player_id used in this repo for the winner of the match                                                                                                                                                                                                |
| winner_name    |                                                                                                                                                                                                                                                              |
| winner_hand    | - R = right, L = left, U = unknown. For ambidextrous players, this is their serving hand.                                                                                                                                                                    |
| winner_ht      | - height in centimeters, where available                                                                                                                                                                                                                     |
| winner_age     | - age, in years, as of the tourney_date                                                                                                                                                                                                                      |
|          score | the match score                                                                                                                                                                                                                                              |
| best_of        | - '3' or '5', indicating the the number of sets for this match                                                                                                                                                                                               |
| minutes        | - match length, where available                                                                                                                                                                                                                              |
| w_ace          | - winner's number of aces                                                                                                                                                                                                                                    |
| w_df           | - winner's number of doubles faults                                                                                                                                                                                                                          |
| w_svpt         | - winner's number of serve points                                                                                                                                                                                                                            |
| w_1stIn        | - winner's number of first serves made                                                                                                                                                                                                                       |
| w_1stWon       | - winner's number of first-serve points won                                                                                                                                                                                                                  |
| w_2ndWon       | - winner's number of second-serve points won                                                                                                                                                                                                                 |
| w_SvGms        | - winner's number of serve games                                                                                                                                                                                                                             |
| w_bpSaved      | - winner's number of break points saved                                                                                                                                                                                                                      |
| w_bpFaced      | - winner's number of break points faced                                                                                                                                                                                                                      |
|  w_unforced_fh |  an unforced error is defined as an error that was not forced by your opponent, putting you into a difficult situation  fh is tennis forehand is a stroke in which the inner side of the palm of the dominant hand that is holding the racket faces forward. |
|  w_unforced_bh | bh backhand is a tennis shot in which one swings the racket around one's body with the back of the hand preceding the palm.                                                                                                                                  |
|   w_winners_fh | a winner occurs when a player is unable to touch the ball with their racquet before it bounces twice during a match for the forehand                                                                                                                                     |
|   w_winners_bh | a winner occurs when a player is unable to touch the ball with their racquet before it bounces twice during a match for the backhand                                                                                                                                        |
|   return_depth | how did the player hit the ball back to reduce the odds of your opponent being able to hit                                                                                                                                                                   |
| shot_Direction | Where did the shot exactly land on the tennis field                                                                                                                                                                                                          |
