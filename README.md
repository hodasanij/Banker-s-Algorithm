In this assignment, you will create a solution for the banker's algorithm project from section 8.6.3 (Banker’s Algorithm) in
the 10th edition of Silberschatz (Operating System Concepts), or the 8th or 9th ed. of Stallings (Operating Systems: Internals
and Design Principles). Your solution can be in either: C, C++, or Java. A partial, possible layout of your project in C++
and in Java is attached to the project description in Slack #general and in Titanium. The description of this algorithm is in
ch. 8 of Silberschatz, and in ch. 6 of Stallings.
Your simulation should contain the essentials of the Banker's Algorithm (see rubric at end of this assignment description),
namely, customers (threads) should make requests of the banker for a limited set of resources. The banker should check
whether the customer is exceeding the maximum number of resources he/she said it would ever request, and if there are
sufficient system resources, and if the request would put the system in an unsafe state.
To determine if the system would be in an unsafe state, the algorithm should attempt to grant the request, by increasing the
resources allocated to the given process, and by reducing the total resources still needed by it to satisfy the maximum
resources it needs. If there is a still a path of allocating resources and having them released that will satisfy all of the
processes that are running, then the system is in a safe state, and the request should be approved.
Only safe requests should be approved.
Once the request is approved, the state of the system (Allocated, Need matrices and Available vector) should be updated.
You can either have the customer make requests until they reach their maximum needed, then release all resources and exit.
Here is an example of the output from your program.
