# Step 5: Order a RileyLink

!!! danger "Time Estimate"
    - 15-20 minutes to read about the RileyLink and other radio-link options
    - 15 minutes to order a radio-link
    - 15-20 minutes to assemble the RileyLink (if you choose that radio-link)

!!! info "Summary"
    - Decide what kind of radio-link to buy
    - Order your radio link
    - If you choose Rileylink
        - Assemble the RileyLink

!!! warning "FAQs"
    - **Rileylink vs radio-link**: The Rileylink is the original design. Other DIY Loopers have created several other options.  A new section has been added to this page: [Radio-link Options](step5.md#radio-link-options).  All headers will continue using Rileylink in the name (because we don't want to mess up the links).  But gradually, radio-link will be used in the body of the pages - unless it is specific to Rileylink.
    - **"Do I need a radio-link?"** Yes. Loop will not work without a radio-link. Omnipod users will not be able to bolus from their looping pod without a radio-link.
    - **"What happens if I lose my radio-link or walk away from it?"** Good question...answered [here](../faqs/rileylink-faqs.md#what-happens-if-i-walk-away-from-my-rileylink).
    - **"Can I use an Omnipod RileyLink with a Medtronic pump? or vice versa?"** Good question...answered [here](../faqs/rileylink-faqs.md#what-will-happen-if-you-use-a-916mhz-antenna-rileylink-with-an-omnipod-or-vice-versa).
    - **"Can I swap out radio-links at any time?"** Yes, you can. Radio-links can be replaced quite simply without needing to start a new pod or rebuild Loop app. There's a place in Loop settings where you find your new device name and turn "on" the Bluetooth connection to start using it. You can swap between RileyLink, OrangeLink, EmaLink or the next version of link.
    - **"How close does the radio-link need to be to me? Do I have to carry it with me?"** Good questions...answered [here](../faqs/rileylink-faqs.md#do-i-have-to-carry-the-rileylink-everywhere).
    - **"Why is it named RileyLink?"** Riley is the name of Pete Schwamb's daughter and he's the guy that created the RileyLink.
    - **"Can I make my own radio-link?"** Technically yes, however it is not an easy project. You'll need specialized tools and patience. [add link here to FAQs](../faqs/rileylink-faqs.md)

## What is RileyLink

The radio-link (RL) is an open-source hardware device that can bridge Bluetooth Low Energy (BLE) to the radio-frequency wireless communication used by select Medtronic and Omnipod pumps. What does that mean to you? It means radio-link is the communication highway between your insulin pump, CGM, and iPhone.

**Loop will not work without the radio-link.**

![img/rl_diag.png](img/rl_diag.png){width="450"}
{align="center"}

## Order RileyLink

There used to be just one option. Now there are more, so you have to make a decision.

## Radio-link Options

!!! danger "Radio-links"
    - One thing that might affect your choice is where you live
        - These devices are sold at cost
        - If you are in the US, shipping for RileyLink and OrangeLink is less expensive
        - The EmaLink ships from Europe
        - A [Comparison Chart](https://getrileylink.org/rileylink-compatible-hardware-comparison-chart?fbclid=IwAR2vHbOzla-zmM-cSp4NkOB_23k3spgnaYvCIGRcACcIQ25FJAU_7HRkH2A) is provided by the getrileylink (non-profit) organization
    - RileyLink
        - Original design, available from [getrileylink](https://getrileylink.org)
        - Rechargable battery (max 36 hours per charge)
        - Must order either Omnipod or Medtronic version
    - OrangeLink
        - Designed by Vic Wu, available from [getrileylink](https://getrileylink.org)
        - Uses 2 AAA batteries
        - Works with either Omnipod or Medtronic
        - Uses new chipsets, reported to have longer range
        - Matches Apple Airpod form factor, so can use airpod cases
    - EmaLink
        - Designed by Sorin Kupas-Spunei to increase range, offer smaller sizes
        - Rechargable battery (a variety of battery sizes are available)
        - Must order either Omnipod or Medtronic version
        - See [EmaLink Information](https://github.com/sks01/EmaLink#emalink) and [EmaLink Wiki](https://github.com/sks01/EmaLink/wiki)
            - Do not worry about the beta testing discussion on the wiki - this link passed beta-testing
        - This design is from Europe, available by sending a private message via github to Sorin (sks01)
        - For US buyers, sometimes a group-buy is organized on Facebook to minimize shipping costs
            - Robert Holbrook has made it easier for US buyers with this [Ema Order Sheet](https://docs.google.com/forms/d/e/1FAIpQLSdcHBUN6e1yPxxvlaXYRBL1liF9W8OYDOpTR2tWquXESo0bKg/viewform)

## Assemble RileyLink

Your RileyLink will come with the battery disconnected and the parts not already inside the case. It will be up to you to put the RL in the case and attach the battery.

Make sure the lipo battery is well-plugged into the connection. Line up the little ridge appropriately, and push fairly firmly to get the connection tight.  Poor battery cable connection can make the Loop communications fail.  See photos below, for example.

!!! info "Common new user errors"

    The most common two errors for new RileyLink owners are (1) not fully pushing in the lipo battery cable connection and (2) failing to charge the RileyLink. Compare your lipo battery cable with the photos; it takes a bit of oomph to push that plug fully in like the photos shown below. Remember to charge your RileyLink each night.

![img/battery-cables.jpg](img/battery-cables.jpg){width="400"}
{align="center"}

Loose battery cable on left, Proper battery cable on right

Finally, the board and the battery fit into the slim case fairly tightly as well.  Click on the image below to watch a helpful [assembly video](https://www.youtube.com/watch?v=-GHxxEJMCZc&feature=youtu.be).

[![img/slimcase.png](img/slimcase.png)](https://www.youtube.com/watch?v=-GHxxEJMCZc&feature=youtu.be)

## Extra Details about RileyLink

All of these radio-links communicate with the pump through radio frequency communications and with the phone through Bluetooth.  Numerous factors can influence how well those communications can function...interferences from other devices, temperature, physical blocking, going through your body (think water), etc.

### Radio communications

When your RL and pump are first paired, Loop performs a series of tests that you won't see...they are tuning tests. Basically, RL sends little test messages to the pump and waits for a response. The RL tries this same "ping" to the pump a range of various radio frequencies. The range of radio frequencies it tries is based on the pump you've told RL to expect (Omnipod, Medtronic NA/CA, or Medtronic WW).  RL will then record the radio frequencies that provided the strongest response and use that frequency for future pump communications.

Usually this best frequency is pretty constant for any given pump+RL, but during temperature changes it may be that the best frequency is not the one currently set. In the event that RL has problems communicating with the pump, Loop has code built-in that will automatically tell the RL "Hey, try that tuning pump thing again...maybe there's a better frequency we need to try." This retuning is started automatically if pump communications fail for 14 minutes (in other words, two looping cycles).

### Bluetooth communications

The radio-link communicates with your iPhone and Loop app through Bluetooth (BT).  

!!! info "Bluetooth Troubleshooting"

    If your iPhone has BT issues, your Loop will have failures.  There have been reports of BT audio devices (such as BT pairings in your car or home audio BT speakers) interfering with the Loop.  If you are finding Loop failures frequently happening at a particular location, you may try to troubleshoot if there are BT problems in the area.

Your BT signal strength can be seen in the Loop settings, Pump settings, device menu, on the `Signal Strength` line. As you move closer and further away from your phone, you can watch that number dynamically change. This line is **not** displaying the signal strength of your pump RF communications, just BT between the radio-link and the phone.

You will notice the Signal Strength is a negative number and in units of dB.  Remember that number line from elementary school?  A signal strength of -50&nbsp;dB is a stronger signal than  -80&nbsp;dB.<br/><br/>

![img/RL_bt.jpg](img/RL_bt.jpg){width="400"}
{align="center"}

### RileyLink Lights

!!! danger ""
    This section is about the RileyLink lights. The other radio-link lights may be different. The light pattern for other radio-links are not included on this page.

The RileyLink has several lights that you may notice from time to time. There is no 'power' light. If you suspect that your RileyLink is not being powered, try turning it off and on using the small sliding switch. You should see lights in the middle of the board flash when you do this.  If they flash, that means the board has power.

* Red light: Charging light. The red light will remain on while RileyLink is charging, and it will turn off when charging is complete. You may notice the red light turn on periodically even after charging is complete...it's just "topping off".

* Green light: Bluetooth connection light. The green light will remain on while you have a BT connection with your iPhone.  If that green light fails to stay on, you should troubleshoot your BT connections. Try restarting BT on your iPhone and/or turning the RileyLink off/on by its power switch.

* Blue light: Pump communications.  If you have an older firmware on your RileyLink, some of the blue lights will flash periodically as it communicates with the pump. It's just letting you know that it is busy talking and collecting info. You will also see increased blue flashes if you have "Enabled Diagnostic LEDs" for MDT users that have the RLs with updated firmware (shipping since late August 2018).

A solid blue light that consistently remains lit on the board could mean one of two things:

* A temporary issue that can be resolved by rebooting the RL physically (turning the switch off/on), or

* An electrical short or damage to the board.  Sweat and moisture are most likely culprits, so try to keep case free from those environments. Don't keep RL in sports bras or waistband next to skin, for example, while exercising.

If your blue light remains on despite trying a restart, it is time to pull out your backup RL.

### RileyLink Charging

The battery that comes with RileyLink is not charged completely when it is shipped, so feel free to charge it up.  You'll need a [mini-USB cable](https://www.amazon.com/AmazonBasics-USB-2-0-Cable--Male/dp/B00NH13S44) and [0.5A USB charging power supply](https://www.amazon.com/Cellet-Powered-Charger-iPhones-Smartphones-/dp/B00FE8WFCO) like your iPhone power supply.  RileyLink takes about 2 hours to fully charge (the red light will turn off when fully charged, read note above about red light patterns) and should easily last at least a full day of constant Loop use.  Typically, it can go into the 30-hour range without any problems.  Most people charge their RL each night when they are sleeping.  You don't have to worry about leaving the RL plugged in "too long" for charging.  It will automatically stop charging the battery when it is fully charged.

Since the best practice is to charge your RileyLink overnight while you sleep, and the battery lasts safely over 24 hours, there is no battery level indicator for the RileyLink.  The RileyLink's charge level is not viewable on Nightscout, nor within the Loop app.  If you forget to charge your RileyLink overnight, you can recharge it with a portable USB battery in a pinch.  A [short mini-USB cable](https://www.adafruit.com/product/899) could be a good addition to a small gear bag.

### Range

The range that your radio-link will function is **heavily** dependent on the environment that you are in. Most people wear the RL in a pocket or carry a belt holster during the day. The radio frequency communications will have a shorter range than the BT communications, therefore RL will do better closer to the pump rather than the iPhone if you are deciding on options for carrying gear.

Problematic environments will be places like technical conferences, sports arenas, and other places where wireless communications are heavy and plenty.

### RileyLink Lipo Battery

Keep your RileyLink and lipo battery protected from damage.  Lipo batteries are unsafe when damaged or punctured, so the case is an important part of safe Looping. If your battery is damaged in some way, please disconnect it immediately, and dispose of it (they should be recycled). You can order new RileyLink batteries on the [GetRileyLink website](http://getrileylink.org/)

### Removing Lipo Battery

To remove the lipo battery from the RileyLink, please do so slowly and patiently. Work the battery connection side to side slowly to loosen it from the plug. Some people have reported success using small, curved needle-nose pliers such as hemostats. Others have used small flathead screwdrivers as shown in [this video](https://youtu.be/s2qNPLpfwww).

[![img/rileylink_battery_removal.png](img/rileylink_battery_removal.png)](https://youtu.be/s2qNPLpfwww)

## Waiting for RileyLink

Yes, waiting for your radio-link to arrive is extremely difficult if they are backordered.  PLEASE be patient, since Loop CANNOT work without one.

If you're really dying to do something while the radio-link ships, you can proceed with finishing these build directions all the way through Step 14...but after that you'll have to wait for the radio-link.  You can't properly enter any settings or pump info in Loop app without it.

## Next Step: Enroll in Apple Developer Program

Now you are ready to move onto Step 6 to [enroll in the Apple Developer Program](step6.md).
