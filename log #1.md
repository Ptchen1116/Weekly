
## What I Learned

**1、DDIA**

I finished the first chapters of Designing Data-Intensive Applications. Chapter 1 was very insightful, introducing the three core goals of data systems: reliability, scalability, and maintainability.


**2、[資安駭客親自解答網友疑問！Google 是史上最強駭客工具？曾靠假證件攻破銀行機房](https://www.youtube.com/watch?v=CmcTKacenIM)**

GQ invited penetration tester Jayson E. Street to answer questions about his work, including what penetration testers do, what a typical penetration testing process looks like, and the differences between red teams and blue teams.

One point that stood out to me was Jayson’s explanation that the purpose of the red team (attackers) is to help the blue team (defenders) improve their security. Another interesting point was that hackers do not only attack over the internet. They may also use physical social engineering techniques, such as entering a company’s building with a fake ID badge or leaving a USB drive on an employee’s desk to see whether they will plug an unknown device into company computers.

The final explanation of what a firewall is was particularly relevant to my job. Jayson described a firewall as a very exclusive club: every packet trying to enter the network is inspected, and only those that satisfy a predefined set of rules are allowed through. I thought this analogy made the concept much easier to understand.


**3、Azure DNS**

I learned the basics of Azure DNS, particularly how to manage DNS record sets, configure different record types (such as A and CNAME records), and understand the purpose of TTL (Time to Live) in DNS propagation.

## What I Built

**1、LiveKit Server Deployment**

I attempted to deploy a LiveKit server on an Azure VM. The deployment is still in progress and not yet fully successful.

## Mistake I Made

**1、Incorrect Assumption About the Authentication Flow**

While trying to understand our company's authentication flow, I made an incorrect assumption. Since I saw a JWT being sent with requests to the AI server, I assumed the AI server was responsible for validating the request from the backend. Under that assumption, the AI server would also need access to the JWT signing secret.

After discussing it with the team, I realized the JWT is included in the HTTP request header, and the backend validates it before forwarding the authenticated request to the AI server.

During the discussion, I realized I had caused some confusion because I was reasoning from my assumptions rather than the actual implementation. The experience taught me an important lesson: always read the code before drawing conclusions.

## Things I Cared About

1、G2's reverse sweep over TES and TSW's miraculous 3–1 victory over TES. Why is it always TES?

2、Had a terrible game playing Ahri into Veigar. Should have taken Electrocute + Resolve for better survivability in the laning phase.

3、[Taylor Swift's Wedding](https://www.bbc.com/news/articles/cvg5zn58nj2o)