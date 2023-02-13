# dachshund_players_distributor

## Documentation, created by chatGPT:

This Python script reads data from a CSV file containing ice hockey match results and player statistics. It then calculates the average ratings for each player based on their weighted goals, where the weight is given based on the number of goals scored in a match and the overall score of the match. Finally, it assigns players to teams based on their ratings, allowing for the option to randomly swap some players before assigning them to teams.

The main functions in this script are:

**get_player_names_goals(player)**: Extracts the goals and name of a player from the input string in the format "Name(goals on the match)".

**save_weighted_goals(player_name,players_weighted_goals,player_weighted_goals)**: Saves the weighted goals for a player in a dictionary.

**save_match_nums(player_name,players_match_nums)**: Saves the number of matches played by a player in a dictionary.

**calculate_avg_ratings(players_weighted_goals,players_match_nums)**: Calculates the average rating for each player based on their weighted goals and the number of matches played.

**get_current_players_ratings(players_avg_ratings,is_here)**: Filters out players who are not present (according to is_here) and returns a dictionary with their current ratings.

**swap_players(sorted_current_players)**: Randomly swaps some players in the list of current players before assigning them to teams.

The script first reads in the CSV data using the csv module, storing it in result_lines. It then initializes dictionaries to keep track of the weighted goals and number of matches played for each player. It iterates through each match and roster, calling the appropriate functions to update these dictionaries.

It then calculates the average ratings for each player and filters out players who are not present using is_here. It sorts the remaining players by their rating and optionally swaps some players randomly. It finally assigns the players to teams based on their sorted ratings, allowing for the option to create three teams.

The output of the script is the list of players in each team, printed to the console.
