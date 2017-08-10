+++
tags = ["book-review","development"]
categories = ["books"]
date = "2017-08-10T21:30:00Z"
title = "Review - Refactoring - Improving the design of existing code - Part 2"
keywords = ["refactoring", "development", "software", "book"]

+++

### Chapter 2

### Goals of refactoring
* Refactoring code makes a code base easier to understand and modify.

* Refactoring does not change observable the observable behaviour of the software.

<!--more-->

### Refactoring improves design
* Poorly designed code adds complexity and increase the number of lines of code required to achieve the same functionality. An important aspect of improving design is to eliminate duplicate code. Reducing the number of lines of code helps in future modification.

* Code should easily communicate its purpose.

* Refactoring helps achieve robust and scalable code

* Good design is vital for agile and fast software development. Teams can progress with a poorly designed code base for a period but eventually it catches up to the team and slows them down

* Refactoring should be done in short bursts instead of large chunks. Follow the boy scout rule and leave code that you have touched in a better state.

### Refactoring problem areas
* Databases are often difficult to refactor without causing major outages for a business or without writing extra code to work around refactored areas so to maintain existing behaviour.

* Poorly designed interfaces are difficult to change, since the team might not have access to all code bases that implement the interface.
