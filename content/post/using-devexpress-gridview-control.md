+++
tags = ["devexpress","gridview","code","c#","development"]
categories = ["development","code","c#"]
date = "2011-08-05T00:00:00Z"
title = "Using Devexpress Gridview Control"
keywords = ["development","code","c#"]
+++

This is another post in my series of DevExpress controls that I use and like. In this post I will be looking at the ASPxGridView control. This control is one of my most used and favourite DevExpress controls. The functionality that you get straight out of the box is impressive to say the least. I’m able to add functionality that is extremely useful to the users with very little effort or code.

<!--more-->

The features that I like in the control are:

1. Default themes
2. Data sorting
3. Data grouping
4. Data editing
5. Colum re-arrangement

The features that I have listed are features that come straight out the box. I tend to normally bind the GridView to a list of business objects and either enable or disable the features through the control markup. I find these features really useful since I don’t need to write extra code on the application side nor do I have any additional views or stored procedures
on the database side. I should mention that depending on what you do with data editing you make need to handle row events.

The features that I like the best is the data grouping functionality and the reason for this is that it allows users to group on any column they need to. The first screen shot shows the default gridview without any grouping. The second screen shot shows what happens when the user groups on one of the columns and the third screen shot shows what happens when the grouping is on two different columns.

{{< figure src="/images/default3.png" title="Devexpress Gridview Control" >}}
{{< figure src="/images/groupontwocolumns1.png" title="Data Grouping example 1" >}}
{{< figure src="/images/groupononecolumn2.png" title="Data Grouping example 2" >}}
