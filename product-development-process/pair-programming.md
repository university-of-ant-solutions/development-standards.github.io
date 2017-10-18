---
description: Pair Programming
keywords: pair programming, agile, scrum, development
title: Pair Programming
---

# Pair programming

![Pair programming](/product-development-process/images/pair-programming.jpg)

Pair programming is when two programmers working at single workstation. The two programmers must swap between two roles frequently:

- One, the driver, writes code
- The other “navigates” reviews each line of code as it is typed in, suggesting ideas and catching errors.

The roles must be swapped on a timer, for example 5 minutes or 3 minutes, which you can set with a phone alarm or an application on the computer.

## Why do you want to pair programming ?
Advantages
## When do you want to pair programming ?

- *Conceptually complex tasks.* Pair programming can really improve your performance on conceptually complex tickets, because these are the ones where the number of details is so large that a single developer would be significantly slowed down and have a higher probability of making mistakes.Having another developer on hand reduces these problems.For example, when integrating a new payment provider with a backend server and a frontend app, the number of details is immense and could be ameliorated by pairing.

- *Speeding up important tasks (e.g. the sprint goal).* In order to prioritise the sprint goal, when the sprint backlog is empty but there are still sprint-goal-related tickets in doing, developers should pair on the sprint goal tickets rather than taking tickets from the product backlog.This brings the full development power of two devs to bear on the most critical work in the sprint.The exception to this is if a single dev is particularly well-placed to do the tickets and would be slowed down by pairing – in that case, that dev should tackle the sprint goal.

- *Training.* Pair programming is extremely useful for onboarding new developers – whether new to Theodo or new to a team.A more experienced developer can pair with a trainee to quickly and effectively share knowledge of the project and general coding skills.Pairing helps the trainee stay engaged and ensures they write code themselves, instead of leaving the work to the experienced developer.When pairing for training, it is particularly important to respect the timer.A good balance is for the trainee to pair in the morning and tackle tickets on their own in the afternoon.

- *Help.* When a developer needs help with a specific issue, they can ask another developer – for example their coach, the architect on the project or any developer who knows about the issue, or indeed any developer – to pair with them.Knowledge can then be shared fluently.
Even pairing with a developer with no specific experience in the project can be useful as they may catch errors you have missed, or bring fresh ideas

- *Bottlenecks.* When there are more developers available than tickets available (e.g. in the case of dependency chains, or blocked tickets), pairing can allow the full power of multiple developers to be focused on the available tickets.

- *Knowledge-sharing.* Pairing is great for the express purpose of sharing knowledge of a new feature – a developer working the sole ticket implementing new functionality can ask another developer to pair so that the second developer also learns the additional information that is being introduced to the project.This is important to maintain a cross-functional team, which is necessary for a scrum dev team.

- *Interviewing.* Pair programming is a revealing way to gain an insight into candidates interviewing for the role of developer.When you pair with someone, you can assess their knowledge firsthand, see how they react to new knowledge, and experience their style of communication and coding.

## Five Rules of Pair Programming Etiquette. These rules are:

1. **Agree on the physical environment beforehand**

    - When coding with another person physical environment counts. You might be accustomed to reading dark text on a light background. Your partner might prefer light text against black. As strange as it sounds, this is a significant disconnect. It’s hard to talk about code you cannot see. Your eyes become conditioned.
    - The same is true with keyboard shortcuts and mouse behavior. Some people like mouse wheels that roll down to move through a page, some people are used to down rolls. Asking a programmer to adjust the way he or she works hardware creates friction.
    - In terms of mouse and keyboard, if there is a disconnect, one of the programmers might have to designate a driver. If a designated driver scenario is not possible,  you might allow each programmer to stay at his or her workstation and use screen sharing technology found in products such as TeamViewer, Skype, GotoMeeting and Join.me.
    - Page color scheme format is a bit harder to accommodate, particularly when Integrated Development Environments are in play. Given enough time, one member of the pair programming team might agree to the other programmer’s screen preference. Or, both programmers might come up a color schema that is acceptable to each. Yet, both developers need to be able to view the code in a variety of ways– variable inspection, call stack and variable watches, for example.  A common environment needs to be identified. Not being able to glean code information quickly and accurately will cause friction and slow the pair down. Taking the time to agree on physical environment beforehand will save loads of time later on.

2. **When talking about code, always refer to line number and file name**
    - Take a look at the following question:
      >What is the value of the variable?
    - Compare the content of that question to the following question:
      >“What is the value of the variable, obj at Line 232 of the file, MyFile.java?”
    - The first question needs a whole lot more follow up to attain clarity. The second question, not so much, if any at all.
    - Thus, when talking about code, unless you are pointing directly at a monitor that you and your programming partner can see, always reference your focus of attention, at least by line number. Figuring out the place where you or your partner is giving attention takes time, time that could be spent solving a problem.
    - If you don’t have line numbers turned on in your IDE, do so. Knowing what to look at will save oodles of time in your labors.

3. **When disagreeing, talk in terms of benefit**
    - I have ideas. You have ideas. All programmers have ideas. That’s how we’re built. Sometimes pair programming ideas are in sync. Sometimes they’re not. Disagreement is good. That’s how better ideas are synthesized. However, disagreements that go on forever, with no resolution in sight, eat time.

    - One trick I’ve found that when I am in disagreement with a programming partner is to always talk in terms of benefit. For example, you can say, “I think that the benefit of using my idea is [STATE THE BENEFIT HERE]”. An idea without a benefit ain’t. It’s an opinion. And opinions are like noses. Just about everybody has one.

    - Coming to resolution on an idea is a lot easier when comparing benefits. Jousting away in the Lists of Opinion goes on until the other guy falls off the horse. Pair programming is not about trial by combat. Articulating benefit works!

4. **When feeling ill at ease, say so**
    - I am always aware about how much my feelings influence my thinking. When I am feeling assaulted, put on the defensive or frustrated, my immediate concern is to assuage the feeling, not to have better ideas. Trying to make bad feelings go away eats time. And, when in a pair programming situation, making bad feeling go away without making the other party aware of my ill ease is counterproductive.

    - Look we’re all human. Sometimes we get thrown by a snide remark, a piece of sarcasm or an unintended insult made by our programming partner. It happens. Most time the person casting the remark has no intention of harm. He or she is unaware. So there is a benefit to be had.

    - When you are ill at ease, say so. It’s better to let the information flow for a few minutes and make things right than to harbor a defensive grudge that goes on through the afternoon and into the night. You can say something as simple as, “Dude, I know you probably didn’t mean it, but calling my idea lame really hurt. Maybe moving forward you can just say that my idea has some shortcomings we need to address.”

    - Most people are intrinsically kind. Those that aren’t are not good candidates for pair programming. Better to make known your ill feelings as soon as you experience them. If the person can adjust, then move forward. If not, ask your manager to pair program with someone else.

5. **Bestow as many compliments as possible**
    - Pair programming is a very special type of intimacy between two human beings. Two people are working together at a very detailed level to solve complex problems.Your pair partner is sharing a very special part of him or herself: his or her thinking. For better or worse, it’s a relationship between two people, maybe not the type you have with a sibling or friend, but it’s not exactly as transient as sharing a seat with another person on the subway. You really do get to know a person by working with them.

    - One of the great benefits that I’ve found when having a good pair programming experience is the sense of empowerment I feel when we’re moving ahead together efficiently. Either I feel as if I am helping out, or I feel as if I am being helped out. It’s win-win.

    - One of the ways I’ve discovered to increase that sense of empowerment between myself and my programming partner is to always give a compliment when an opportunity to compliment presents itself. It is my firm belief that the human being has yet to be born that does not want to be appreciated for the work he or she does or the thinking he or she has. People want to feel good about they work they do. Pair programming is no exception. One of the fastest ways I have found to get a good feeling going is to offer a sincere compliment whenever I can. It doesn’t have to be a drama. Sometimes a simple, “good idea” will suffice.

    - When my pair partner feels good, I tend to feel good. And for those of us that have been on the terrain for a while have come to understand, happy cows make better milk. The more compliments you make, the more efficiently the pair will move.

## Reference
- https://www.versionone.com/agile-101/agile-software-programming-best-practices/pair-programming/

- https://blog.logentries.com/2017/01/5-rules-of-pair-programming-etiquette/

- https://www.theodo.fr/blog/2017/01/pair-programming-and-when-to-use-it/

- https://en.wikipedia.org/wiki/Pair_programming

