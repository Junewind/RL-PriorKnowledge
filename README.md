Updates and how to use them:

1. Define a reward dictionary with the following keys: "positive", "negative", "tick", "loss", "win". Pass it to the PLE object under the argument reward_values. Negative, tick and positive keys checked and working.
2. Pass the path to the .txt map file as a string to the originalGame object like so : originalGame('/path/to/map.txt')
3. Pass the experiment name as a string to originalGame object like so: originalGame('/path/to/map.txt', 'fire')
options:
'fire' - Places the princess on the ground floor for fire experiments
'ladder' - Places the princess on the first floor for ladder experiments
None(default) - Places the princess on the "top" floor as seen in the original code.

# EXAMPLE USAGE

<code>

mapname = 'enemies.txt'
experiment = 'fire' # choose between ladder/fire/None

game = originalGame(mapname, experiment)

rewards = {
    "positive": 1.0,
    "negative": -1.0,
    "tick": 1.0,
    "loss": -5.0,
    "win": 5.0
}

p = PLE(game, fps=30, reward_values = rewards, display_screen=True, force_fps=True)

p.init()

</code>

New maps are under the following names:
fire_1.txt
fire_2.txt
fire_3.txt
ladder_1.txt
ladder_2.txt
fireandladder.txt
enemies.txt
