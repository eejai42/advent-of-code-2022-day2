
# Rock Paper Scissors

**NOTE:** This readme is DERIVED from the knowledge graph defined here:
        https://airtable.com/appsl1IuS9feiUMfF/tblvNX7NFoldBUYox/viwti0QueGt41e9Ec?blocks=hide

You may find this JSON version of rules helpful - which allows for the following pseudo code to solve the problem in ~8 lines.
**Knowledge Graph JSON**: [SSoT/Day02.json](SSoT/Day02.json).

        private int CalculateLineScore(string line)                                                   // i.e. "A Y" = 2 + 6 = 8
        {
            var parts = line.Split(" ".ToCharArray()).ToList();                                       // "A Y" => ["A","Y"]
            var opponentSign = this.SignsByOpCode[parts[0]];                                          // Full Sign Object for A = Rock
            var suggestedSign = this.SignsBySuggestionCode[parts[1]];                                 // Full Sign Object for Y = Paper
            if (suggestedSign.WinsAgainstName == opponentSign.Name) return suggestedSign.WinScore;    // Return 8
            else if (suggestedSign.LosesToName == opponentSign.Name) return suggestedSign.LossScore;  // Return 2
            else return sssuggestedSign.DrawScore;                                                    // Return 5
        }

The Elves begin to set up camp on the beach. To decide whose tent gets to be closest to the snack storage, a giant Rock Paper Scissors tournament is already in progress.

Rock Paper Scissors is a game between two players. Each game contains many rounds; in each round, the players each simultaneously choose one of Rock, Paper, or Scissors using a hand shape. Then, a winner for that round is selected: 

Rock defeats Scissors

<img src="https://v5.airtableusercontent.com/v1/13/13/1670054400000/Sn7v-AY1h-Cy0LH7Y-qbaQ/vWHJxabiDYhV6R1PDrshjZnt9kf_3jI32ZHES4_43VeqJl5s0fSw2DvbIAeGj6fjG6YoP5QGPtHBBpYAeG5mIZCbMAzcd2HVCfWj2ImzwF8ROMT_3o1QFYu9H3NvmZzaD2CByZ2x6hyQrRCo06hHVEUkSuZwcP2d8mtpszFGMdo/bv159n2QdnQyS9CaXeLBj0LvD-pelTvxCX6iyXQociI" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/13/13/1670054400000/6jzsY8XKfRrp7DtmnIz6Cg/Zo5th4PWxucXkdAA00qmm4AuYkAMRkauGhC6GyQ-wymQHfuxz1NpSnUipHSjyxoP8obgvkyfLJ4xRjlp8oQBE-uRRvXYCcA3pXMFjCKh2cUqeClSJ4ZBaEMX-3HVV3FdX7VlLHfPK9UkX0P92UuzdfzPNvV5OyGObcVre2hTmu4/fvoUqCVAX2k_GIwYt_Sn5E4hjvVg8HhFWGApbcN5Pt4" style="width: 5em;" />

Paper defeats Rock

<img src="https://v5.airtableusercontent.com/v1/13/13/1670054400000/IHoa_8MYcnIJ3UiSFJ8NGQ/oJlKEQsxzGpkxUJV1R4uOf3l89UmqAchsdK_DJiRb8uJJV23un3P-_WUHU8jtN8lp_qSs225bb8vn0WqtKOqMj5CnOyffJEzafXJ3n3qucpuFL_fIRyp6R28n754wxELsbdPS-FqPhFUh_HauL77D-EN8oK7Rdg2oWwas3LHhPs/kMiMGjGhvI9L-UAm35tZ27sVo_JGBQOb1N8cl2jx5BA" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/13/13/1670054400000/Sn7v-AY1h-Cy0LH7Y-qbaQ/vWHJxabiDYhV6R1PDrshjZnt9kf_3jI32ZHES4_43VeqJl5s0fSw2DvbIAeGj6fjG6YoP5QGPtHBBpYAeG5mIZCbMAzcd2HVCfWj2ImzwF8ROMT_3o1QFYu9H3NvmZzaD2CByZ2x6hyQrRCo06hHVEUkSuZwcP2d8mtpszFGMdo/bv159n2QdnQyS9CaXeLBj0LvD-pelTvxCX6iyXQociI" style="width: 5em;" />

Scissors defeats Paper

<img src="https://v5.airtableusercontent.com/v1/13/13/1670054400000/6jzsY8XKfRrp7DtmnIz6Cg/Zo5th4PWxucXkdAA00qmm4AuYkAMRkauGhC6GyQ-wymQHfuxz1NpSnUipHSjyxoP8obgvkyfLJ4xRjlp8oQBE-uRRvXYCcA3pXMFjCKh2cUqeClSJ4ZBaEMX-3HVV3FdX7VlLHfPK9UkX0P92UuzdfzPNvV5OyGObcVre2hTmu4/fvoUqCVAX2k_GIwYt_Sn5E4hjvVg8HhFWGApbcN5Pt4" style="width: 5em;" /> -> <img src="https://v5.airtableusercontent.com/v1/13/13/1670054400000/IHoa_8MYcnIJ3UiSFJ8NGQ/oJlKEQsxzGpkxUJV1R4uOf3l89UmqAchsdK_DJiRb8uJJV23un3P-_WUHU8jtN8lp_qSs225bb8vn0WqtKOqMj5CnOyffJEzafXJ3n3qucpuFL_fIRyp6R28n754wxELsbdPS-FqPhFUh_HauL77D-EN8oK7Rdg2oWwas3LHhPs/kMiMGjGhvI9L-UAm35tZ27sVo_JGBQOb1N8cl2jx5BA" style="width: 5em;" />



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

