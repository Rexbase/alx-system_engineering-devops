[![Burning Bus](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/294/pQ9YzVY.gif)](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/294/pQ9YzVY.gif)

**Bookty Postmortem: Critical Platform Failure**

**Overview:**
Last week, the Bookty platform encountered a severe failure, leading to a universal 500 Error across all platform routes. This incident significantly disrupted services, impacting around 90% of our user base. The root cause was traced back to the malfunction of our master server, web-01.

**Timeline:**
- **Detection Time:** The issue was first noticed on Friday, November 13th, at 01:26 hours (West Africa Time) when Mr. Matthew, our Site Reliability Engineer, observed a noticeable lag in the master server's performance.
- **Actions Taken:**
  - The on-call engineers swiftly disconnected the malfunctioning master server (web-01) for detailed analysis.
  - During this period, all incoming requests were rerouted to the client server (web-02).
- **Resolution Time:** The problem was successfully resolved by Saturday, November 15th, at 18:46 hours (West Africa Time).

**Root Cause and Resolution:**
- **Root Cause:**
  - The Bookty platform operates on two Ubuntu cloud servers. The primary server, web-01, experienced a memory outage due to an overwhelming number of requests.
  - This was compounded by a previous testing scenario where the client server (web-02) was temporarily disconnected for testing but was not adequately reconnected to the load balancer.
- **Resolution:**
  - The master server underwent a temporary disconnection for memory clean-up.
  - It was then reconnected to the load balancer, and a round-robin algorithm was implemented to ensure an equitable distribution of requests between the master and client servers.

**Measures Against Future Problems:**
To mitigate the risk of similar incidents in the future, we have instituted the following measures:

- **Optimal Load Balancing Algorithm:**
  - Ensure the selection of the most suitable load balancing algorithm for your programs.
- **Continuous Server Monitoring:**
  - Implement regular monitoring of server health to promptly identify and address any anomalies.
- **Backup Servers:**
  - Maintain additional backup servers to prevent the program from going completely offline during unforeseen issues.

This postmortem outlines the key details of the platform failure, our response timeline, and the implemented measures to prevent such issues from reoccurring in the future.
