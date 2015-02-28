<h1>Battery Report</h1>

<p>After reading Power Consumption Analysis of Bluetooth Low Energy, ZigBee and ANT Sensor Nodes in a Cyclic Sleep Scenario, 
I acquired an estimate of how long the different battery candidates would last, based on their research findings.</p>

<p>They tested a ZigBee device at various duty cycles, to determine the average current consumption. I based my graph on these findings, since 
the ZigBee's continuous use should be the main source of power drain.</p>

<p>For low power use, the battery life of AA batteries is 2850 mA/h, the battery life of AAA batteries is 1150 mA/h, and the battery life of C batteries
is 7800 mA/h.</p>

<p>In my graph, I show how the batteries should perform at duty cycles of 1%, 2.5%, and 5%.   I'm not exactly sure how our ZigBee will be configured, so I
could only provide estimates.</p>

<p><img src="http://i.imgur.com/RJUtgOi.png" alt="Batteries"></p>

<p>In addition to my previous findings, the AA battery has a larger energy to volume ratio than the other two batteries. I still believe 4 AA
batteries are the best choice.</p>

<p>References:</p>

<p><a href="http://research.microsoft.com/pubs/192688/IWS%202013%20wireless%20power%20consumption.pdf">Research Paper</a></p>
<p><a href="https://learn.adafruit.com/minty-boost/batteries">Battery Article</a></p>
