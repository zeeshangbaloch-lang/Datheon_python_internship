# Datheon Python Internship

This repository contains my completed tasks for the Datheon Python Internship.

**Author:** Muhammad Zeeshan

## Completed Tasks

|Task|Project|Folder|Status|
|-|-|-|-|
|1|Hangman Word Guessing Game (Console)|`Task1\_Hangman/`|Done|

\---

## Task 1: Hangman Word Guessing Game (Console)

A terminal-based Hangman game written in Python 3. The player guesses a hidden word one letter at a time and loses after 6 wrong guesses.

### Features

* Random secret word chosen with `random.choice()`
* ASCII gallows art that updates after every wrong guess
* Word shown as blanks that fill in as you guess (e.g. `p \_ \_ h o \_`)
* Shows all wrong letters guessed so far
* Repeated letters are ignored with a message, with **no penalty**
* Input validation (only a single letter a-z is accepted)
* Clear victory and game-over screens that reveal the word

### Requirements

* Python 3.8 or newer
* No extra libraries needed (uses only the standard library: `random`)

### Installation

1. Clone this repository:

```
   git clone https://github.com/zeeshangbaloch-lang/Datheon\_Python\_Internship.git
   ```

2. Go into the project folder:

```
   cd Datheon\_Python\_Internship/Task1\_Hangman
   ```

### How to Run

```
python hangman.py
```

On some systems use `python3 hangman.py` instead.

### How to Play

1. The game shows the gallows and a row of blanks, one for each letter.
2. Type one letter and press Enter.
3. A correct letter is revealed in every place it appears.
4. A wrong letter adds a part to the hangman. You can make 6 wrong guesses.
5. Guess the whole word before the drawing is complete to win.

### Project Structure

```
Datheon\_Python\_Internship/
├── README.md
└── Task1\_Hangman/
    └── hangman.py
```

### Code Overview

|Part|What it does|
|-|-|
|`secret`|List of possible secret words|
|`STAGES`|List of 7 ASCII drawings (0 to 6 mistakes)|
|`show\_game()`|Prints the gallows, the masked word, wrong letters and tries left|
|`play()`|Runs one full game: input, validation, win/lose checks|

Key design choices:

* A `set` called `guessed` stores every letter tried, so a repeated letter is detected before any penalty is applied.
* The mistake count is used as the index into `STAGES`, so the correct picture is shown without long `if/else` chains.

### Example Output

```
      +---+
      |   |
      O   |
      |   |
          |
          |
    =========

Word: \_ a \_ \_ \_ \_
Wrong letters: x z
Tries left: 4
```

## Author

Muhammad Zeeshan

