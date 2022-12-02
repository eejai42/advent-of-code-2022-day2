
# Rock Paper Scissors

**NOTE:** This readme is DERIVED from the knowledge graph defined here:
        https://airtable.com/appsl1IuS9feiUMfF/tblvNX7NFoldBUYox/viwti0QueGt41e9Ec?blocks=hide

You may find this JSON version of rules helpful - 
**Knowledge Graph JSON**: [SSoT/Day02.json](SSoT/Day02.json).

The Elves begin to set up camp on the beach. To decide whose tent gets to be closest to the snack storage, a giant Rock Paper Scissors tournament is already in progress.

Rock Paper Scissors is a game between two players. Each game contains many rounds; in each round, the players each simultaneously choose one of Rock, Paper, or Scissors using a hand shape. Then, a winner for that round is selected: 

Rock defeats Scissors

<img src="https://v5.airtableusercontent.com/v1/11/11/1670011200000/vDNIbVnCenipc2UTQksDiw/SXm6r3CZ94_kfwlf-jAY_r8QfDGTqDJPjQZvxJuBTMP0SP8yp622CiwSL-f8cIZSTq5sIOHdcBjQVNaI3vg0kBUdYDLo-WUUS3ZieuqjTiHNcPaeRJIwlMp8nqzW0Z9oEApjWNCPG1B7r1tPJ0kKDOXzt31yYR2NMJSteMqAypg/AyUW9K2Y4fpzKsX8v706i81N_ZLxnX9jSgO-Ti-ZA-U" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/11/11/1670011200000/a4jQfHX4Bt7R3Ct0DsdSiQ/50uSd_MSwsY5EoDUgpz-pLMMlDL3dNI7mwkYwJJ_LjUrnhkef19fbQW5kE7ERIaD7hpaZaJjp6QzkK6JbsrejvY0kVkvPl2ORL7ZWIvFUitQjFDBPDYMgc8Niui9kteoWE8ghnWSNah0ByL3A8509yreCEdImDVqyU8wz6_0lzQ/EleuLtghM8A57UA6U4SCXK66votMJOeNwNOrel72C-I" style="width: 5em;" />

Paper defeats Rock

<img src="https://v5.airtableusercontent.com/v1/11/11/1670011200000/u7UPng61e-J5zuJftLTPoQ/lfv21wpko9JLcsKI-hYLe9G41zBv7d-rNOUQ8GMKYKy3H5WkZlbMpbmHOecSgHEhdQsONBSe5nkI-dBiJG4W747LDh9eHdjE94id3kULNNvJ3Gvfkpw3n179-lLH1GiwpWC90Gh9yAy8gt-Xty8pydulnmDshouQL16glxyVOPY/kawao4qOAG3d-Vut4K62JOcaRIggEPNqV738Go7Wftg" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/11/11/1670011200000/vDNIbVnCenipc2UTQksDiw/SXm6r3CZ94_kfwlf-jAY_r8QfDGTqDJPjQZvxJuBTMP0SP8yp622CiwSL-f8cIZSTq5sIOHdcBjQVNaI3vg0kBUdYDLo-WUUS3ZieuqjTiHNcPaeRJIwlMp8nqzW0Z9oEApjWNCPG1B7r1tPJ0kKDOXzt31yYR2NMJSteMqAypg/AyUW9K2Y4fpzKsX8v706i81N_ZLxnX9jSgO-Ti-ZA-U" style="width: 5em;" />

Scissors defeats Paper

<img src="https://v5.airtableusercontent.com/v1/11/11/1670011200000/a4jQfHX4Bt7R3Ct0DsdSiQ/50uSd_MSwsY5EoDUgpz-pLMMlDL3dNI7mwkYwJJ_LjUrnhkef19fbQW5kE7ERIaD7hpaZaJjp6QzkK6JbsrejvY0kVkvPl2ORL7ZWIvFUitQjFDBPDYMgc8Niui9kteoWE8ghnWSNah0ByL3A8509yreCEdImDVqyU8wz6_0lzQ/EleuLtghM8A57UA6U4SCXK66votMJOeNwNOrel72C-I" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/11/11/1670011200000/u7UPng61e-J5zuJftLTPoQ/lfv21wpko9JLcsKI-hYLe9G41zBv7d-rNOUQ8GMKYKy3H5WkZlbMpbmHOecSgHEhdQsONBSe5nkI-dBiJG4W747LDh9eHdjE94id3kULNNvJ3Gvfkpw3n179-lLH1GiwpWC90Gh9yAy8gt-Xty8pydulnmDshouQL16glxyVOPY/kawao4qOAG3d-Vut4K62JOcaRIggEPNqV738Go7Wftg" style="width: 5em;" />



If both players choose the same shape, the round instead ends in a draw.

Appreciative of your help yesterday, one Elf gives you an encrypted strategy guide (your puzzle input) that they say will be sure to help you win. "The first column is what your opponent is going to play: 

A for Rock
B for Paper
C for Scissors


The second column--" Suddenly, the Elf is called away to help with someone's tent.

The second column, you reason, must be what you should play in response: 

X for Rock
Y for Paper
Z for Scissors


Winning every time would be suspicious, so the responses must have been carefully chosen.

The winner of the whole tournament is the player with the highest score. Your total score is the sum of your scores for each round. The score for a single round is the score for the shape you selected 

1 for Rock
2 for Paper
3 for Scissors


plus the score for the outcome of the round (0 if you lost, 3 if the round was a draw, and 6 if you won).

Since you can't be sure if the Elf is trying to help you or trick you, you should calculate the score you would get if you were to follow the strategy guide.

For example, suppose you were given the following strategy guide:


A->Y

B->X

C->Z


This strategy guide predicts and recommends the following:

                        

    
**A->Y**

 - **Opponent Chooses:** Rock   (A)
 - **You should play:** Paper (Y)
 - **Result:** Win
 - **Final Score:** 2 + 6 = 8

 - **"Purple" Notes:** In the first round, your opponent will choose Rock (A), and you should choose Paper (Y). This ends in a win for you with a score of 8 (2 because you chose Paper + 6 because you won).

**B->X**

 - **Opponent Chooses:** Paper   (B)
 - **You should play:** Rock (X)
 - **Result:** Loss
 - **Final Score:** 1 + 0 = 1

 - **"Purple" Notes:** In the second round, your opponent will choose Paper (B), and you should choose Rock (X). This ends in a loss for you with a score of 1 (1 + 0).

**C->Z**

 - **Opponent Chooses:** Scissors   (C)
 - **You should play:** Scissors (Z)
 - **Result:** Draw
 - **Final Score:** 3 + 3 = 6

 - **"Purple" Notes:** The third round is a draw with both players choosing Scissors, giving you a score of 3 + 3 = 6.



In this example, if you were to follow the strategy guide, you would get a total score of 15 (8  + 1  + 6 ).



What would your total score be if everything goes exactly according to your strategy guide?

