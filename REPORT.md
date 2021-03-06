###Primary Problem

The primary reason behind undertaking this project was an issue that almost all our team members faced during our recent summer internships. As new hires, we were expected to get familiarized with the codebase of some software project. All of us faced occasional ambiguities in understanding some part of the code or the rationale behind designing and writing code in a particular way, or wished to coordinate a joint action with the code owner to improve it. However, the task of finding the most relevant person to contact for resolving our ambiguities was a difficult task as it required mining through the long commit histories in the repository. Secondly, Slack is a core tool that is being increasingly used by developers in software companies. A wide range of Slack bots have been developed to automate a variety of tasks to improve work productivity. Owing to these two aforementioned reasons, we decided to build a Slack bot to solve this problem.

###Primary Features

1) Finding the top contributors to a file based on number of commits - This feature can be used to rank the users in nonincreasing order to find out the developers who are most well-acquainted the code. 

2) Finding the most recent contributors to a file based on time of commits - This feature can be used to rank the users in a nonincreasing order of the time of commits. This feature is useful in cases where the person who is well-acquainted with the code is no longer associated with the project or the team has undergone changes recently.

3) Finding the top contributing organizations based on number of commits - A lot of projects are becoming open source these days. Many organizations are contributing to these open source projects. So this feature would be useful in finding out organization - wise contributions to the code.


###Screenshots

1) Interaction with Bot

<img width="1130" alt="screen shot 2016-12-04 at 3 59 59 am" src="https://cloud.githubusercontent.com/assets/7821766/20869402/b1b8fe3c-ba3f-11e6-9265-b34a74ad4ba2.png">


2) Fetch commit history of repository

<img width="1131" alt="screen shot 2016-12-04 at 4 00 50 am" src="https://cloud.githubusercontent.com/assets/7821766/20869409/c82327a6-ba3f-11e6-80f1-9d1a9479b26e.png">


3) Get top n committers

<img width="1131" alt="screen shot 2016-12-04 at 4 01 20 am" src="https://cloud.githubusercontent.com/assets/7821766/20869415/e7cfa7c8-ba3f-11e6-8d9c-b933b6054e5e.png">


4) Get top n recent committers

<img width="1139" alt="screen shot 2016-12-04 at 4 02 00 am" src="https://cloud.githubusercontent.com/assets/7821766/20869437/40dc044c-ba40-11e6-9aea-ef5f24e7161e.png">

5) Get organization wise contributions

<img width="1136" alt="screen shot 2016-12-04 at 4 02 47 am" src="https://cloud.githubusercontent.com/assets/7821766/20869442/557dd22c-ba40-11e6-81c1-75a148134f12.png">


###Reflection on the development process and project

Working on this project was a great experience as it gave us a good hands-on experience with the various stages in the SDLC. We also gained a good understanding of working with Node.JS, Slack and GitHub APIs. Each of us worked concurrently on some feature in each phase and put together our work in the end, except in the deployment phase. In the deployment phase, we adopted a different approach to accomplish the task assigned to us. All of us sat together to solve the problem as none of us had any experience in performing a complete project setup including deployment on an EC2 instance. Throughout the project, we focused on getting the basic functionality implemented first, and thereafter tried to polish our work in further iterations by handling edge cases, adding additional functionality, etc. Overall, it was a challenging yet rewarding experience, and we are glad that we could accomplish the project successfully.

###Limitations and future work
1. We are considering only the contributions to the default branch. As a part of future work, we can consider contributions to all the branches within the repository while calculating statistics. 
2. Currently, we are providing email IDs of the contributors. We can later improve on this and provide the Slack handle of those contributors to improve ease-of-use. 
3. The GitHub API is quite restrictive in terms of the number of commits we can fetch per API call. To support GitHub repositories having a large number of commits, we have to make multiple API calls. As a result, the users may have to wait for some time before they can start querying.
