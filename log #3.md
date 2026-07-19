
## What I Learned

**1、DDIA**

I've been reading Chapters 4 and 5 of DDIA. Chapter 4 introduced various ways of encoding and transmitting data between processes. It was somewhat abstract for me because JSON is the only data interchange format I have worked with before. I haven’t finished Chapter 5 yet, but I have learned about leader-based replication, including how replication improves scalability, fault tolerance, and latency, as well as the challenges introduced by asynchronous replication, such as replication lag and consistency issues.

**2、How JavaScript Closures Relate to React**

A **closure** is the combination of a function and references to its surrounding lexical environment. In other words, a closure allows a function to access variables from its outer scope, even after that scope has finished executing. In JavaScript, closures are created when functions are created.

React heavily relies on closures because each render creates new function instances that capture the state and props from that specific render. This behavior allows hooks such as `useEffect` and `useCallback` to access values from the render where they were created. However, it can also lead to a common problem called **stale closure**, where a function captures outdated state or props from an earlier render.

To avoid stale closure issues, developers need to ensure that functions always capture the latest values they depend on. This can be achieved by specifying correct **dependencies** in hooks, using **functional updates** when new state depends on previous state, or using **refs** when accessing mutable values that should stay up to date without triggering a re-render. In addition, **cleanup functions** help prevent outdated side effects from continuing after a component has changed or unmounted.

*References:*
- *[MDN - Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Closures)*
- *[Dan Abramov - A Complete Guide to useEffect](https://overreacted.io/a-complete-guide-to-useeffect/)*
- *[Stale Closures Impact on React Components](https://www.palo-it.com/en/blog/stale-closures-impact-on-react-components)*

## What I Built

**1、Built React tests with Vitest, React Testing Library, and TypeScript**

When writing tests, I always keep one question in mind: can these tests help me ensure that the existing functionality remains unchanged during refactoring? Writing tests also helps me better understand and improve the old, messy code I wrote before. By adding test coverage first, I can refactor with more confidence and verify that my changes do not introduce regressions.

**2、Fixed the Meta Quest connection problem**

It was difficult to locate the issue because I was not familiar with Meta Quest. Initially, I suspected it was a network or firewall problem. However, after running the WebRTC connection test on Meta Quest using [Connection Tester](https://livekit.com/webrtc/connection-test), I confirmed that the issue was not related to network connectivity.

My coworker suggested that the issue might be related to the proxy configuration. I checked the proxy logs and found the error `tls: unknown certificate authority`. After further investigation, I discovered that Meta Quest did not trust the SSL certificate issued by Let's Encrypt. I replaced the certificate with one issued by ZeroSSL, which resolved the connection issue.

## Things I Cared About

1、Bought T1 Galio and T1 Seraphine. T1 Seraphine looks so pretty.

2、[麥當勞「FIFA世界盃餐」登場！美墨莎莎醬系列、芒果可口可樂®氣泡飲，金黃地瓜條回歸](https://www.beauty321.com/post/72629)