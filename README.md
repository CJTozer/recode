# Philosophy

There are lots of resources out there to learn a new language using small, normally mathematical, problems.  But these usually don't cut to the meat of what it means to be a great coder.  They tend to focus on:
* Mathematics or logic problems - because these are easy to set up and test
* Single-function programs which serve a very simple purpose, without much infrastructure
* Writing one's own code, rather than using 3rd-party OSS

This project aims to provide something more "real".  That might suit you better, it might not!

## Outline

My initial thoughts are:
* I'm interested in teaching how to build a program that interacts with other systems
* Rather than having a `run -> read input file -> produce answer -> end`, I'd like to have a real-time process which is configured, receives requests, and has to communicate with other systems to function properly
* This still needs to be easy to test, so a well-defined API like OpenAPI would work well for specifying the interfaces

To achieve this, my idea is to:
* Have coders produce a Docker container which runs their program
* Test this using some Docker composition tool (TBD which one)
* Encourage debuggability - coders will need to look through their own logs to work out what's going wrong
* Use OpenAPI for the specification of the process, and of the other systems
* Combined, this allows significant flexibility in language choice, and allows the problems to build upon earlier foundations
* Further down the line, it may be that the coder has to produce several containers which talk to each other
* There will be testing focus on real-world scenarios - like one of the data sources being unavailable, or the process under test being restarted...
