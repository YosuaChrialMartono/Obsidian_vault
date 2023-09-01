---
college, rpl, sem_5, 
---
#rpl #notes 
# Introduction to Software Engineering
---
## What is software
### What is a software
- **Instructions** : When executed will return desired outcomes
- **Data Structures** : Capable of manipulating information and data
- **Documentation** : Describes the operation and use of program
### Characteristics of Software
1. Software is developed or engineered
2. Most software is custom-built, although there are many industry that is moving towards component-based construction
3. Software doesn't "wear out" - it’s deteriorate
	1. Hardware failure rate depicted in a form of the “bathtub curve” 
	   ![[Pasted image 20230829132806.png]]
	2. Software failure rate depicted in a form of the “idealized curve”.
	   ![[Pasted image 20230829132832.png]]
4. Software application example
	- System software
		- os windows, etc
	- Application software 
	- Engineering/scientific software 
		- Matlab, octave, etc
	- Embedded software 
	- Product-line software 
	- WebApps (Web applications) 
		- Web development
	- AI software
		- chat gpt
### Information System
- Information System is a software, since it checked all the requirements for one. 
- But not all software are information system. 
- An IS for different organization has different features.

## What is software engineering
## Relationship Between Software Engineering and Computer Science
![[Pasted image 20230829133747.png]]

### Seminal Definition
the establishment and use of sound engineering principles in order to obtain economically software that is reliable and works efficiently on real machines.
### IEEE Definition
1. The application of a systematic, disciplined, quantifiable approach to the development, operation, and maintenance of software; that is, the application of engineering to software. 
2. The study of approaches as in (1).
### Solving Problem with Software Engineering

```
Existing problems related to a computer or existing computer system sometimes doesn't necessarily have the underlying problem that have something to do with computers. 
```

Therefore, we must understand ***the nature of these problems first***.
- Don't impose "ngoding" on every problem
- Solve the problem first and use "ngoding" if needed to solve it.

### Solving Problem with Software Engineering
1. Analyzing the problem
	- Break the problem to bite sized pieces
	- Understand and try to connect those pieces
2. Construct the solution that address the problem's various aspects
	- **Synthesis,** in this process we will put together a large structure from the pieces that we have broken down from the previous step
### A layered Technology

![[Pasted image 20230901204232.png]]

#### Process 
process layer is the **foundation**.
- the **glue** that holds the technology together
- **enables rational and timely development**
- **defines framework**
- forms the **basis for management control** of software project
- **establish the context** of :
	- **Technical methods** are applied
	- **Work products** are produced
	- **Milestones** are established
	- **Quality** is ensured
	- **Change** is properly managed

#### Methods
- Provide the **technical how-to's** for building software
- **Encompass a broad array of tasks** 
  (include communication, requirement analysis, design modeling, program construction, testing, and support)
- **Rely on a set of basic principles**, each govern an area of technology that includes modeling activities and other descriptive techniques.

#### Tools
- **Provide automated or semiautomated support** for the process and the methods

### Conclusion
```
Although it does seem enticing to start coding first but it is sometime more worth it in the long run to design the software first
```
## The Essence of Software Engineering Practice

### How to solve a problem according to George Pólya
#### 1. Understand the problem (communication and analysis). 
- **Who are the stakeholders?** 
  Stakeholders as in the people who has a say in your software
- **What are the unknowns?**
  What are needed (data, functions, features) to solve the problem
- **Can the problem be compartmentalized**
  Can it be broken down to more understandable pieces
- **Can the problem be represented graphically** 
  Analysis model? Graph to understand the problem better
#### 2. Plan a solution (modeling and software design).
- **Have you seen similar problem before**
  Can we see a pattern that is present in other solutions or programs that answers our problem
- **Has a similar problem been solved**
  If so, is it reusable
- **Can subproblems be define**
  Can we define a subproblems that we already have a solution to
- **Can you represent a solution in a manner that leads to effective implementation?**
  Can a design model be created
#### 3. Carry out the plan (code generation). 
- **Does the solution conform the plan**
  Are the source codes traceable to the design model we made
- **Is each component part of the solution provably correct?**
  Have we reviewed or better the design and code? Have we apply correctness proofs to the algorithm 
#### 4. Examine the result for accuracy (testing and quality assurance).
- **Is it possible to test each component part of the solution**
  Have we implemented a testing strategy to the program
- **Does the solution produce results that conform to the data, functions, and features that are required?**
  Have we validated the program based on the stakeholders requirements

## Focus
```
The cost effective development of highly quality software
- Sommervile
```


