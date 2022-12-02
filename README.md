
# Rock Paper Scissors

**NOTE:** This readme is DERIVED from the knowledge graph defined here:
        https://airtable.com/appsl1IuS9feiUMfF/tblvNX7NFoldBUYox/viwti0QueGt41e9Ec?blocks=hide

You may find this JSON version of rules helpful - 
**Knowledge Graph JSON**: [SSoT/Day02.json](SSoT/Day02.json).

The Elves begin to set up camp on the beach. To decide whose tent gets to be closest to the snack storage, a giant Rock Paper Scissors tournament is already in progress.

Rock Paper Scissors is a game between two players. Each game contains many rounds; in each round, the players each simultaneously choose one of Rock, Paper, or Scissors using a hand shape. Then, a winner for that round is selected: 

Rock defeats Scissors

<img src="https://v5.airtableusercontent.com/v1/11/11/1669996800000/AdgSpuiPGi-DTU-FDneGQQ/fQCX8RHi1DqPZ1XhV2NWKVixQ9RwgqhmfwGAvHO7VVNph_0D-c_e_doAmtEXAWfrak4beAY3cvmgyxsUBEuDgqBYrXWa4AQhxeq0N2GT-qiuSxfckwurNrptEoaf_TBBE1oU3Sfl2o_HuQLBW9NsOck7Q4tygEV-I-oSh4F_Jqs/LMu7KTNaYtANYuagXbDnktt3nTniVwAez89JH44IsP8" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/11/11/1669996800000/BwTXWC_CF28syozIpjifLQ/pVaqPq2jrvslYrRiK1wbgE45qRfTUw-qrYADq-Bez9yLnLsFF7OVCrSM7E76sznfMNSCY-5BBnjMVEI2TjpctPKsaj93daMQqf0sP7iJZZfusdJm9KRZ1_UKRf8IrmZM_T6LN46BuSdTlJWClUebjLt9WIg4Br0NHMvTyvnKMq0/iB0FvRjkPF7WddqKuGAQ08qViDjfzKhgTebuK06kNms" style="width: 5em;" />

Paper defeats Rock

<img src="https://v5.airtableusercontent.com/v1/11/11/1669996800000/2pVThO1GQUa6a3rmad12Vg/PyLJzvrdNRbNb2hyhyskcBiHQ0pwtMOQITRAG0-mqoVtnAwdNaeXErsw4H7z0m96Gmt1uSxxc_H3O2xNUTNuRKW5bMeMED6N8lS9l03jgGu9CmZBVI9d8-5Cc3sA-0n5wbMYsp4wp471Ah160qqiuWS9Q1XKQfGWl0YIKrcq6CE/MH3tulrPAoa3LBSpf4fyRhrCNSaCXG8YP07f6uE-UaA" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/11/11/1669996800000/AdgSpuiPGi-DTU-FDneGQQ/fQCX8RHi1DqPZ1XhV2NWKVixQ9RwgqhmfwGAvHO7VVNph_0D-c_e_doAmtEXAWfrak4beAY3cvmgyxsUBEuDgqBYrXWa4AQhxeq0N2GT-qiuSxfckwurNrptEoaf_TBBE1oU3Sfl2o_HuQLBW9NsOck7Q4tygEV-I-oSh4F_Jqs/LMu7KTNaYtANYuagXbDnktt3nTniVwAez89JH44IsP8" style="width: 5em;" />

Scissors defeats Paper

<img src="https://v5.airtableusercontent.com/v1/11/11/1669996800000/BwTXWC_CF28syozIpjifLQ/pVaqPq2jrvslYrRiK1wbgE45qRfTUw-qrYADq-Bez9yLnLsFF7OVCrSM7E76sznfMNSCY-5BBnjMVEI2TjpctPKsaj93daMQqf0sP7iJZZfusdJm9KRZ1_UKRf8IrmZM_T6LN46BuSdTlJWClUebjLt9WIg4Br0NHMvTyvnKMq0/iB0FvRjkPF7WddqKuGAQ08qViDjfzKhgTebuK06kNms" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/11/11/1669996800000/2pVThO1GQUa6a3rmad12Vg/PyLJzvrdNRbNb2hyhyskcBiHQ0pwtMOQITRAG0-mqoVtnAwdNaeXErsw4H7z0m96Gmt1uSxxc_H3O2xNUTNuRKW5bMeMED6N8lS9l03jgGu9CmZBVI9d8-5Cc3sA-0n5wbMYsp4wp471Ah160qqiuWS9Q1XKQfGWl0YIKrcq6CE/MH3tulrPAoa3LBSpf4fyRhrCNSaCXG8YP07f6uE-UaA" style="width: 5em;" />



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

