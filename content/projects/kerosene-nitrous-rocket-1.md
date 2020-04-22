+++
content_img_path = "/images/kerosene.jpg"
date = 2019-11-15T08:00:00Z
layout = "project"
subtitle = ""
thumb_img_path = "/images/kerosene.jpg"
title = "Kerosene/Nitrous Rocket"

+++
### Overview

The [Stanford Student Space Initiative](https://stanfordssi.org/) (SSI) is the school's largest project-based student group and comprises teams ranging from high altitude balloons to astrobiology. As part of the Olympus project, I participated in the development and testing of a 1.5 kN thrust liquid engine rocket. [Version 1](https://arc.aiaa.org/doi/10.2514/6.2019-4231) of the engine was designed, built and hot fired in 2018. When I joined the project, the team was focused on iterating the design and getting the rocket ready for the Intercollegiate Rocket Engineering Competition (IREC) and Friends of Amateur Rocketry (FAR) Mars Competition, both scheduled for summer 2020.

![](/images/lathe.jpg)

I began on this project by machining key components of the rocket that had been destroyed in a previous hot fire test anomaly. Once it was clear that IREC and FAR Mars would be postponed due to COVID-19, the team transitioned efforts to redesigning the engine. The goals of the redesign were to:

* Reduce weight
* Reduce cost
* Improve manufacturability (notice the chatter marks on the part pictured above) and make assembly easier
* Reduce time between tests for quicker design iterations
* Add a throttling feature

### Reducing Weight

As a competition rocket, every gram counts, and though the original design was optimized to be as light as possible, a lot was still unknown until after the hot fire tests, which provided real data to better characterize the rocket. The results highlighted parts that could be made even lighter, either through a change in geometrical design or material selection, or even removed altogether. For example, the original injector was manufactured through direct metal laser sintering of Inconel 718. This superalloy, chosen for its high strength and thermal properties, is also quite heavy. But perhaps we could achieve the same pressure and thermal loads through a different design, maybe with a creative trick like pairing a highly conductive metal with regenerative cooling.

![](/images/pyrovalves.jpg)

Another area that we realized had extra mass was the pyrovalve assembly (see the image above). The original design had extra height so that fittings could be threaded into it, but after switching to a face-seal we could make things shorter.

### Reducing Cost

This often went hand in hand with weight reduction--Inconel is one of the more expensive materials to 3D print--so the strategy here involved evaluating if we could change to cheaper metals while trying to also reduce overall part count.

### Improving Manufacturability

Many of the components that had been destroyed in the hot fire test anomaly proved difficult to machine again. A few of the parts had dimensions that were not matched well to the dimensions of the aluminum stock we could get, leading to a lot of time spent turning down diameters. Further, the requirement that the tanks needed to be hydrostatically tested to a safety factor of 2 (1300 psi) meant the threads had to be very tightly toleranced, which was difficult to accomplish on manual tools in the student machine shop.

All of this led to a brainstorming session in which we decided to combine a few of the components into a single, additively manufactured part and pursue a welded tank design. 

### Reducing Time Between Tests

I am a big proponent of iterative design

### Throttling