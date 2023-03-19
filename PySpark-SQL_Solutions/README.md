
## Solving list of Questions in PYSPARK(SQL)

1. List of Winners of Each World champions Trophy Hint: Total Result of all rounds of Tournament for that player is considered as that player's
Score/Result. Result attributes: winner, tournament_name

![Screenshot (18)](https://user-images.githubusercontent.com/98254459/195666334-69a31b36-372e-45b2-ae33-4c5165c49aeb.png)

2. List of Players with number of times they have won Tournament in descending order(Max to min).
Result attributes: player_name, number_of_wins

![Screenshot (19)](https://user-images.githubusercontent.com/98254459/195666337-cfeacff5-b672-4ac0-8e14-47e8883cf592.png)

3. Most and Least Popular eco move in world championship history.
Result attributes: eco, eco_name, number_of_occurences Final result will have only two rows

![Screenshot (20)](https://user-images.githubusercontent.com/98254459/195666339-b813426d-ba07-4567-ad9b-4114d5c0294b.png)

4. Find the eco move with most winnings.
Ps. Use this opening move in your next chess game🙂 Result attributes: eco, eco_name

![Screenshot (21)](https://user-images.githubusercontent.com/98254459/195666342-54618411-f354-461f-aafa-c5a212ec8d66.png)

5. Longest and shortest game ever played in a world championship in terms of move.
Chess Funda: "move" is completed once both White and Black have played one turn. e.g If a game lasts 10 moves, both White and Black have played 10 moves)

Result attributes: game_id, event, tournament_name, number_of_moves Final result will have only two rows

![Screenshot (22)](https://user-images.githubusercontent.com/98254459/195666343-f143b7d4-f8c0-4c63-ba75-585e10a08b6f.png)

6. Shortest and Longest Draw game ever Played.
Result attributes: game_id, event, tournament_name, number_of_moves Final result will have only two rows

![Screenshot (23)](https://user-images.githubusercontent.com/98254459/195666346-51519d21-212a-4690-a0fc-604758b88e3c.png)

7. Most and Least rated Player.
Result attributes: player_name, elo Chess Funda: elo is the rating of the player in chess tournament. Final result will have only two rows

![Screenshot (24)](https://user-images.githubusercontent.com/98254459/195666347-a37748c1-79bb-4ec5-b3d7-95123cc70573.png)

8. 3rd Last Player with most Loss.
Result attributes: player_name Final result will have only one row

![Screenshot (25)](https://user-images.githubusercontent.com/98254459/195666351-2274f7f2-be82-490c-8bfa-dea0405046ce.png)

9. How many times players with low rating won matches with their total win Count.
Result attributes: player_name, win_count

![Screenshot (26)](https://user-images.githubusercontent.com/98254459/195666353-44859c03-b62e-44b7-9c5e-aa2a4b923906.png)

10. Move Sequence for Each Player in a Match.
Result attributes: game_id, player_name, move_sequence, move_count

![Screenshot (27)](https://user-images.githubusercontent.com/98254459/195666354-acf7b224-51b5-4208-a1fd-43febbcbd755.png)

11. Total Number of games where losing player has more Captured score than Winning player.
Hint: Captured score is cumulative, i.e., for 3rd capture it will have score for 1, 2, and 3rd. Result attributes: total_number_of_games Final result will have only one row

![Screenshot (28)](https://user-images.githubusercontent.com/98254459/195666357-f31b577c-e905-4f49-988a-fd2c4a0cd809.png)


## CONCLUTION

The above questions required proper level of understanding on the 3 tables that we got. being new to SQL lot of experience related to conditional Statements in SQL, joins, sub queries and also some complex WITH statements were learned and put to use. The most important part was all the questions were answred with the expectation set right. we also used union and we were in a situvation were OFFSET did not work and we used window function row_number() to solve the problem.