[![Burning Bus](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/294/pQ9YzVY.gif)](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/294/pQ9YzVY.gif)

# BooktifuL Failure Report

## Overview
Last week, the BooktifuL platform experienced a critical failure, resulting in a 500 Error for all requests made on the platform routes. This incident caused a disruption in service, impacting approximately 90% of our users. The root cause was identified as the failure of our master server, web-01.

## Timeline
The error was first detected on Friday, February 24th, at 14:00 hours (West Africa Time) when our Site Reliability Engineer, Mr. Douglas, observed a significant lag in the master server's speed. Our on-call engineers promptly disconnected the malfunctioning master server, web-01, for a thorough system analysis. During this period, all incoming requests were redirected to the client server, web-02. The issue was successfully resolved by Saturday, February 25th, at 24:00 hours (West Africa Time).

## Root Cause and Resolution
The BooktifuL platform is hosted on two Ubuntu cloud servers. The master server, web-01, which was originally designated to handle all requests, experienced a memory outage due to an overwhelming number of requests. This was exacerbated by a previous test where the client server, web-02, was temporarily disconnected for testing purposes and was not properly reconnected to the load balancer afterward.

To address the issue, the master server underwent a temporary disconnection for memory clean-up. It was then reconnected to the load balancer, and a round-robin algorithm was configured to ensure an equal distribution of requests between the master and client servers.

## Measures Against Future Problems
To prevent similar issues in the future, we have implemented the following measures:

1. **Optimal Load Balancing Algorithm:** Ensure the selection of the most suitable load balancing algorithm for your programs.
2. **Continuous Server Monitoring:** Regularly monitor server health to promptly identify and address any anomalies.
3. **Backup Servers:** Maintain additional backup servers to prevent the program from going completely offline during unforeseen issues.
