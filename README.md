- 👋 Hi, I’m @Geoff1948. I'm retired but have always been interested in electronics. I studied computer engineering in the 1970s but one or two things have changed since then. My daughter bought me an Arduino starter kit about three years ago and I've been learning ever since.

- 👀 I'm a keen gardener and have been deleloping a system for monitoring and controlling two watering systems for my garden. I have about 75 planters and pots and a single sensor could not represent different soil types, planter capacity or plant needs.  

My system uses six ESP32 Firebeetles in "Raingods" with inexpensive sensors to gather a wider sample of readings set in representative environments, each reporting to Thingspeak every three hours, two minutes apart. The seventh Firebeetle, the "Watergod" interprets the data and controls the valves, usually once per day. Six fields of a single Thingspeak channel register moisture percentage, the remaining two report the time period for which each of two valves is opened. A second Thingspeak channel records the battery levels of the six Raingods and two batteries in the Watergod.

The purpose of my system is to conserve water, replacing very reliable but inflexible timeswitches. The oldest Raingod has been functioning on three AA cells for over nine months and is expected to continue without battery replacement for at least a year. This is made possible by the extraordinarily low quiescent current taken by the ESP Firebeetle microcontroller (m/c) and by removing the internal voltage regulators in the sensors and powering them directly from a pin on the m/c. Initially I found that the Firebeetle remained asleep permanently if asked to sleep for more than half an hour but that problem has been overcome by using a series of defined variables. 

The internal Ultra Low Power clock is inaccurate but by waking the m/c briefly for a timecheck within a three hour period a correction can be applied that results in far greater accuracy when it is time to waken fully. I have forked an excellent Unix based sketch to obtain time but this came without DST adjustment. I have developed a perpetual calculator to compensate.

The cost of units has been kept low by using small LockNLock food boxes and cable glands to provide cases and exclude moisture from the m/cs and hot glue/shrink tubing to encapsulate the surface mount electronics on the sensors. The oldest of the sensors has been in use for nine months without malfunction but could be encapsulated in resin as a higher cost more reliable option.

Processing of the data stored on Thingspeak occupies quite a high percentage of the overall sketch. This might have been performed on Thingspeak itself using MathWorks and that is an option for those wishing to build upon and improve the project as presented. I have learned never to consider a project complete; it can always be improved. The system works for me at the moment but will be the subject of continuing development. At the end of the wires and pipes are living plants that can cease to live very easily; they will be my teachers, if I have got something wrong.

- 📫 How to reach me ...for first contact, write on my message board. Later maybe email.

<!---
Geoff1948/Geoff1948 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
