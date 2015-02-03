# KiWi.Docs
Documentation and notes for different modules

## KiWi.Deadbolt
#### Option 1
- ATMEGA328 Microcontroller programmed using Arduino
- LM400 Bluetooth dongle
- Power suppy TBD

##### Networks
- [x] Mobile <--> Deadbolt (Bluetooth)
- [x] Mobile <--> Server (Wifi or Bluetooth)
- [x] Server <--> Deadbolt (Bluetooth)

####To Sum Up
System is larger but easy to develop. Bluetooth interaction can get difficult at times. Auto-unlock feature will be genuinely based on Bluetooth distance (however this is not as reliable as one might hope). Lots of code help (NerdKits) and shouldn't be too hard to develop overall.

----

#### Option 2 (Optimized)
- Attiny2313 Microcontroller programmed using Arduino Uno
- XBee communication protocol
- Power suppy TBD

##### Networks
- [ ] Mobile <--> Deadbolt (No direct communcation!)
- [x] Mobile <--> Server (Wifi or Bluetooth)
- [x] Server <--> Deadbolt (XBee)

####To Sum Up
System is small, power efficient, and fast. Auto unlock feature WILL rely on location along with Wifi or Bluetooth. Personally, I don't know how to couple this specific microcontroller with XBee but I assume it is possible. We completely ditch the Bluetooth protocol. And ZigBee XBee is a more power efficient system according to papers like [Power Consumption of Wireless Protocols](http://research.microsoft.com/pubs/192688/IWS%202013%20wireless%20power%20consumption.pdf). This would be considered as an "actual" project because there is some research that needs to be done but nothing that cannot be completed within a couple of months.

----

####Miscellaneous
- Android platform should be first choice. It has many support utilites like BlueTerm which help development a lot more efficient. If we have time, we can consider IOS.
- With both options, the PCB board must be designed in advance. We can potentially ask for some contractor to design it for us granted our parts work as intended on a breadboard first.
- Power supply is a major concern. For a decent usage, 3 AA batteries can power the deadbolt (but we can reduce that down to one (1) if possible at least for the demo.
- NerdKit might be something we are interested in buying
- [Pinnochio](https://pinocc.io) is a slightly easier (and pricey system) which can be our failsafe. Watch a video [here](http://www.youtube.com/watch?v=TYj5OHki9ss). I feel that any idiot can make our system with this, so let's not do this.
- Development needs to be parallel. Each step below should be done together
  - Motor should be coupled with a simple board for now ensuring the power consumption, torque, etc. (Jesun + Caroline) (Finished by the end of Feb / start of March)
  - Microcontroller and communication protocol must be developed together with the server and Android app (Kapil + Mathew) (Finished by the end of Feb / start of March)
    - Will also require a PCB design (Start process at the beginning of March)
  - Power supply optimization (Xun + Nick) (By mid of March)
