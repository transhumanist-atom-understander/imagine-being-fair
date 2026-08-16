One model of rational agency is a proof-based agent, and one fun exercise with proof-based agents is to play them against each other in prisoner's dilemmas.
They exchange source code and try to decide whether to cooperate or defect by writing formal proofs.

In this game, two agents that are in a certain sense fair—that cooperate if and only if there's a proof that their opponent cooperates—will cooperate with each other.

Of course, playing fair isn't playing to win, and [the paper on this game](https://arxiv.org/abs/1401.5577) defined a "prudent" player that does better than a fair one.
But cooperation between fair agents is the simplest interesting exercise in proof-based decision theory.

Personally, though, I found this exercise discouraging, and not only because it required deep math to answer such a simple question.
These two fair players are looking for proofs of the other's cooperation, and you can prove they both find them.
But I can't really imagine what reasoning these agents are doing about each other.

Recently, I was trying out a different but [equivalent](https://www.lesswrong.com/posts/2JQzDZXjoG2opnAjk/my-payorian-fairbot-was-just-the-original-fairbot) definition of fairness, and found the proof of mutual cooperation to be not only elementary but satisfyingly explicit.
If you want to actually imagine being a fair agent deciding to cooperate, then read on.

## Terminology and the new definition of fairness

When talking about provability, I'll sometimes say that a player knows something when I mean there's a proof of it.
So the old definition of fairness is that a fair player cooperates if and only if they know their opponent cooperates.

I'll also sometimes talk about "possibility".
When I say something's impossible, that means there's a proof it can't happen.
So another way to state the old definition of fairness is that a fair player defects if and only if it's possible that their opponent defects.

The new definition of fairness depends on a new concept: betrayal.
If I betray you, that means not only that I defect, but that I knew you would cooperate and defected anyway.

Now, the new definition of fairness.
A fair player defects if and only if it's possible that their opponent betrays them.

## If you're fair, and know I'm fair, you cooperate

First, a fact about betrayal.
If there's a proof I cooperate with you—that is, if it's impossible that I defect against you—then it's also impossible that I betray you.

With that in mind, we can prove that a fair player never betrays anyone.
Suppose you're fair.
And suppose you're playing against some other player that you know cooperates.
It's therefore impossible that they betray you.
So, being fair, you cooperate.
There's no one that you know cooperates but defect against—no one you betray.

Now let's assume not only that you are fair, but that you know I'm fair.
Then you know I don't betray you, so you cooperate.

## Conclusion

Maybe proof-based decision theory isn't as hard as we thought?
Years ago, we could have made a different choice among equivalent definitions of fairness.
Then we wouldn't be saying that [fair players cooperate with each other because of magic](https://www.lesswrong.com/w/logical-decision-theories?lens=an-introduction-to-logical-decision-theory-for-everyone-else#Logical_decision_theory).
Although proving equivalence of the two fairness definitions does require magic (that is, Löb's theorem).

By the way, though the "betray" terminology is new in this post, it's just an English translation of a suggestion from James Payor [which has been the subject of a few different posts](https://www.lesswrong.com/w/payor-s-lemma).
I thought [his explanation of the motivation](https://www.lesswrong.com/posts/LaCP6WyNzX8kiZn3w/payorian-cooperation-is-easy-with-kripke-frames?commentId=tQ4KqFQ8a5K8qt2Ye) was interesting.
