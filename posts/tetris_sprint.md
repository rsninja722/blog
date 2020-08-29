# Tetris Sprint
##### 2020.08.28

## What Is Sprint?

Across the hundreds of versions of Tetris, the sprint game mode usually consists of the player being required to clear 40 lines as fast as possible. Since each game plays slightly differently, the world record time for a 40 line sprint is often considered on a game by game basis. Some games add delay between actions such as clearing lines, which makes the fastest possible time slower. The version of Tetris I'll be focusing on for this post is called [jstris](https://jstris.jezevec10.com/).     

## Why jstris?

jstris is the version that often has the fastest sprints played across all versions. This is because it is one of the most popular versions that is easily accessible on the web, there is no delay between any actions, and it runs without lag on almost any computer from this century.

## The Record

At the time of writing, the world record for clearing 40 lines sits at 15.654 seconds. This time was achieved by player [Vince_HD](https://www.youtube.com/channel/UCCzAoxNXXrD8onYFZaPqDqQ). I believe he is only 15 years old and uses a laptop keyboard.

Here is a replay of the game.

![](media/tetris1.gif)

## How Is This Possible?

There are many mechanics of modern Tetris versions that enable this level of speed

### randomizer

Unlike older versions of the game where the tetriminos given to the player were completely random, a 7 bag randomizer is used for most modern versions. This means you will be given all seven tetriminos in a random order repeatedly. 7 tetriminos are put in a "bag", and then taken out one by one and put into the queue. Once the "bag" is empty, it is refilled with the seven pieces again. This makes it so players can expect to wait a maximum of 13 pieces before they get the piece they want, and stack accordingly. 

### hold

Players are allowed to swap the piece in play, with one that they are holding. This allows a player to keep their stack clean by holding on to pieces that can't be placed well at the time. It is much easier to play quickly if the stack is kept clean, meaning that there are no gaps covered up and that the stack is fairly flat.

### preview

Most modern versions show the next 5 pieces that will be given to the player. This gives them time to think about where they will place a piece before they actually have to use it.

### DAS and ARR

The biggest factor that allows pieces to be moved so quickly are settings that the player can modify called DAS (delayed auto shift), and ARR (auto repeat rate). DAS is how long the player has to hold left or right before the piece will start moving sideways on its own. I like to keep DAS around 80 milliseconds. This makes it so I only have to hold a direction for around 5 frames before the piece starts moving automatically. There is no best DAS setting and everyone plays with whatever they are comfortable with. When starting out though, it is better to use a slower DAS as you get used to time it takes. ARR is the amount of time between each automatic movement to the side. Most players use a 0 ARR so the piece moves all the way to the side in one frame.

### hard drop

the hard drop button instantly drops the piece as low as it will go and place it. This is incredibly fast compared to holding down and waiting for the piece to fall.

### 180° rotation

Instead of rotating twice, players can use the 180° key to flip the piece faster.

### finesse

This isn't really a mechanic of the game, it's just a measurement of how efficiently a player is playing. 0 is the best score, and every point represents one unnecessary key press. For each piece in every possible placement there is a smallest amount of key presses to get the piece to that place. [here](https://harddrop.com/wiki/0G_60_Hz_SRS_Movement_Finesse) is every sequence if ya really want to look at it.

In this situation, instead of rotating then pressing right multiple times using 4 key presses, it is more efficient to use DAS to get to the right then rotate clockwise. This gets the piece to the desired location in only 2 key presses. 
![](media/tetris2.png)

## Abstraction

As with most amazing human accomplishments such as computers, government, and corporations, abstraction is what allows people to accomplish so much. When first starting to play Tetris, players have to take time to think about each key press. As they play the controls start to feel more natural and they can focus on where they want to place the piece. Eventually players stop thinking about the controls all together and can automatically execute sequences of key presses to move a piece where they want. All they have to do is abstractly think where they want a piece to be, and it will happen. Once a player has spent enough time playing, they can easily recognize patterns of multiple pieces. No longer do they have to think of where they want each piece to go, they can think of an area they want to fill, or a shape they want to create and they will do it automatically. At this point the player's brain is hardwired to play Tetris and can increase their speed by fixing or working on minor details in their playing.

## How Much Faster Can Players Go?

Vince_HD maintains an average of 6.5 pieces placed every second during his record breaking play. This equates to around 150 milliseconds per piece. The average human reaction time is 215 milliseconds according to [human benchmark](https://humanbenchmark.com/tests/reactiontime). He is already deciding where to place each piece at the upper limit of human reaction time, so any improvement past this point will most likely be in hundreds or tens of milliseconds. Unlike other old games like super mario bros. where the record is within seconds of the theoretical frame perfect run, the record for Tetris is still far from a perfect run. On jstris there are only 23 times under 20 seconds, 10 times under 18 seconds and 4 times under 17 seconds. Before Vince_HD's play, I never thought it was possible to get under 16 seconds, so who knows, maybe a new player will come along and shatter the record once again.

The [fastest possible time](https://www.youtube.com/watch?v=Uqr69JJFa88) is believed to be 1.65 seconds. Perfect RNG is needed and a piece needs to be placed every frame. An unmodified human will never come close to this time but we might be able to approach this time in the far future with brain modifications and interfaces.

## Me

I've been playing for almost 3 years, and my best time is 36.838 seconds at a speed of 2.7 pieces a second.

![](media/tetris3.gif)