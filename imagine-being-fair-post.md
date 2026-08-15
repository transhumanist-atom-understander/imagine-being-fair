One model of rational agency is a proof-based agent, and one fun exercise with proof-based agents is to play them against each other in prisoner's dilemmas.
They exchange source code and try to decide whether to cooperate or defect by writing formal proofs.

In this game, two agents that are in a certain sense fair—that cooperate if and only if there's a proof that their opponent cooperates—will cooperate with each other.

Of course playing fair isn't playing to win, and [the paper on this game](https://arxiv.org/abs/1401.5577) defined a "prudent" player that does better than a fair one.
But cooperation between fair agents is still special as the simplest interesting exercise in proof-based decision theory.

Personally, though, I found this exercise a bit depressing, and not only because it requires deep math for such a simple question.
You prove that both these agents looking for proofs of the other's cooperation find them, but there's something missing.
I can't really imagine what reasoning these agents are doing about each other.

Recently though, I learned that with another [equivalent](https://www.lesswrong.com/posts/2JQzDZXjoG2opnAjk/my-payorian-fairbot-was-just-the-original-fairbot) definition of fairness, the proof of cooperation is much more explicit.
If you want to actually imagine being a fair agent deciding to cooperate, then read on.

## Terminology and the new definition of fairness

For talking about provability in English, I'll sometimes instead talk about possibility.
If something's impossible, that means there's a proof it can't happen.
I'll also sometimes say that a player knows something when I mean there's a proof of it.
So the old definition of fairness is that a fair player cooperates if and only if they know their opponent cooperates, or that they defect if and only if it's possible that their opponent defects.

The new definition of fairness depends on another concept I'll have to introduce, which is betrayal.
If I betray you, that means not only that I defect, but that I knew you would cooperate and defected anyway.

The new definition of fairness is that a fair player defects if and only if it's possible that their opponent betrays them.

## If you're fair, and know I'm fair, you cooperate

First of all, an obvious fact about betrayal.
If there's a proof I cooperate with you—that is, if it's impossible that I defect against you—then it's also impossible that I betray you.
That's just because defection is a part of betrayal.

With that in mind, we can prove that, if you're fair, you don't betray anyone.
To betray someone, there would have to be a proof that they cooperate, and you defect against them.
But suppose there's a proof I cooperate.
We just saw that means it's impossible that I betray you.
So, being fair, you cooperate.

Now that we know that fair players don't betray anyone, let's assume not only that you are fair, but that you know I'm fair.
Then you know I don't betray you, so you cooperate.

## Conclusion

Maybe reasoning about proof-based agents isn't as hard as we thought?
Years ago, we could have made a different choice among equivalent definitions of fairness.
Then we wouldn't be [saying that fair players cooperate with each other because of magic](https://www.lesswrong.com/w/logical-decision-theories?lens=an-introduction-to-logical-decision-theory-for-everyone-else#Logical_decision_theory).
Although proving equivalence of the two fairness definitions does require magic (that is, Löb's theorem).
