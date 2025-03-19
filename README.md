# AdaptivePokerAI
Adaptive Poker AI project for CS 4701

To create a poker bot, refer to the instructions for how to extend the PyPokerEngine BasePokerPlayer class: https://github.com/ishikota/PyPokerEngine

After creating a poker bot, one may again follow the instructions for simulating a game between AI players: https://github.com/ishikota/PyPokerEngine.

Alternatively, playing as a human player against a bot is possible: https://github.com/ishikota/PyPokerGUI.

The dependencies for this project are pypokerengine version 1.0.1, pypokergui version 0.0.7, and backports.ssl_match_hostname version 3.7.0.1. The first
two dependencies are the latest versions of PyPokerEngine and PyPokerGUI, and the latter dependency is used to patch an issue in PyPokerGUI where an import
is unrecognized by the latest Python Interpreter. In addition, pypokergui/server/templates/round_state.html is a template with a bug that tries to slice a list
using a float, which is not valid syntax, so the template is patched by using integer division (//) instead.

Shortcut to test GUI: `pypokergui serve {path to yml file inside tests/GUI} --port 8000 --speed moderate`

Codebase structure:
```AdaptivePokerAI/
│
├── src/
│   ├── players/
│   │   └── calling_station_player.py
│   └── ...
│
├── tests/
│   ├── gui
│       └── two_calling_station_players_test.yaml
│
├── data/
│   └── ...
│
├── README.md
└── requirements.txt
```
