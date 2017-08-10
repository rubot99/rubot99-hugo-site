+++
tags = ["book-review","development"]
categories = ["books"]
date = "2017-08-20:30:00Z"
title = "Review - Refactoring - Improving the design of existing code"
keywords = ["refactoring", "development", "software", "book"]

+++

I’m an avid listener of the CodingBlocks.Net podcasts and it’s been one of my go to podcasts for software development. I have especially enjoyed the podcasts where the presenters reviewed the Clean Code book by having a podcast per chapter where they discussed their individual thoughts. So I thought I would follow their idea and write blogs posts reviewing Martin Fowler’s book on Refactoring. This year I wanted to read a few software development books and write a few posts, so what better way to merge my two goals reading the book and writing posts for the sections/chapters 😉

<!--more-->

###Foreword + Preface + Chapter 1

The first section talks about the importance of designing software before you start implementation. Good design is no substitute for immediate implementation gratification. Putting coding first is a sure way of spiralling from engineering to code hacking. Poor design reduces the readability and maintainability of your code. It is said code is read and modified more frequently than it is written. Poorly designed code bases often suffer from copy and paste code rather than reusable modules. This all makes code difficult to maintain and increasing the chances of adding bugs. 

Controlled refactoring is the way to improve an existing code base that might be poorly designed or one that has accumulated cruft over time. Refactoring is not a magic bullet but also has risks involved. Any modification to a code base has the potential to introduce bugs.

One preliminary step you need to take before starting any refactoring is to have a comprehensive suite of tests. This ensures that existing functionality is not broken during the refactoring.

The second step is to decompose things into smaller parts and to refactor. It is difficult to refactor large parts but is more manageable to refactor smaller parts.

Renaming functions and variables are an important step. Good code should communicate its intent without the need of extra documentation. Readable code might initially seem less performant, but in the long run it will be easier to change. 
