+++
tags = ["ux","development"]
categories = ["development","ux"]
date = "2012-05-01T00:00:00Z"
title = "Is Intuitive User Interface Design Actually Subjective"
keywords = ["development","ux","windows"]

+++

I have been using Microsoft Essentials as my antivirus program ever since it was released. I really like the clean and simple user interface and the small memory footprint. I also recommend it to everyone. However recently I noticed that I hadn’t run a system scan in a while and the Microsoft Essential icon had turned yellow. 

<!--more-->

When I opened Microsoft Essentials, the main window had a large yellow ‘Scan Now’ button. Since I hadn’t run a system scan for a while, I thought I should run a full scan instead of a quick scan. So I selected full scan from the scan options and then clicked the yellow ‘Scan Now’ button. What I expected to happen now was that Microsoft Essentials would start a full system scan, however what happened was a quick scan was started. This surprised me and at first I assumed that I had made a mistake. So after investigating this for a few weeks I realised that when you click the yellow ‘Scan Now’ button it always starts a quick scan regardless of what scan option was selected.

Initially I thought this wasn’t intuitive, but after thinking about it more I started to wonder, if actually intuitiveness was subjective. Would another user actually expect that the application would run a quick scan when they clicked on the yellow ‘Scan Now’ button regardless of the scan option selected? Is there enough of a distinction between the regular scan now section and high priority yellow ‘Scan Now’ button to explain the difference of scan types that will be executed?

If I was designing this process what I would do is check the scan type selected and run that particular scan. I agree that when a system scan hasn’t been run for a long time you would want to alert the user (large yellow button) and you would want the user to run a complete system scan. Running a quick system scan makes sense since it would take less time to complete and on a psychological level there is a higher probability that the scan would complete before the user decided to cancel it. I think this could be achieved by the fact that the quick scan is selected by default in the scan options section and if the user has made the decision to perform a full scan they expect it will take longer than usual.

I would be quite interested in what anyone else thinks.

Below are screenshots of my process:

1. Open Microsoft Essentials when the icon has turned yellow.

{{< figure src="/images/sc12.jpg" >}}

2. Main window opens with the large yellow ‘Scan Now’ button visible and the quick scan option is selected by default. I then select the full scan option and click the yellow ‘Scan Now’ button.

{{< figure src="/images/sc2.jpg" >}}
{{< figure src="/images/sc3.jpg" >}}

3. You notice that a quick scan has been started.

{{< figure src="/images/sc4.jpg" >}}

4. After cancelling the scan I made sure the full scan option was selected and then clicked on the regular scan now button. This time a full scan is started.

{{< figure src="/images/sc5.jpg" >}}
{{< figure src="/images/sc6.jpg" >}}