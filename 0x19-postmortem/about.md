#0x19. Postmortem
This project is quite intriguing.

In the realm of software systems, encountering failures is inevitable, and these setbacks can arise from a multitude of factors: bugs, sudden surges in traffic, security vulnerabilities, hardware malfunctions, natural calamities, human errors, and the list goes on. However, failure is not a dead end; it's an opportunity for learning and improvement. Exceptional Software Engineers embrace failure as a stepping stone for growth, drawing insights from their mistakes to prevent their recurrence. While facing failure is acceptable, repeating the same mistakes is not.

A valuable tool frequently employed in the tech industry is the postmortem. Following any system outage, the responsible team(s) compile a summary with two primary objectives:

1. **Information Accessibility:** The postmortem serves as a comprehensive account of the outage's cause, ensuring easy access for other company employees. Given that outages can significantly impact a company, it is crucial for managers and executives to comprehend the events and anticipate their ramifications on workflow.

2. **Root Cause Analysis and Resolution:** The postmortem delves into the identification of the root cause(s) behind the outage, emphasizing the implementation of measures to rectify the issues at their core. This proactive approach aims to fortify the system against similar failures in the future.

In light of a previous web stack debugging project or a personal encounter with an outage, the task at hand necessitates the composition of a postmortem. This document becomes a narrative of the challenges faced, the lessons learned, and the strategies employed to reinforce the system's resilience.

#Requirements:
Issue Summary (that is often what executives will read) must contain:

duration of the outage with start and end times (including timezone)
what was the impact (what service was down/slow? What were user experiencing? How many % of the users were affected?)
what was the root cause
Timeline (format bullet point, format: time - keep it short, 1 or 2 sentences) must contain:

when was the issue detected
how was the issue detected (monitoring alert, an engineer noticed something, a customer complained…)
actions taken (what parts of the system were investigated, what were the assumption on the root cause of the issue)
misleading investigation/debugging paths that were taken
which team/individuals was the incident escalated to
how the incident was resolved
Root cause and resolution must contain:

explain in detail what was causing the issue
explain in detail how the issue was fixed
Corrective and preventative measures must contain:

what are the things that can be improved/fixed (broadly speaking)
a list of tasks to address the issue (be very specific, like a TODO, example: patch Nginx server, add monitoring on server memory…)
Be brief and straight to the point, between 400 to 600 words

#Resources
[Project Explained](https://medium.com/@gdnwstom/postmortem-web-stack-outage-incident-8575745ccecc)
