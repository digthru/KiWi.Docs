#####looking into other, similar products is good.
We understand. Other products have their fair share of issues like connectivity and battery life. We hope to try different techniques i.e. ditching Bluetooth to learn from their mistakes and potentially develop a competetive product.

#####temperature range seems extreme? electronics surviving in a 100+ Celsius environment is very difficult. Did you mix up C and F temperatures? For reference, ordinary 63/37 solder melts at 183C
Thank you for catching this. We will reconsider this and it seems like we forgot to change the units to Farenheight when we normalized measurements before submitting the report.

#####motor specially made for the Arduino?


#####Is an arduino library really needed for XBEE modules? They’re fairly easy to use directly, in either transparent/AT mode or infrastructure mode. The Digi XCTU utility can be used to initially configure the modules
With our initial research, there was better online support which is why we inclined to use Arduino. Additionally, one of our major concerns is working with the Raspberry Pi and XBee modules. We are still not 100% sure on how to handle this which is why we decided to pursue Arduino. We will definitely research more into what you said and see what we can do!

#####how is the proximity of the smartphone to the door lock detected if there is no Bluetooth used?
We use GPS location of the phone in comparison to the deadbolt which is collected during calibration phase while setting up the lock through the mobile application. Apologize for the confusion in the paper.

#####Wifi GeoFencing? so when the user's phone is connected to the local wifi network, it assumes they're home?
The Raspberry PI NEEDS wifi all the time - atleast during our MVP build. The mobile app will communicate with when it is within the "geo-fence." The raspberry pi will filter and issue all user commands sent through the mobile device and into the XBee connected lock. In future we will use Bluetooth which can be used in the event of an Internet failure. In the event of a power failure, you can always use a physical key.

#####Where is the web app hosted? I assume the RasPI is acting as a web server here.
Similar to Chromecast! We will rely on port forwarding to enable access around the world. In reality, there will be two (2) web application in use; however, we have only documented one (1) for simplifying the report. The Rasbperry PI will log it's data on the KiWi servers and maintain web socket connection with us during all times! This way users can control the system from anywhere in the world. During our MVP phase, we will use Heroku to run the KiWi webserver on the NodeJS framework.

#####How is the communication between the base station and the lock unit secured?
We are still figuring this out. Any ideas would be great!

#####How are user connections to the web application (or the communications from the app to the base station) secured?
Basic stuff like HTTPS encryption. TBH, our MVP doesn't look like it will not have any state-of-the-art security.

#####What about users that will want to use multiple locks?
This is an issue. Currently, we will provide multiple base stations and multiple deadbolt locks. Obviously, most users would only want to have one but for our MVP we will only focus on a singular scenario.

#####Why is only one XBEE purchased? Don't you need two of them for a link?
We had only purchased one (1) when we wrote that paper. Rest assured, we have two; one for the Arduino and another for the Raspberry Pi. :)

#####what sort of electronics are going to be used to drive the motor? H-bridge for a DC motor? Stepper driver and/or dual H-bridge for a stepper motor?
Good question. No answer yet. Caroline and Jesun are on it. We should get this going by end of this month hopefully.

#####will there be some limit switches such that the electronics will be able to detect the state of the deadbolt? What about when someone uses the physical key?
Yes. We will have a way to communicate any manual unlocks with the Raspberry Pi and finally the KiWi webserver.

#####Can the low battery state be detected (i.e., such that the user has a chance to change/charge batteries before the doorlock fails to work due to dead battery)?
For our MVP product, no we won't. But technically, we should be able to do it.

#####One option that can save some time and money would be to simply purchase some premade electronics project boxes (either diecast aluminum or ABS plastic) such as those from BUD or Hammond. Metal enclosures are a problem when internal antennas are used.
We will be considering this option as well. For now, we want to dream big!

#####Block diagram could use more detail
Thank you for your feedback. We will improve it for next time.

#####Group seems to have done better-than-usual research into other competing products and relevant standards
Thanks!
