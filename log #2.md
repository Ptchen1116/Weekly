
## What I Learned

**1、DDIA**

I finished Chapters 2 and 3 of DDIA. Chapter 2 covers relational, document, and graph data models, along with their query languages. Chapter 3 covers storage engines, including index structures such as LSM-trees and B-trees, as well as OLAP (data warehouses) and column-oriented storage. Both chapters were challenging because I had only worked with relational databases before, but they gave me a much better understanding of how modern database systems are designed.

**2、[Should You Still Become a Software Engineer in 2026? GitHub VP](https://www.youtube.com/watch?v=W6aOdLlEz1w)**

Scott Hanselman, Vice President and Member of Technical Staff at Microsoft and GitHub, shared his thoughts on how AI will impact the future of software engineering and engineering careers.

He mentioned that although AI is excellent at creating new features, it does not design good architecture. AI-generated code can easily lead to god objects or messy code. Therefore, having a strong software development lifecycle (SDLC) is more important than ever. Scott pointed out that probably 70% of his code is written by AI, and AI-generated code still goes through the same processes as human-written code, including code review, signing, testing, and GitHub Actions workflows.

When asked what someone should do to land a software engineering job within 12 months, Scott emphasized two key areas:

1. **The Basics:** Learn core concepts such as HTTP, DNS, distributed systems, and concurrency topics like deadlocks. These fundamentals remain essential regardless of how much AI improves.
2. **Commnication and Clarity:** Become a clear communicator who can explain your code, design decisions, and trade-offs. The ability to articulate your thinking is a critical skill for engineers.

Scott also encouraged junior developers to use tools like [GitHub Copilot Chronicle](https://github.blog/changelog/2026-06-02-gain-insights-across-your-agent-sessions-with-chronicle/). Chronicle is a built-in analysis feature that captures insights from a developer’s historical GitHub Copilot interactions, allowing them to review, analyze, and improve their AI-assisted coding habits.

**3、[陽明交大專員偷刻教授印章虛報款項　遭開除刪光師生檔案遭判刑](https://www.ettoday.net/news/20260705/3195440.htm)**

The dismissed administrative staff member exploited a vulnerability in **Gmail’s “Forgot Password” recovery mechanism**, which failed to verify whether the administrator of the official email account still had authorized access privileges. By resetting the account password, the individual gained unauthorized access to the official mailbox and deleted important files.

I think organizations should immediately disable accounts when employees leave and make sure former employees cannot access company systems. They could also restrict external logins by allowing access only from trusted IP addresses or internal networks. Last but not least, important data should always be backed up regularly so it can be recovered if something goes wrong.


## What I Built

**1、LiveKit Server Deployment**

Successfully deployed a LiveKit server on an Azure Virtual Machine (VM). I also implemented a token exchange authentication workflow in which the frontend sends an application JWT to a backend endpoint. After validating the JWT, the backend issues a LiveKit access token, enabling the client to securely connect to the LiveKit server.

## Mistake I Made

**1、Keeping Git History Clean When Testing GitHub Actions**

While deploying the LiveKit server, I set up a CI/CD pipeline using GitHub Actions. During the process, I ran into an issue where the workflow couldn't read the required environment credentials. Since debugging GitHub Actions often requires pushing changes to trigger a new workflow run, I ended up making multiple commits with identical messages such as **"fix: unable to read environment credentials."** This cluttered my Git history, and I later had to use **git rebase** to clean up the commit history.

Fortunately, I was the only person working on the repository, so rewriting commit history did not affect anyone else. However, rewriting history is generally not a good practice once commits have been shared, as it can create conflicts for collaborators or other branches.

After discussing the issue with Gemini, I realized a better workflow for the future. When I encounter a bug that requires multiple trial and error commits, especially GitHub Actions issues that can only be tested by pushing code, I should create a dedicated branch, like `fix/github-actions-env`. I can make as many experimental or "dirty" commits as needed on `fix/github-actions-env` without worrying about polluting the main development history. Once the issue is resolved, I can open a **Pull Request** into the `dev` branch and use **Squash and Merge**. This approach keeps the `dev` branch history clean while still allowing me to preserve my debugging process. What’s more, if I want to discard those dirty commits, I can simply delete the branch after the fix has been merged.

## Things I Cared About

1、G2 took down T1 3–1, but I’m still buying the T1 skins coming out next Wednesday anyway.

2、[致癌物沙拉油最新流向》新增440項產品！24項食用油/16款泡麵/7款水餃/超商/台糖/泰山...退貨退款方式、下架品項批號一次看](https://www.storm.mg/lifestyle/11147131)

3、[【情報】巴哈姆特動畫瘋今晚新番首播預告《我是不才惡女~雛宮蝶鼠互換傳》](https://forum.gamer.com.tw/C.php?bsn=82464&snA=106&tnum=1)