On why the house always wins.

- talk about the man who lost his best friends on that ski trip
- talk about earlier referencing how she saved you

After having dated my girlfriend for almost 5 years, I'm still amazed at the number of times where her genius and intellect have stopped me from going down a path of pain
fueled by my own ego and unwavering belief in my own ability to solve any "problem." Of course the only issue, is that not everything is a "problem" with clearly defined
input and output, as my job and personal interests tend to lead me to believe. In particular, the hill she saved me from dying on was believing I could beat the roulette
machines at our local casino with what I thought was an "unbeatable" strategy.

It all started with a very simple observation. For outside odds like red/black, even/odd, the chances that I hit at least once on a given option within the span of one try is 50%.
However, if I try twice, my odds increase from 50% to 75%!. Don't believe me? Think about a simple coin toss. What are the odds of you flipping tails at least once
given that you are going to flip twice? Well, take all possible outcomes where I get tails over the total number of outcomes. All the possible outcomes are
(Heads, _Tails_), (_Tails_, _Tails_), (_Tails_, Heads), and (Heads, Heads). Three out of four times, I win! In fact, for any n where n is the number of tries to get a given outcome,
we can calculate the rate of success as 1 - (probability of outcome)^(number of tries) where (probability of outcome)^(number of tries) = odds that you don't ever get your desired outcome.
Hopefully the intuition is clear, but if not, 1 represents the total probability of all outcomes. Subtracting the times where the thing I wanted doesn't happen at all will leave me with
all the times where it does. If I keep rolling, my odds increase asymptotically which is just a big word way of saying it gets really close to being guaranteed.

Great, now what does "win" mean in the context of the casino? It means leaving with more than you came in with. If, starting with 100 dollars, I bet five dollars on
black, and it turns out to be right, I've got 110 dollars! If I'm wrong, I'm at 95 dollars. Stay above 100. Simple, right?

When thinking about things that involve risk, we of course need to do everything in our power to skew the results of an unpredictable future in our favor where
possible (and legal). In my head that meant two of two things.

1. Make the number of attempts high enough that the losses are so low in probability that they become negligible.
2. Ensure that if you were to lose, the value of how much you lose, pales in comparison to what happens when you win.

From there, the strategy was clear. I would choose a sufficiently large enough n, where the odds of me hitting black at least once are in the high 95%. (For 50/50 odds, that number is 9).
Now, to ensure that the value of how much I lose pales in comparison to what happens if I were to win, I'll make sure to always bet more money when I win, and less when I lose. In practice,
this means that every win needs to compensate for any losses incurred up until that point (plus more because who wants to walk out with what they came in with).
In my case, it meant _always double your bet when you lose_. If I'm right, always doubling my bet (up to 9 tries) 99% of the time, will give me more money than when I started. To protect
against downside risk, I would "reset" my wager to some base amount after I won, so that when I lose, I can "almost guarantee" that I make it back.

Just to recap the plan is this:

1. Starting with some initial amount a, place a minimum bet of b.
2. If you guess the correct outcome, "reset" your bet to be the minimum amount and add the amount you won to the final amount.
   a. If you're wrong, subtract what you bet from the final amount and double your last bet.
3. Repeat steps 1 and 2 until you reach a desired final amount.

Great, all I need to do is choose a sufficiently high enough starting point, that I can afford to lose 9 times in a row. (For 50/50 odds, that number is ~2600).

At this point, armed with all the technical analysis and statistics to back me up, I approached my partner to explain how we'll never have to work again a day in our lives. This new get
rich slow plan I've described won't make us billionaries, but it should be enough to cover the cost of rent. I explained the steps carefully and consisely, taking care to
preemtively address any concerns that she might raise, and almost immediately I was met with resistance.

"Why do you think you have a unique perspective on this problem?"

"Don't you think if this was possible, casinos would ban roulette tables?"

"Have you tried to research to see if anyone has tried something similar?"

"Even if this strategy does 'work', you're only making 5 dollars each time. I could find you 5 dollars on the ground."

Perhaps the most damming critique of all was "The fact that you headed back to the casino to try out this strategy means that they've won." A statement so simple, but stunningly
complex to understand when you've convinced yourself of a certain idealogy. In any event, for every comment, I had a reply. If she swung, I dodged. And with enough tireless debate,
her final words to me were "Look, if its so simple, why don't you simulate it, because 'I lost all my money at the casino' isn't going to cut it when rent is due.".

Great! Now I have both a mission and a goal, backed by sound data from my back of the envelope calculations, and confirmation (at least in my head at the time) that the strategy was both
correct, and _viable_, but most importantly, I had a way to _prove_ both of those to be true. Unfortunately, because I was also headed off to get a haircut, I wouldn't have time to write this
proof out in code.

Enter repl.it! A platform for running and testing code live in the browser. I could write a couple helper functions to get the main parts of the simulation down in the Uber to my haircut. I
would set up the recurring scenarios while waiting my turn, and while I'm getting my haircut, I could watch the line go up and the the right confirming what I thought to be true.
