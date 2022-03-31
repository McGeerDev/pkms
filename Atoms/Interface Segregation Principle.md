202203310739

Status: #principle
Tags: [[Software Architecture]]


# Interface Segregation Principle
#### Or Interface Seperation Principle

ISP is like [[Microservices]] such that responsibility(Interface) is split up. If multiple users consume an interface then that interface should be split up so that each user isn't required to update and recompile their entire application because an unrelated part of the original interface changed. 

Basically consumed modules that contain baggage (Other dependant modules) are dangerous.
If something in the baggage breaks it could break the entire module and the system that consumes it. The ISP tries to fix this by forcing you to only consume what you use.


---
# References