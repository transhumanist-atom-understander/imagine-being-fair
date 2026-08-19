One model of rational agency is a proof-based agent, and one fun exercise with proof-based agents is to play them against each other in prisoner's dilemmas.
The players are computer programs that exchange source code and try to decide whether to cooperate or defect by writing formal proofs.

In this game, two agents that are in a certain sense fair—that cooperate if and only if there's a proof that their opponent cooperates—will cooperate with each other.

Of course, playing fair isn't playing to win, and [the paper on this game](https://arxiv.org/abs/1401.5577) defined a "prudent" player that does better than a fair one.
But cooperation between fair agents is the simplest interesting exercise in proof-based decision theory.

I found this exercise discouraging, and not only because it required deep math to answer such a simple question.
Even after doing the proof, I couldn't really imagine being a player in this game, reasoning through the situation and deciding to cooperate.

Recently, I was trying out a different but [equivalent](https://www.lesswrong.com/posts/2JQzDZXjoG2opnAjk/my-payorian-fairbot-was-just-the-original-fairbot) definition of fairness.
With the new definition, I found the proof of mutual cooperation to be not only elementary, but also satisfyingly explicit about the reasoning a fair player could do to decide to cooperate.

I'll start by discussing mutual cooperation with the old definition of fairness, and try to communicate why it's so unsatisfying.
Then I'll give the new definition of fairness, and we'll think through a fair-vs-fair match from the perspective of one of the players.

## Mutual cooperation with the old definition of fairness

In this section I'll use the old definition of fairness.
To repeat: a fair player cooperates if and only if there's a proof that their opponent cooperates.

When talking about provability, I'll sometimes say that a player knows something when I mean there's a proof of it.
So a fair player cooperates if and only if they know their opponent cooperates.

I'll also sometimes talk about "possibility".
When I say something's impossible, that means there's a proof it can't happen.
So a fair player defects if and only if it's possible that their opponent defects.

Suppose that you're fair and you know I'm fair.
Mutual cooperation seems, if circular, at least consistent: we each cooperate because the other (provably) does so.
But can you really rule out the possibility that I defect?
Mutual defection seems equally self-consistent.

Suppose I do defect. Why would that be?
I'm fair, so it must be because it's possible that you defect.
Why would you defect?
You're fair, so it must be because it's possible that I defect.

Can we really rule out such a circle of suspicion?

As it turns out, Löb's theorem guarantees that when we both go looking for proof of the other's cooperation, we both find it.
But even though I can follow the argument, there's something missing—perhaps you could call it a mechanism.

I thought I just had to live with this unsatisfying argument until I learned a new definition of fairness, which I'll give in the next section.
If you want to actually imagine being a fair agent deciding to cooperate, then read on.

## Mutual cooperation with the new definition of fairness

The new definition of fairness depends on a new concept: betrayal.
If I betray you, that means not only that I defect, but that I knew you would cooperate and defected anyway.

Now, the new definition of fairness.
A fair player defects if and only if it's possible that their opponent betrays them.

First, a basic fact about betrayal.
Defecting against you is a necessary condition for betraying you.
Therefore, if there's a proof that someone cooperates with you—that is, if it's impossible that they defect against you—then it's also impossible that they betray you.

With that in mind, we can prove that a fair player never betrays anyone.
Suppose you're fair.
And suppose you're playing against some other player, and you have a proof that they cooperate.
It's therefore impossible that they betray you.
So, being fair, you cooperate.
There's no one who you know will cooperate but still defect against—no one you betray.

Now let's assume not only that you are fair, but that you know I'm fair.
Then you know I don't betray you, so you cooperate.

## Conclusion

With the old definition of fairness, it seems like a fair-vs-fair match could go either way.
Defect-defect looks plausible, but we rule it out with some weird math fact.

With the new definition, I can imagine being a fair player reasoning about my opponent: they're fair, so they don't betray anyone, so I'll cooperate.

To me, this is encouraging.
Maybe proof-based decision theory isn't as hard as we thought, right?
Years ago, we could have made a different choice among equivalent definitions of fairness.
Then we wouldn't be saying that [fair players cooperate with each other because of magic](https://www.lesswrong.com/w/logical-decision-theories?lens=an-introduction-to-logical-decision-theory-for-everyone-else#Logical_decision_theory).
Although proving equivalence of the two fairness definitions does require magic (that is, Löb's theorem).

By the way, though the "betray" terminology is new in this post, it's just an English translation of a suggestion from James Payor, [which has been the subject of a few previous posts](https://www.lesswrong.com/w/payor-s-lemma).
I thought [his explanation of the motivation](https://www.lesswrong.com/posts/LaCP6WyNzX8kiZn3w/payorian-cooperation-is-easy-with-kripke-frames?commentId=tQ4KqFQ8a5K8qt2Ye) was interesting.
