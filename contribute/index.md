# General

SOBotics tries to leverage the programing skills of community members to improve the overall user experience for visitors of Stack Overflow. 
The main tool we are using is chat and bots (programs) that scan SO in real time to find issues that we can handle.

The quantity of posts (answers, questions), comments, reviews and other actions of SO users is huge. We are right at the beginning of our implementation and need support from other community members to both refine current programms and to address issues that have not been implemented yet.

These are some examples, but you're stepping in to an area where not only your programming skills are needed but also your ideas and passion are welcomed.

What follows is a list of our projects, and some particular areas they need help with.


# [Guttenberg](https://github.com/SOBotics/Guttenberg) - Java

## More reasons for a post to be reported (LINQ?)

With SOBotics/Guttenberg#74, it will be easier to add reasons that trigger a report.
It would be helpful, ff someone comes up with new reasons that could improve our results. For this, implementing LINQ could be tested. ( SOBotics/Guttenberg#73 )

## Web dashboard for reported posts

We can have a dashboard like http://diffchecker.com/ where we display the differences between posts. This would help in the plagiarism flags. 

## More sources

At the moment, Guttenberg can only compare posts to linked or related questions with the target. Getting data from GitHub or a search engine could improve the results.

----------------------------

# [Natty](https://github.com/SOBotics/Natty) - Java

## Addition of Machine Learning techniques to detect questions posted as answers. 

Over a period of 1 week, we have collected a [dataset](http://51.254.218.90:8000/vowpalData.txt) of all the new answers to old questions. Coupled with SEDE, we can learn the 

## Implementation of intelligent blacklist

The blacklisted words all have the same value at the moment. Getting data from Sentinel, we can find out as to how many false positives are there and find a way to autoscale the blacklist filter value. 

----------------------------

# [Heat Detector](https://github.com/SOBotics/SOCVFinder) - Java

## Improvising the NLP System

We can improve the NLP system, feed and or settings of NLP. At the moment, we are using a dataset of rude flagged comments provided by Stack Exchange. We can extend this by using the data that has been collected till now. 

## Improving perspective reports by providing feedback

Reports by Heat Detector because of Perspective do not take feedback as of now. We need to develop the bot to take feedback for that as well. 

------------------------

# New projects that are yet to be started

## LQP Queue Monitor

Low Quality Posts queue is infested with robo-reviewers who have deleted many posts which turn up as bad audits. Scraping the 10k LQPQ history page would help us find these users who can be flagged accordingly. 

## API cache

We are planning to cache the results of `/posts` or `/answers`. This would save us tons of requests to the SE API and would make it possible to run multiple bots on the same IP.
The AU-version of Natty for example could run on the same server as Guttenberg although they both use the API a lot. (multiple request per minute and bot)
