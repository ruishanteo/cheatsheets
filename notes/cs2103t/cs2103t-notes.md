# CS2103T Notes

-   [CS2103T Notes](#cs2103t-notes)
-   [Java](#java)
    -   [Varargs](#varargs)
-   [Programming Paradigm](#programming-paradigm)
    -   [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)
-   [Requirements](#requirements)
    -   [Non-functional requirements](#non-functional-requirements)
    -   [Quality of requirements](#quality-of-requirements)
    -   [Gathering requirements](#gathering-requirements)
    -   [Specifying Requirements](#specifying-requirements)
-   [Design](#design)
    -   [Design Fundamentals](#design-fundamentals)
    -   [Modeling](#modeling)
    -   [Design Patterns](#design-patterns)
        -   [Singleton Pattern](#singleton-pattern)
        -   [Abstraction Occurrence Pattern](#abstraction-occurrence-pattern)
        -   [Facade Pattern](#facade-pattern)
        -   [Command Pattern](#command-pattern)
        -   [Model View Controller (MVC) Pattern](#model-view-controller-mvc-pattern)
        -   [Observer Pattern](#observer-pattern)
    -   [Design Approaches](#design-approaches)
-   [Principles](#principles)
    -   [`S`ingle Responsibility Principle](#single-responsibility-principle)
    -   [`O`pen-Closed Principle](#open-closed-principle)
    -   [`L`iskov Substitution Principle](#liskov-substitution-principle)
    -   [`I`nterface Segregation Principle](#interface-segregation-principle)
    -   [`D`ependency Inversion Principle](#dependency-inversion-principle)
    -   [Separation of Concerns Principle](#separation-of-concerns-principle)
    -   [Law of Demeter](#law-of-demeter)
    -   [YAGNI Principle](#yagni-principle)
    -   [DRY Principle](#dry-principle)
    -   [Brooks' Law](#brooks-law)
-   [UML](#uml)
    -   [Class Diagrams](#class-diagrams)
        -   [Notation — Class Diagrams](#notation--class-diagrams)
        -   [Associations — Class Diagrams](#associations--class-diagrams)
            -   [Navigability](#navigability)
            -   [Multiplicity](#multiplicity)
            -   [Dependencies](#dependencies)
            -   [Composition (Has-A)](#composition-has-a)
            -   [Aggregation](#aggregation)
            -   [Inheritance (Is-A)](#inheritance-is-a)
    -   [Objects Diagrams](#objects-diagrams)
        -   [Notation — Objects Diagrams](#notation--objects-diagrams)
    -   [Sequence Diagrams](#sequence-diagrams)
        -   [Notation — Sequence Diagrams](#notation--sequence-diagrams)
    -   [OODM](#oodm)
    -   [Activity Diagrams](#activity-diagrams)
        -   [Notation — Activity Diagrams](#notation--activity-diagrams)
-   [Project Management](#project-management)
    -   [Revision Control](#revision-control)
    -   [Project Planning](#project-planning)
        -   [Work Breakdown Structure](#work-breakdown-structure)
        -   [Milestones](#milestones)
        -   [Buffers](#buffers)
        -   [Issue Trackers](#issue-trackers)
        -   [GANTT Charts](#gantt-charts)
        -   [PERT Charts](#pert-charts)
    -   [SDLC Process Models](#sdlc-process-models)
        -   [Sequential Models](#sequential-models)
        -   [Iterative Models](#iterative-models)
        -   [Agile Models](#agile-models)
            -   [XP](#xp)
            -   [Scrum](#scrum)
            -   [Unified Process](#unified-process)
        -   [CMMI](#cmmi)
-   [Coding Standards](#coding-standards)
    -   [Naming](#naming)
    -   [Layout](#layout)
    -   [Statements](#statements)
    -   [Classes and interfaces](#classes-and-interfaces)
    -   [Methods](#methods)
    -   [Types](#types)
    -   [Variables](#variables)
    -   [Loops](#loops)
    -   [Conditionals](#conditionals)
    -   [Comments](#comments)
-   [Implementation](#implementation)
    -   [Coding Quality](#coding-quality)
    -   [Documentation](#documentation)
        -   [Types](#types-1)
        -   [Guidelines](#guidelines)
    -   [Error Handling](#error-handling)
    -   [Reuse](#reuse)
-   [Quality Assurance](#quality-assurance)
    -   [Code Reviews](#code-reviews)
    -   [Static Analysis](#static-analysis)
    -   [Formal Verification](#formal-verification)
-   [Test Case Design](#test-case-design)
-   [Testing](#testing)
    -   [Regression Testing](#regression-testing)
    -   [Developer Testing](#developer-testing)
    -   [Unit Testing](#unit-testing)
    -   [Integration Testing](#integration-testing)
    -   [System Testing](#system-testing)
    -   [Alpha and Beta Testing](#alpha-and-beta-testing)
    -   [Dogfooding](#dogfooding)
    -   [Exploratory and Scripted Testing](#exploratory-and-scripted-testing)
    -   [User Acceptance Testing](#user-acceptance-testing)
    -   [Test Automation Testing](#test-automation-testing)

# Java

## Varargs

Syntactic sugar type feature that allows writing a method that can take a variable number of arguments.

```java
public static void search(String ... keywords){
      // method body
}
```

# Programming Paradigm

Guides programmers to analyse programmig problems ad structure programmig solutions in a specific way

## Object-Oriented Programming (OOP)

-   Views the world as a network of interacting objects
-   Tries to create a similar object network inside the computer's memory so that a similar result can be achieved programmtically

# Requirements

-   A software requirement specifies a need to be fulfilled by the software product.
-   A software project may be
    -   Brownfield project i.e., develop a product to replace/update an existing software product
    -   Greenfield project i.e., develop a totally new system from scratch
-   Requirements come from stakeholders
-   Requirements can be divided into:
    -   Functional requirements specify what the system should do
    -   Non-functional requirements specify the constraints under which the system is developed and operated

## Non-functional requirements

Specify the constraints under which the system is developed and operated

-   NFRs are easier to miss
-   Sometimes NFRs are critical to the success of the software

## Quality of requirements

-   Characteristics of well-defined requirements:

    -   Unambiguous
    -   Testable (verifiable)
    -   Clear (concise, terse, simple, precise)
    -   Correct
    -   Understandable
    -   Feasible (realistic, possible)
    -   Independent
    -   Atomic
    -   Necessary
    -   Implementation-free (i.e. abstract)

-   Set of requirements as a whole should be:
    -   Consistent
    -   Non-redundant
    -   Complete

## Gathering requirements

-   Brainstorming session
    -   No "bad" ideas (aim is to generate ideas; not to validate them)
-   Product surveys
    -   Studying existing products can unearth shortcomings of existing solutions that can be addressed by a new product
-   Observation
    -   Observing users in their natural work environment can uncover product requirements
-   User surveys
    -   Surveys can be used to solicit responses and opinions from a large number of stakeholders regarding a current product or a new product
-   Interviews
    -   Interviewing stakeholders and domain experts can produce useful information about project requirements
-   Focus groups
    -   Focus groups are a kind of informal interview within an interactive group setting
-   Prototyping
    -   A prototype is a mock up, a scaled down version, or a partial system constructed
        -   to get users feedback
        -   to validate a technical concept (a "proof-of-concept" prototype)
        -   to give a preview of what is to come, or to compare multiple alternatives on a small scale before committing fully to one alternative
        -   for early field-testing under controlled conditions

## Specifying Requirements

-   Feature list

    -   A list of features of a product grouped according to some criteria such as aspect, priority, order of delivery, etc

-   User stories

    -   Short, simple descriptions of a feature told from the perspective of the person who desires the new capability, usually a user or customer of the system
    -   Format: As a `{user type/role} I can {function} so that {benefit}`
    -   `{benefit}` can be omitted if it is obvious
    -   Can:
        -   Add more characteristics to the `{user role}`, e.g. As a **forgetful** user, ...
        -   Write user stories at various levels (epic/theme)
        -   Add conditions of satisfaction to a user story
        -   Include:
            -   Priority: how important the user story is
            -   Size: the estimated effort to implement the user story
            -   Urgency: how soon the feature is needed
    -   Convenient for scoping, estimation, and scheduling
    -   Less details compared to traditional requirements specifications
    -   Captures non-functional requirements too because even NFRs must benefit some stakeholder
    -   Handy for recording requirements during early stages of requirements gathering

-   Use cases

    -   Set of sequences of actions, including variants, that a system performs to yield an observable result of value to an actor
    -   Describes an interaction between the user and the system for a specific functionality of the system
    -   Only externally visible behavior (omit UI details)
    -   **Actor**: An actor (in a use case) is a role played by a user.

        -   can be a human or another system.
        -   not part of the system; they reside outside the system.

    -   **Main Success Scenario (MSS)** describes the most straightforward interaction for a given use case, which assumes that nothing goes wrong
    -   **Extensions** are "add-on"s to the MSS that describe exceptional/alternative flow of events

-   Glossary

    -   Serves to ensure that all stakeholders have a common understanding of the noteworthy terms, abbreviations, acronyms etc

-   Supplementary requirements
    -   This section can be used to capture requirements that do not fit elsewhere
    -   Typically, this is where most Non-Functional Requirements will be listed

# Design

## Design Fundamentals

-   **Abstraction**

    -   Data abstraction: abstracting away the lower level data items and thinking in terms of bigger entities
    -   Control abstraction: abstracting away details of the actual control flow to focus on tasks at a higher level

-   **Coupling**
    -   Coupling is a measure of the degree of dependence between components, classes, methods, etc. Low coupling indicates that a component is less dependent on other components
    -   High coupling is discouraged: maintenance, integration, testing and reuse of module is harder.
    -   Types: content, common/ global, data, external, subclass, temporal

## Modeling

-   A model provides a simpler view of a complex entity because a model captures only a selected aspect. This omission of some aspects implies models are abstractions.
-   Multiple models of the same entity may be needed to capture it fully.
-   Models can be used as a blueprint for creating software.

## Design Patterns

-   An elegant reusable solution to a commonly recurring problem within a given context in software design
-   Common format to describe a pattern:

    -   Context: The situation or scenario where the design problem is encountered
    -   Problem: The main difficulty to be resolved
    -   Solution: The core of the solution. It is important to note that the solution presented only includes the most general details, which may need further refinement for a specific context
    -   Anti-patterns (optional): Commonly used solutions, which are usually incorrect and/or inferior to the Design Pattern.
    -   Consequences (optional): Identifying the pros and cons of applying the pattern
    -   Other useful information (optional): Code examples, known uses, other related patterns, etc

-   23 Design Patterns divided into 3 categories:
    -   Creational: About object creation. They separate the operation of an application from how its objects are created.
        -   Abstract Factory, Builder, Factory Method, Prototype, **Singleton**
    -   Structural: About the composition of objects into larger structures while catering for future extension in structure.
        -   Adapter, Bridge, Composite, Decorator, **Facade**, Flyweight, Proxy
    -   Behavioral: Defining how objects interact and how responsibility is distributed among them.
        -   Chain of Responsibility, **Command**, Interpreter, Template Method, Iterator, Mediator, Memento, **Observer**, State, Strategy, Visitor

### Singleton Pattern

-   When to use:

    -   Requires only one instance of a class
    -   There is a risk of creating multiple objects by mistake
    -   Creating such multiple objects has real negative consequences

-   How to use:

    -   Private constructor with a public class-level method to access the single instance
    -   Optional `<<Singleton>>` UML stereotype to indicate role

![Singleton Pattern UML](https://nus-cs2103-ay2324s1.github.io/website/book/designPatterns/singleton/what/images/singleton.png)

-   Pros:
    -   Easy to apply
    -   Effective in achieving its goal with minimal extra work
    -   Provides an easy way to access the singleton object from anywhere in the code base
-   Cons:
    -   Acts like a global variable that increases coupling across the code base
    -   In testing, its difficult to replace Singleton objects with stubs (static methods cannot be overridden).
    -   In testing, singleton objects carry data from one test to another

### Abstraction Occurrence Pattern

-   When to use:

    -   Group of similar entities with common information
    -   Also differing in significant ways

-   How to use:
    -   Split entity into 2 classes
    -   1 object for common information (`Abstraction`) and many for unique information (`Occurrence`)

![Abstraction Occurrence Pattern UML](https://nus-cs2103-ay2324s1.github.io/website/book/designPatterns/abstractionOccurrence/what/images/abstractionOccurrence.png)

### Facade Pattern

-   When to use:

    -   Components need to access functionality deep inside other components.

-   How to use:
    -   Create a Facade class that sits between users of component and component internals
    -   All access to the component happens through the `Facade` class

![Facade Pattern UML](https://nus-cs2103-ay2324s1.github.io/website/book/designPatterns/facade/what/images/textLibraryBook.png)

### Command Pattern

-   When to use:

    -   Have a system is required to execute a number of commands
    -   Each doing a different task

-   How to use:
    -   Create a general `Command` object such that it can be used without knowing the exact type of command (using polymorphism)
    -   Example: Command interface in AB3 where all Commands implement this interface and have an `execute` method

![Command Pattern UML](https://nus-cs2103-ay2324s1.github.io/website/book/designPatterns/command/what/images/clientInvoker.png)

### Model View Controller (MVC) Pattern

-   When to use:

    -   Support storage/retrieval of information
    -   Displaying of information to the user (often via multiple UIs having different formats)
    -   Changing stored information based on external inputs

-   How to use:
    -   Split the data, presentation and control logic into 3 parts:
        -   View: Displays data, interacts with the user, and pulls data from the model if necessary.
        -   Controller: Detects UI events such as mouse clicks and button pushes, and takes follow up action. Updates/changes the model/view when necessary.
        -   Model: Stores and maintains data. Updates the view if necessary.

![MVC Pattern](https://nus-cs2103-ay2324s1.github.io/website/book/designPatterns/modelViewController/what/images/sequenceDiagram.png)

-   In a simple UI where there is only one view, Controller and View can be combined as one class.

### Observer Pattern

-   When to use:

    -   An object (possibly more than one) is needs to be notified when a change happens to another object

-   How to use:
    -   Force the communication through an interface known to both parties
    -   Have all observers implement an Observer interface
    -   Add all observers to the observee's observer list
    -   When there is an update, notify all added observers

![Observer pattern UML](https://nus-cs2103-ay2324s1.github.io/website/book/designPatterns/observer/what/images/observableInterfaceDiagram.png)

## Design Approaches

-   Top-down: Design the high-level design first and flesh out the lower levels later
    -   Useful when designing big and novel systems where the high-level design needs to be stable before lower levels can be designed
-   Bottom-up: Design lower level components first and put them together to create the higher-level systems later.
    -   Not usually scalable for bigger systems.
    -   One instance where this approach might work is when designing a variation of an existing system or re-purposing existing components to build a new system
-   Mix: Design the top levels using the top-down approach but switch to a bottom-up approach when designing the bottom levels
-   Agile: Emergent and not defined up front
    -   Overall system design will emerge over time, evolving to fulfill new requirements and take advantage of new technologies as appropriate
    -   Just enough initial architectural modeling at the very beginning of a project to get your team going
    -   Does not produce a fully documented set of models in place before you may begin coding

# Principles

## `S`ingle Responsibility Principle

-   Definition: A class should have one, and only one, reason to change

-   If a class has only one responsibility, it needs to change only when there is a change to that responsibility
-   Good way of identifying classes during the design phase

## `O`pen-Closed Principle

-   Definition: A module should be open for extension but closed for modification. That is, modules should be written so that they can be extended, without requiring them to be modified

-   Aims to make a code entity easy to adapt and reuse without needing to modify the code entity itself
-   Separating the specification (i.e. interface) of a module from its implementation

## `L`iskov Substitution Principle

-   Definition: Derived classes must be substitutable for their base classes

-   Subclass should not be more restrictive than the behavior specified by the superclass
-   LSP is not followed when substituting a subclass object for a superclass object breaks the functionality of the code

## `I`nterface Segregation Principle

-   Definition: No client should be forced to depend on methods it does not use

-   Can depend on an interface with just the methods it need, instead of the entire class

## `D`ependency Inversion Principle

-   Definition:
    -   High-level modules should not depend on low-level modules. Both should depend on abstractions
    -   Abstractions should not depend on details. Details should depend on abstractions

## Separation of Concerns Principle

-   Definition:

    -   To achieve better modularity, separate the code into distinct sections, such that each section addresses a separate concern
    -   A concern is a set of information that affects the code of a computer program

-   Reduces functional overlaps
-   Limits ripple effect when changes are introduced to a specific part of system
-   Can be applied at the class level as well as higher levels
-   Lead to higher cohesion and lower coupling

## Law of Demeter

-   Definition:

    -   An object should have limited knowledge of another object
    -   An object should only interact with objects that are closely related to it

-   Aims to prevent objects from navigating the internal structures of other objects
-   Method `foo` of an object `obj` should invoke only the methods of the following kinds of objects:
    -   Object `obj` itself
    -   Objects passed as parameters of `foo`
    -   Objects created/instantiated in `foo` (directly or indirectly)
    -   Objects from the direct association of `obj`

## YAGNI Principle

-   Definition:
    -   You Aren't Gonna Need It!
    -   Do not add code simply because 'you might need it in the future'
-   Some capability you presume your software needs in the future should not be built now
-   Do not have perfect information about the future
-   The extra work might go to waste when some of your predictions fail to materialize

## DRY Principle

-   Definition:

    -   Don't Repeat Yourself
    -   Every piece of knowledge must have a single, unambiguous, authoritative representation within a system

-   Guards against the duplication of information
-   Examples of violations:
    -   Functionality being implemented twice even if the two implementations are different
    -   Value of a system-wide timeout being defined in multiple places

## Brooks' Law

-   Definition: Adding people to a late project will make it later

-   The additional communication overhead will outweigh the benefit of adding extra manpower, especially if done near a deadline

# UML

## Class Diagrams

-   Used to model class structures of an OO solution
-   Describe the structure (but not behaviour) of OOP solution

### Notation — Class Diagrams

-   Visibility: `+` for public | `-` for private | `#` for protected | `~` for package (static)
-   Class-level methods/ attributes are underlined
-   `<<interface>>`
-   `<<enumeration>>`
-   `{abstract}` or _abstract_
-   OK to omit:
    -   Methods

### Associations — Class Diagrams

-   Association roles appears on end that plays that role

#### Navigability

-   `Solid arrow`
-   The concept of which object in the association knows about the other object.
-   E.g. Navigability is from `Box` to `Rope`, `b` will have reference to `r` but not vice versa. One can navigate from `b` to `r` using `b`'s object reference of `r`.

#### Multiplicity

-   `0..X`
    -   Number of X is on end nearer X.
-   The aspect of an OOP solution that dictates how many objects take part in each association.

#### Dependencies

-   `Dotted line`
-   A need for one class to depend on another without having a direct association in the same direction.

#### Composition (Has-A)

-   `Shaded diamond`
-   Diamond is on the end of the whole.
-   A composition is an association that represents a strong whole-part relationship.
    -   When the whole is destroyed, parts are destroyed too (parts cannot exist without whole).
    -   Cannot be cyclical links.

#### Aggregation

-   `Non-shaded/hollow diamond`
-   Diamond is on the end of the container.
-   An aggregation is an association that represents a container-contained relationship.
    -   Similar to that of composition except the containee object can exist even after the container object is deleted.
    -   Weaker relationship than composition. Aggregation represents a container-contained relationship. It is a weaker relationship than composition.

#### Inheritance (Is-A)

-   `Triangle arrow` (inheriting class - class or interface - interface)
-   `Triangle arrow` with dotted line: implementing an interface
-   Does not matter whether the triangle is filled or empty
-   Points to parent class
-   Inheritance implies the derived class can be considered as a sub-type of the base class (and the base class is a super-type of the derived class), resulting in an is a relationship.

## Objects Diagrams

-   Used to model object structure of an OO solution
-   Multiple object diagrams can correspond to a single class diagram

### Notation — Objects Diagrams

-   Object names are underlined
-   If there is inheritance, show either parent class or child class (not both)
-   MUST omit:
    -   Methods
    -   Multiplicities
-   OK to omit:
    -   Object name
    -   Variable name/ value
    -   Attributes compartment (if not relevant)

## Sequence Diagrams

### Notation — Sequence Diagrams

-   Arrows representing method calls: solid lined arrows
-   Arrows representing method returns: dashed lined arrows
-   Class/object name is not underlined
-   Use an X at the end of the lifeline of an object to show its deletion
-   Self-invocation calls is denoated by an arrow from the bar to itself
-   Method calls to static methods are received by the class itself

    -   You can use `<<class>>` to show that a participant is the class itself

-   All frames should use a rectangle with a clip on the bottom-right corner
-   **loop** frame: indicate a loop
    -   loop [condition]
-   **alt** frame: indicate alternative paths
    -   alt [condition]
    -   No more than one alternative partitions be executed in an alt frame- **opt** frame: indicate optional paths
    -   opt [condition]
-   **ref** frame: allow a segment of the interaction to be omitted and shown as a separate sequence diagram
    -   ref diagram title
    -   sd diagram title
-   **par** frame: indicate parallel paths
    -   The corresponding Java implementation is likely to be multi-threaded- Keywords are `loop` (while), `opt` (if) and `alt` (if elseif)
-   OK to omit:
    -   Activation bar
    -   Return arrows
    -   Activation bar of self-invocation

## OODM

-   Similar to class diagram notation but must omit:
    -   methods
    -   navigability
-   Do not contain solution-specific classes (classes that do not exist in the problem domain e.g. DatabaseConnection)

## Activity Diagrams

-   Models workflows

### Notation — Activity Diagrams

-   **Action**: rounded corners rectangle
    -   Denotes a single step in an activity.
-   **Control flow**: arrow-head line
    -   Denotes the flow of control from one action to the next.
-   **Start node**: shaded circle
    -   Denotes the start of the activity
-   **End node**: inner shaded circle with with a surrounding circle
    -   Denotes the end of the activity
-   **Branch node**: diamond square with two [conditions]
    -   Denotes the start of alternate path.
    -   Exactly one of the guard conditions should be true.
-   **Merge node**: diamond square
    -   Denotes the end of alternative paths
-   **Fork node**: bar
    -   Denotes the start of concurrent flows of cotntrol.
-   **Join node**: bar
    -   Denotes the end of parallel paths
-   **Rake** : rake symbol
    -   Denotes that the action is described in another subsidiary activity diagram
-   **Swim lanes**: partition
    -   Denotes who is doing which action (also called swimlane diagrams)
-   OK to do:
    -   Multiple arrows can start from the same corner of a branch node
    -   Omit merge node if it there's no ambiguity
    -   Omit [Else] condition.

# Project Management

## Revision Control

-   Process of managing multiple versions of a piece of information
-   Will track the history and evolution of your project
-   Makes it easier for to collaborate
-   **Repository** is the database that stores the revision history.
-   **Using History**
    -   Tag a specific commit to identify
    -   To see what changed: `diff`
    -   To restore the state of the working directory at point in the past: `checkout` the commit
-   **Remote Repositories**
    -   `git clone` a repo to create a copy
    -   Original repo is referred to as `upstream` repo
    -   `git pull` from one repo to another
    -   `git push` new commits in one repo to another
    -   Fork is a remote copy of a remote repo
    -   Pull request is a mechanism for contributing code to a remote repo
-   **Branching** is the process of evolving multiple versions of the software in parallel.
    -   Merge conflicts happen when you try to merge two branches that had changed the same part of the code and the revision control software (RCS) cannot decide which changes to keep.
-   **Centralized RCS** uses a central remote repo that is shared by the team.
-   **Distributed RCS** allows multiple remote repos and pulling and pushing can be done among them in arbitrary ways.
-   **Forking flow**: the 'official' version of the software is kept in a remote repo designated as the 'main repo'. All team members fork the main repo and create pull requests from their fork to the main repo.
-   **Feature branch workflow** is similar to forking workflow except there are no forks.
-   **Centralized flow** is similar to the feature branch workflow except all changes are done in the master branch.

## Project Planning

### Work Breakdown Structure

-   Depicts information about tasks and their details in terms of subtasks
-   Can also include prerequisite tasks and effort estimates for each task
-   Effort is traditionally measured in man hour/day/month
-   All tasks should be well-defined

| Task ID | Task     | Estimated Effort | Prerequisite Task |
| ------- | -------- | ---------------- | ----------------- |
| A       | Analysis | 1 man hour       | -                 |
| B       | Design   | 2 man day        | A                 |

### Milestones

-   End of a stage which indicates significant progress
-   Should account for dependencies and priorities when deciding on the features to be delivered at a certain milestone
-   Each intermediate product release is a milestone

### Buffers

-   Time set aside to absorb unforeseen delays
-   Very important to include because effort/time estimations are notoriously hard
-   Do not inflate task estimates to create hidden buffers (have explicit buffers instead)
    -   Reason: With explicit buffers, it is easier to detect incorrect effort estimates which can serve as feedback to improve future estimates

### Issue Trackers

-   Issue trackers (sometimes called bug trackers) are commonly used to track task assignment and progress

### GANTT Charts

-   2-D bar-chart
-   Drawn as time vs tasks
-   Solid bar represents the main task (composed of a number of subtasks)
-   Grey bars represent subtasks
-   Diamond shape indicates an important deadline/deliverable/milestone

### PERT Charts

-   Program Evaluation Review Technique
-   Shows the order/sequence of tasks
-   Directed graph:
    -   Nodes or vertices capture the effort estimations of tasks
    -   Arrows depict the precedence between tasks
-   Helps determine the following:
    -   Order of tasks
    -   Which tasks can be done concurrently
    -   Shortest possible completion time
    -   Critical path (path where any delay can directly affect the project duration, hence it is important to ensure tasks on the critical path are completed on time)

## SDLC Process Models

-   Software development goes through different stages such as requirements, analysis, design, implementation and testing
-   Collectively known as the software development life cycle (SDLC)

### Sequential Models

-   Views software development as a linear process
-   Also called waterfall model
-   When one stage of the process is completed, it produces some artifacts to be used in the next stage
-   A strict sequential model project moves only in the forward direction

![Sequential Model](https://nus-cs2103-ay2324s1.github.io/website/book/processModels/introduction/sequentialModels/images/diagram.png)

-   Pros:
    -   Work well for a project that produces software to solve a well-understood problem
-   Cons:
    -   Real-world projects often tackle problems that are not well-understood at the beginning

### Iterative Models

-   Advocates producing the software by going through several iterations
-   Each iteration produces a new version of the product that builds on the version produced in previous iteration

![Iterative Model](https://nus-cs2103-ay2324s1.github.io/website/book/processModels/introduction/iterativeModels/images/diagram.png)

-   Breadth-first
    -   An iteration evolves all major components and all functionality areas in parallel
-   Depth-first
    -   An iteration focuses on fleshing out only some components or some functionality area.
    -   Early depth-first iterations might not produce a working product.
-   A project can be done as a mixture of breadth-first and depth-first iterations

### Agile Models

#### XP

-   Extreme programming
-   Stresses custoemr satisfaction
-   Aims to make develoeprs confidently respond to changing requirements (even late in life cycle)
-   Emphasizes teamwork
-   Improve in: communication, simplicity, feedback, respect and courage
-   Has a set of simple rules

#### Scrum

-   Scrum is a process skeleton that contains sets of practices and predefined roles. The main roles in Scrum are:
    -   The **Scrum Master**, who maintains the processes (typically in lieu of a project manager).
    -   The **Product Owner**, who represents the stakeholders and the business.
    -   The Team, a cross-functional group who do the actual analysis, design, implementation, testing, etc.
-   A Scrum project is divided into iterations called **Sprints**.
-   A key principle of Scrum is its recognition that during a project the customers can change their minds about what they want and need.
-   The daily scrum meeting is not used as a problem-solving or issue resolution meeting.
-   Issues that are raised are taken offline and usually dealt with by the relevant subgroup immediately after the meeting.
-   Members answer these questions
    -   What did you do yesterday?
    -   What will you do today?
    -   Are there any impediments in your way?

#### Unified Process

-   Flexible and customizable process model framework
-   Consists of four phases: inception, elaboration, construction and transition

| Phase        | Activities                                                                                                                                                                               | Typical Artifacts                                                      |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Inception    | Understand the problem and requirements<br>Communicate with customer<br>Plan the development effort                                                                                      | Basic use case model<br>Rough project plan<br>Project vision and scope |
| Elaboration  | Refine and expand requirements<br>Determine a high-level design                                                                                                                          | System architecture<br>Various design models<br>Prototype              |
| Construction | Major implementation effort to support the use cases identified<br>Design models are refined and fleshed out<br>Testing of all levels are carried out<br>Multiple releases of the system | Test cases of all levels<br>System release                             |
| Transition   | Ready the system for actual production use<br>Familiarize end users with the system                                                                                                      | Final system release<br>Instruction manual                             |

### CMMI

-   Capability Maturity Model Integration
-   Defines 5 maturity levels for a process (specifies criteria):
    -   Level 1: Initial
        -   Processes unpredictable, poorly controlled and reactive
    -   Level 2: Managed
        -   Processes characterised for projects and is often reactive
    -   Level 3: Defined
        -   Processes characterised for organisations and is proactive
    -   Level 4: Quantitatively Managed
        -   Processes measured and controlled
    -   Level 5: Optimizing
        -   Focus on process improvement

# Coding Standards

## Naming

-   Names representing packages should be in all lower case.
-   Class/ enum names must be nouns and written in PascalCase.
-   Variable names must be in camelCase.
-   Constant names must be in SCREAMING_SNAKE_CASE.
-   Names representing methods must be verbs and written in camelCase.
-   Abbreviation and acronyms should not be uppsercase when used as part of a name.
-   All names should be written in English.
-   Variables with a large scope should have long names, variables with a small scope can have short names.
-   Boolean variables/ methods should be named to sound like booleans.
-   Plural form should be used on names representing a collection of objects.
-   Iterator variables can be called i, j, k.
-   Associated constants should have a common prefix.

## Layout

-   Basic indentation should be 4 spaces.
-   Line length should be no longer than 120 characters.
-   Place line break to improve readability.
-   Use egyptian style brackets.
-   Method definitions should have the following form:
    ```
    public void someMethod() throws SomeException {
              ...
    }
    ```
-   if-else class of statemets should have the following form:
    ```
    if (condition) {
              statements;
    }
    ```
-   for statement should have the following form:
    ```
    for (initialization; condition; update) {
              statements;
    }
    ```
-   while statement should have the following form:
    ```
    while (condition) {
              statements;
    }
    ```
-   switch statement should have the following form:

    ```
    switch (condition) {

    case ABC:
              statements;
              //Fallthrough

    case DEF:
              statements;
              break;
    }
    ```

-   try-catch statement should have the following form:
    ```
    try {
              statements;
    } catch (Exception exception) {
              statements;
    }
    ```
-   White space within a statement
    -   Operators should be surrounded by a space character
    -   Java reserved words should be followed by a white space
    -   Commas should be followed by a white space
    -   Colons should be surrounded by white space when used as binary/ ternary operator
-   Logical units within a block should be separated by one blank line

## Statements

-   Put every class in a package
-   Put related classes in a single package
-   The ordering of import statements must be consistent
-   Imported classes should always be listed explicity (not \*)

## Classes and interfaces

-   Class/Interface documentation (Comments)
-   class or interface statement
-   Class (static) variables in the order public, protected, package (no access modifier), private
-   Instance variables in the order public, protected, package (no access modifier), private
-   Constructors
-   Methods (no specific order)

## Methods

-   Method modifiers should be given in the following order:

    `<access> static abstract synchronized <unusual> final native`

## Types

-   Array specifiers must be attached to the type not the variable

    `int[] a = new int[20];`

## Variables

-   Variables should be initialized where they are declared and they should be declared in the smallest scope possible.
-   Class variables should never be declared public.
-   Avoid unnecessary use of `this` with fields.

## Loops

-   Loop body should be wrapped by curly brackets irrespective of how many lines there are in the body.

## Conditionals

-   Conditional should be put on a separate line.
-   Single statement conditionals should still be wrapped by curly brackets.

## Comments

-   All comments should be written in English.
-   Write descriptive header commends for all public classes/ methods.
-   All non-trivial private methods should carry header comments.
-   Javadoc comments should have the following form:
    ```
    /**
        * Returns lateral location of the specified position.
        * If the position is unset, NaN is returned.
        *
        * @param x X coordinate of position.
        * @param y Y coordinate of position.
         * @param zone Zone of position.
        * @return Lateral location.
        * @throws IllegalArgumentException  If zone is <= 0.
        */
        public double computeLocation(double x, double y, int zone)
                      throws IllegalArgumentException {
               //...
        }
    ```
-   Comments should be indented relative to their position in the code.
    ```
    while (true) {
              // Do something
              something();
    }
    ```

# Implementation

## Coding Quality

-   Avoid long methods
-   Avoid deep nesting
-   Avoid complicated expressions
-   Avoid magic numbers
-   Make the code obvious
-   Structure code logically
-   Do not 'trip up' reader
    -   Avoid unused paramters in method signature
    -   Similar things that look different
    -   Different things that look similar
    -   Multiple statements in the same line
-   Practice KISSing
    -   Keep it simple, stupid
    -   Do not try to write 'clever' code
-   Avoid premature optimizations
-   SLAP hard
    -   Single Level of Abstraction Principle
    -   Avoid having multiple levels of abstraction within a code fragment
-   Make the happy path prominent
-   Naming:
    -   Use nouns for things and verbs for actions
    -   Use standard words
    -   Use name to explain
    -   Not too long, not too short
    -   Avoid misleading names

## Documentation

-   Developer-as-user: API documentaion or tutorial-style instructional documentation
-   Developer-as-maintainer: how a system or component is designed implemented and tested

### Types

-   Tutorials (learning-oriented)
-   How-to guides (goal-oriented)
-   Explanation (understanding-oriented)
-   Reference (information-oriented)

### Guidelines

-   Top-down, not bottom-up
    -   The reader can travel down a path she is interested in until she reaches the component she is interested to learn in-depth
-   Comprehensibility
    -   Use plenty of diagrams, examples, simple and direct explanations
-   Document minimally but sufficiently
    -   'just enough' developer documentation

## Error Handling

-   **Exceptions** are used to deal with 'unusual' but not entirely unexpected situations that the program might encounter at runtime.
    -   After a method throws an exception, the runtime system attempts to find something to handle it in the call stack.
-   **Assertions** are used to define assumptions about the program state so that the runtime can verify them.
    -   Assertions can be disabled without modifying the code.
        -   Java disables assertions by default.
    -   Assertions are used to define assumptions about the program state so that the runtime can verify them.
    -   Recommended that assertions be used liberally in the code.
-   **Logging** is the deliberate recording of certain information during a program execution for future reference.
-   **Defensive programming** is proactively eliminating any room for things to go wrong.
    -   Enforcing compulsory associations
    -   Enforcing 1-to-1 association
    -   Enforcing referential integrity (prevents case where A says B is X but B says B is Y)
-   **Design-by-contract approach** is an approach for designing software that requires defining formal, precise and verifiable interface specifications for software components.
    -   Code first checks if the preconditions have been met.

## Reuse

-   **API**: An Application Programming Interface (API) specifies the interface through which other programs can interact with a software component. It is a contract between the component and its clients.
-   **Library**: A library is a collection of modular code that is general and can be used by other programs.
-   **Frameworks**: A software framework is a reusable implementation of a software (or part thereof) providing generic functionality that can be selectively customized to produce a specific application.
    -   Some frameworks provide a complete implementation of a default behavior which makes them immediately usable. (e.g. Eclipse)
-   **Platforms**: A platform provides a runtime environment for applications.
-   **Cloud computing**: Cloud computing is the delivery of computing as a service over the network, rather than a product running on a local machine.
-   **Infrastructure as a service (IaaS)** delivers computer infrastructure as a service.
-   **Platform as a service (PaaS)** provides a platform on which developers can build applications.
-   **Software as a service (SaaS)** allows applications to be accessed over the network instead of installing them on a local machine.

# Quality Assurance

-   Quality Assurance = Validation + Verification

## Code Reviews

-   Systematic examination of code with the intention of finding where the code can be improved

-   Three types covered:

    -   PR reviews
    -   In pair programming
    -   Formal inspections

-   Advantages over testing:

    -   It can detect functionality defects as well as other problems such as coding standard violations.
    -   It can verify non-code artifacts and incomplete code.
    -   It does not require test drivers or stubs.

-   Disadvantages:
    -   It is a manual process and therefore, error prone.

## Static Analysis

-   Analysis of code without actually executing the code
-   Find useful info like:
    -   unused variables
    -   unhandled exceptions
    -   style errors
    -   statistics
-   Linters are a subset of static analyzers

## Formal Verification

-   Uses mathematical techniques to prove the correctness of a program
-   Advantages over testing:
    -   Prove the absence of errors (testing can only prove the presence of errors, not their absence)
-   Disadvantages:
    -   Only proves the compliance with the specification, but not the actual utility of the software
    -   Requires highly specialized notations and knowledge which makes it an expensive technique to administer (more commonly used in safety-critical software such as flight control systems)

# Test Case Design

-   **Postive test case**: is designed to produce valid behaviour.
-   **Negative test case**: is designed to produce an invalid behaviour.
-   **Black-box**: test cases are designed exclusively based on the SUT's specified external behaviour.
-   **White-box**: test cases are designed based on what is known about the SUT's implementation.
-   **Gray-box**: mix of both

-   **Equivalence partitions** (aka equivalence class): A group of test inputs that are likely to be processed by the SUT in the same way.
    -   Avoid testing too many inputs from one partition
    -   Ensure all partitions are tested
-   **Boundary value analysis** (BVA) is a test case design heuristic that is based on the observation that bugs often result from incorrect handling of boundaries of equivalence partitions.
    -   Choose 3 values to test: below, in and above boundary
-   **Combining test inputs**
    -   Testing all possible combinations is effective but not efficient
    -   Combination strategies:
        -   The all combinations strategy generates test cases for each unique combination of test inputs.
        -   The at least once strategy includes each test input at least once.
        -   The all pairs strategy creates test cases so that for any given pair of inputs, all combinations between them are tested.
    -   Heuristic: Each valid input at least once in a positive test case
    -   Heuristic: No more than one invalid input in a test case

# Testing

## Regression Testing

-   Regression testing is the re-testing of the software to detect regressions.
-   When you modify a system, the modification may result in some unintended and undesirable effects on the system. Such an effect is called a regression.

## Developer Testing

-   Developer testing is the testing done by the developers themselves as opposed to dedicated testers or end-users.
-   Early testing is better: earlier a bug is found, easier and cheaper to have it fixed.

## Unit Testing

-   Unit testing is testing individual units (methods, classes, subsystems) to ensure each piece works correctly.
-   Stubs: a stub has the same interface as the component it replaces, but its implementation is so simple that it is unlikely to have any bugs.
    -   Can isolate the SUT from its dependencies
    -   Typically these mimicked responses are hard-coded

## Integration Testing

-   Integration testing is testing whether different parts of the software work together as expected.
-   Not simply a case of repeating the unit test cases using the actual dependencies, but are additional test cases that focus on interactions between the parts.

-   Pure unit/ integration testing has one extra step than hybrid
-   Hybrid skips the steps that requires stubs

## System Testing

-   System testing is testing that takes the whole system and tests it against the system specification.
-   Based on specified external behaviour of the system
-   Includes testing against non-functional requirements:
    -   Usability, portability, performance, security, load, compatibility testing

## Alpha and Beta Testing

-   Alpha testing is performed by the users, under controlled conditions set by the software development team.
-   Beta testing is performed by a selected subset of target users of the system in their natural work setting.

## Dogfooding

-   Creators use their own product to test it.

## Exploratory and Scripted Testing

-   Scripted testing: first write a set of test cases based on the expected behavior of the SUT, and then perform testing based on that set of test cases.
-   Exploratory: Devise test cases on-the-fly, creating new test cases based on the results of the past test cases.
    -   Known as reactive testing, error guessing technique, attack-based testing and bug hunting

## User Acceptance Testing

-   User acceptance testing is testing the system to ensure it meets the user requirements.

---

| System Testing                                    | Acceptance Testing                                                         |
| ------------------------------------------------- | -------------------------------------------------------------------------- |
| Done against the system specifications            | Done against the requirements specification                                |
| Done by testers of the project team               | Done by a team that represents the customer                                |
| Done on the development environment or a test bed | Done on the deploymet site or on a close simulation of the deployment site |
| Both negative and positive test cases             | More focus on positive test cases                                          |

## Test Automation Testing

-   An automated test case can be run programmatically and the result of the test case (pass or fail) is determined programmatically.
-   **Automated testing of CLI apps**: A simple way to semi-automate testing of a CLI (Command Line Interface) app is by using input/output re-direction.
-   **Test automation using test drivers**: JUnit is a tool for automated testing of Java programs.
-   **Automated testing of GUIs**: testing tools like TestFX, Visual Studio, Selenium
-   **Test coverage**: Test coverage is a metric used to measure the extent to which testing exercises the code.
    -   Function/ method coverage: based on functions executed e.g., testing executed 90 out of 100 functions.
    -   Statement coverage: based on the number of lines of code executed e.g., testing executed 23k out of 25k LOC.
    -   Decision/branch coverage: based on the decision points exercised e.g., an if statement evaluated to both true and false with separate test cases during testing is considered 'covered'.
    -   Condition coverage: based on the boolean sub-expressions, each evaluated to both true and false with different test cases. Condition coverage is not the same as the decision coverage.
-   **Dependency injection**: Dependency injection is the process of 'injecting' objects to replace current dependencies with a different object.
    -   Often used to inject stubs to isolate the SUT from its dependencies so that it can be tested in isolation.
    -   Polymorphism can be used to implement dependency injection.
-   **Test-driven development (TDD)**: Advocates writing the tests before writing the SUT, while evolving functionality and tests in small increments.
