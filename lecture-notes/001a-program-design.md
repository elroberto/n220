# Program Design 

## Goal

* Functional Requirements
* Acceptance Criteria

## Technical Design

* Flow chart
* Data model diagrams
* Class diagrams
* Pseudocode

## Testing

* Test Driven Development
* Requirements Test Tracibility


### Functional Requirements

Synonymous with business requirements, functional requirements are generally driven from outside of the development team. This is quite different from how things will work in this course. Functional requirements are the goals of your program. When you have met a functional requirement, your program has met its goal. Often intertwined in functional requirements are gaps in existing functional processes. They are often written from the user's perspective. For example:

```
As an student of the course registration system, 
  I would like for the courses I am registered for to automatically drop onto my Google Calendar. 
```

### Acceptance Criteria

Acceptance Criteria (AC) evolves from functional requirements. It is the criteria by which you grade your program. Here we look at an example from the Functional Requirement given above:

```
Given a successful course registration for a student, 
  When the course is a scheduled course, 
  When the course is not an online course, 
  Then add the course to the student's calendar. 
```
  
Often AC is written in a Given/When/Then format as a standard of practice. There are actually tools that can automate the practice of converting AC to programming test cases. But that is out of scope for today's discussion. For now, just know that Functional Requirements inform AC, and AC informs your programming. 

### Flow Chart

Once you have created AC from Functional Requirements, technical design can begin. Typically a process flow chart is the first step in technical design. This flow chart maps the user and/or technical path through the software. Steps such as events, decisions, and conditions are all mapped out ahead of actual programming. 

### Data Model Diagrams

In a complex application, it is useful to have a data model diagram. This is a model of how data relates to other data. We will discuss more about data models later in the course. 

### Class Diagrams

When building your program, you will think a fair amount about class structure. How you structure code is important for the readability and maintainability of your program. 

### Test Driven Development

A popular method of programming is test-driven. That is, write your tests for your program first. The entire set of tests will fail at first, but then the writing your program is essentially a process of making your tests pass. If you do not practice test driven development, you at least begin to think about test structure early in your program's life. 

### Requirements Test Tracibility

Tests have a natural correlation to Requirements. In large programming shops, it is typical for there to be a mapping database between tests and requirements. This is to ensure that requirements are met once a certain set of tests are passed. 

### Pseudocode

Start expresssing your program in English prose. Don't use first or second person though, use a computational perspective. Here is an example of pseudo code for paper, rock, scissors assignment.

```
/*
Define Players
 */
//enter name of player 1
//define player 1
//enter name of player 1
//define player 2

/*
Define Throws
 */
//enter player 1 throws
//define player 1 throws
//enter player 2 throws
//define player 2 throws

/*
Handle Tie Case
 */
//if player 1 throws == player 2 throws, game is tie

/*
Handle Cases
 */
//if player 1 throws paper
	//if player 2 throws rock, player 1 wins
	//if player 2 throws scissors, player 2 wins

//if player 1 throws rock
	//if player 2 throws scissors, player 1 wins
	//if player 2 throws paper, player 2 wins

//if player 1 throws scissors
	//if player 2 throws rock, player 2 wins
	//if player 2 throws paper, player 1 wins

```
