ipdsb - cc liscensed db exchange of DNA and Seed Samples
ipdsb - distribiuted exchnage for all comunity seed banks 

Distribiution mechanism to peer freely between networks of networks of seed, spore and information exchanges
Crowdsource sequencing of DNA and builing DB of dna of all living beeings before they die out
>github for DNA




# see also:

## the idea
http://www.saatgutkampagne.org/PDF/Resilient_Seed_EN_web.pdf
http://www.diversifood.eu/wp-content/uploads/2018/07/2018-6-29-CSB-report-workshop.pdf
---
5.1 Objective „Conservation“ 50
5.2 Objective „Access and Availability“ 52
5.3 Objective „Sensitisation“ 53
5.4 Objective „Training and Capacity Building“ 54
5.5 Objective „Sustainable Use“ 55
5.6 Objective „Advocacy and legal advice“ 56


## network - nodes
http://www.bgci.org/policy/ipen/
http://www.alpineseedconservation.eu/index.php/category/news/


from http://www.alpineseedconservation.eu/index.php/aims/
---
* Make high quality seed material available for conservation, research and restoration.
* Improve knowledge of the ecology of target species through specific research projects.
* Develop a network for seed conservation and research in the European Alps, fostering collaboration, development of new scientists, and expanding knowledge on key ecological species...


## similar

* https://eol.org/
* http://tolweb.org
* https://en.wikipedia.org/wiki/Tree_of_life_(biology)
* https://en.wikipedia.org/wiki/Wikispecies
* https://opentreeoflife.github.io/
* https://tree.opentreeoflife.org/opentree/argus/opentree10.4@ott93302
* https://en.wikipedia.org/wiki/Encyclopedia_of_Life
* later: https://en.wikipedia.org/wiki/ARKive
* https://en.wikipedia.org/wiki/Integrated_Taxonomic_Information_System

* https://upload.wikimedia.org/wikipedia/commons/9/98/A_Novel_Representation_Of_The_Tree_Of_Life.png
https://www.ecologyandsociety.org/vol21/iss2/art13/

* https://github.com/kgryte/awesome-peer-to-peer

distribiuted via https://hpbn.co/
http://hintjens.com/blog:32

* start of as federated wiki
* become transition to distribiuted model


## technical

From hintjens.com/blog:32
---
Let's recap the requirements:
* The simplest possible solution that works. There are so many edge cases in ad-hoc networks that every extra feature or functionality becomes a risk.
* Supports ephemeral ports, so that we can run realistic simulations. If the only way to test is to use real devices, it becomes impossibly expensive and slow to run tests.
* No root access needed, it must run 100% in user space. We want to ship fully-packaged applications onto devices like mobile phones that we don't own and where root access isn't available.
* Invisible to system administrators, so we do not need their help to run our applications. Whatever technique we use should be friendly to the network and available by default.
* Zero configuration apart from installing the applications themselves. Asking the users to do any configuration is giving them an excuse to not use the applications.
* Fully portable to all modern operating systems. We can't assume we'll be running on any specific OS. We can't assume any support from the operating system except standard user-space networking. We can assume 0MQ and CZMQ are available.
* Friendly to WiFi networks with up to 100-150 participants. This means keeping messages small and being aware of how WiFi networks scale and how they break under pressure.
* Protocol-neutral, i.e., our beaconing should not impose any specific discovery protocol. I'll explain what this means a little later.
* Easy to re-implement in any given language. Sure, we have a nice C implementation, but if it takes too long to reimplement in another language, that excludes large chunks of the 0MQ community. So, again, simple.
* Fast response time. By this, I mean a new node should be visible to its peers in a very short time, a second or two at most. Networks change shape rapidly. It's OK to take longer, even 30 seconds, to realize a peer has disappeared.
