Containers are intended to be stateless and immutable. stateless stands for it cannot store any data, immutable means no
edit cannot be applied on running container.

What is Kubernetes Container Runtime ? 
Kubernetes itself cannot run container. It uses a runtime to manage, monitor, create container.
Supported Container Runtime: 
1. containerd
2. CRI-O
3. Other CRI Implementations

---------------
Container Hook:
---------------
is an event-driven trigger, which works on a specific time of it's lifecycle. 
1. PostStart Hook: After starting Pod/Container, this hook executes.
2. PreStop Hook: Before stopping, Hook will executes
3. StopSignal
Node drain Means Making Empty the node  to shutdow or maintenance

-----------------------
Container Hook Handler:
-----------------------
1. http (httpGet)
2. exec
3. sleep

