# Chernobyl and Software Engineering

And by Chernobyl I mean the HBO miniseries Chernobyl, not the nuclear power plant.  Ceci n'est pas une pipe. \
\
A while ago, I read [this](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/) blog post by Joel Spolsky and it felt very universal, in that everywhere I have worked as a software developer has had some healthy or unhealthy push and pull between developing new features and doing all of the work that surrounds new features, like writing tests, documentation, refactoring, etc.  \
\
And then I watched the miniseries Chernobyl.  In Chernobyl there is a scene where a professor Legasov is explaining to a tribunal after the nuclear disaster how an RBMK reactor like the one at Chernobyl could explode.  In his explanation, he has a set of red and blue cards that he places on an easel of sorts to show how different forces counteract each other and create energy without explosion.  If you haven't seen the series, the speech can be found [here](https://www.youtube.com/watch?v=TmIEI4ky-Zc).\
\
Software engineering has something of a balance that is metaphorically similar.  I know that Chernobyl is an overly dramatic metaphor for most software engineering projects, but bear with me.  I'll paraphrase the miniseries here.\
\
...

\
You don't need to be a software engineer to understand what happens in software development. You only need to know this: There are essentially two things that happen inside a software project. The amount of possible things an application can do (features, race conditions, logic errors, crashes) aka reactivity, which generates money, either goes up or it goes down. That's it. All the software team does is maintain balance.

Features. As features are added, reactivity goes up. But if you don't balance your activity, it never stops rising.  The leads to a code base that is buggy,  impossible to reason about, hard to add new features to, difficult to refactor, etc.  The more things an application can do, the more ways it can fail.

So, tests. They reduce reactivity like brakes on a car.

But there's a third factor to consider, users. Users interact with the system. As they do they find bugs, but once major bugs are cleared they instead create requests for features, or what we call a "void." In software projects, there's something called a "positive void coefficient." What does that mean?

It means that the more users present within the system the higher the reactivity, which means more features, which means more users, which means -- it would appear we have a vicious cycle on our hands. And we would were it not for this... the "negative senior coefficient."

When software engineers get more experience with a code-base it gets less reactive. So features increase reactivity; tests and bug reports reduce it; feature requests increase it; team experience reduces it. This is the invisible dance that powers entire economies without sweat or flame. And it is beautiful when things are normal.

As features are added to a code-base, the overall application decays into technical debt. Technical debt reduces reactivity.

This is the poison which kills otherwise thriving software products.

When the software team is running at full power it burns the technical debt away before it can cause a problem. But because of the under-staffing and under-prioritization, software teams can be directed only at feature development. The technical debt does not burn away. It built up, poisoning the application.

We're starting to lose balance.

Now application development is primed to slow down. And yet, in less than a year it will explode. If you can't understand how a stalled software project could lead to an explosion, I don't blame you. After all, you don't have an MBA and manage a SaaS product.

But, as it turned out, the MBA's who do, don't understand it either.\
\
...

Professor Legasov then goes on to explain how the Chernobyl disaster went on to occur, but I think by now you get the idea.  &#x20;

At the end of the day there are two parties at fault at Chernobyl.  The first party is easily apparent.  The operators of the power plant didn't truly understand the balance that is required to avoid disaster. &#x20;

The second party is the soviet managerial system which chose to use graphite tipped rods which were cheaper than their safer alternative.  Graphite increases reactivity, so when the operator team presses the emergency stop button and all of the control rods (which are meant to reduce reactivity) are inserted into the nuclear reactor core, reactivity spikes to uncontrollable levels and an explosion occurs. \
\
What this means for software engineering is that both the managerial class and the operator class must understand the second order and chain reactive effects that occur inside of a software engineering project.  \
\
Here is a simple effect everyone can get behind:  A code base with no tests is cheaper to produce, but costs money in debugging. \
\
Less simple:  Allocate no time to refactoring and reactivity increases, but the code base becomes unpleasant to work in.  A code base is someone's work environment for 8 hours per day, every single day. An unpleasant code base will discourage senior engineers and they'll move to other projects or companies.  Senior engineers reduce reactivity.  Junior engineers replace them.  Junior engineers increase reactivity.  Reactivity tends towards explosion.\
\
How would you explain something like this to a new executive who has never written a line of code before in their life and whose time is so guarded that they will only ever speak to you (an operator) for 5 or so minutes at a time?   They will never see inside of a control room, they don't know what IDE stands for. &#x20;

In the show, the operators can feel that something is wrong in the reactor, but against their instincts they follow the orders of their superiors.  Their superiors follow the orders of their superiors as well, each of them more and more disconnected from the action that is occurring in the control room.  I've been on both sides of this aisle in my career.  I have felt the uneasiness of the operator in various software engineering positions I've held and I have also felt the top down pressure to increase revenue in product positions.\
\
There is no answer in the show to how to fix this issue, and you won't find any concrete answers in this blog post either.  \
\
Operators, trust your instinct. If a feature takes a little longer to get out to get out right, then that's okay but it's a balance.  If you don't have enough reactivity your product won't get users and you'll be out of a job no matter how perfect the code-base is, and remember, everything is context specific.  A startup can handle more reactivity than an incumbent enterprise code-base. \
\
Managers, trust your operators.  Hire good ones.  Balance the number of seniors and juniors on your team.  Remember, everything you do has second order and third order effects.  Spend some time talking to your operators about those effects.\
\
It doesn't take a nuclear physicist to understand what is going on inside of a software project. &#x20;
