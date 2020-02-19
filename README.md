# OpenAmigaFourPlayerAdapter
OpenAmigaFourPlayerAdapter is an Open Hardware adapter that allows connection of up to four joysticks to Amiga Computers.

![Board](https://raw.githubusercontent.com/SukkoPera/OpenAmigaFourPlayerAdapter/master/img/render-top.png)

### Summary
Some Amiga Games support more than the two joysticks you can connect directly yo all Amiga models. The two extra joysticks are supposed to be connected to the parallel port through an adapter. OpenAmigaFourPlayerAdapter is an Open Hardware implementation of such an adapter, based on [Tomi Engdahl's Multi-joystick extender circuit](https://www.epanorama.net/documents/joystick/amiga_circuits.html), which claims to be the de-facto standard for this. The same circuit was found on other sources, so this should not be too far away from the actual truth.

The adapter slightly improves that design by also providing 5V power to the joystick ports.

The adapter was only tested with Dyna Blaster. [Here is a list](http://eab.abime.net/showthread.php?t=3062) of more games that *should* hopefully work with it.

### Usage
Building the adapter is very easy, just note that you need all male connectors, for both the DB-9 and the DB-25 ports.

You are recommended to **only connect/disconnect the adapter and the joysticks while your Amiga is powered off**, in order to avoid any risk of damage.

The adapter needs no configuration. The only option is whether the 5V power pins of the joystick ports should actually be powered or not. Most old-style joysticks do not need power, but if you are using one with autofire functionalities or maybe [some kind of adapter](https://github.com/SukkoPera/OpenPSX2AmigaPadAdapter), it probably will. Now, the problem is that most (if not all) Amiga models limit the current that can be drawn from the parallel port through a resistor, usually 47 ohm 1/2 W. This means that only about 100 mA will be available on the port. This should be enough for most joysticks, but please make sure this is ok in your case, or you might blow the current limiting resistor inside your Amiga.

[Ian Steadman](http://www.ianstedman.co.uk/Amiga/amiga_h_w/parallel_port/parallel_port.html) says that Amiga parallel port can only supply 3.2mA. I don't know what he based his calculations on, but this definitely means you MUST check carefully what is inside your Amiga and do your maths,

Once you are sure your Amiga can bear the current, just close the jumper placed near the port of interest.

### Releases
If you want to get this board produced, you are recommended to get [the latest release](https://github.com/SukkoPera/OpenAmigaFourPlayerAdapter/releases) rather than the current git version, as the latter might be under development and is not guaranteed to be working.

Every release is accompanied by its Bill Of Materials (BOM) file and any relevant notes about it, which you are recommended to read carefully.

### License
The OpenAmigaFourPlayerAdapter documentation, including the design itself, is copyright &copy; SukkoPera 2020.

OpenAmigaFourPlayerAdapter is Open Hardware licensed under the [CERN OHL v. 1.2](http://ohwr.org/cernohl).

You may redistribute and modify this documentation under the terms of the CERN OHL v.1.2. This documentation is distributed *as is* and WITHOUT ANY EXPRESS OR IMPLIED WARRANTIES whatsoever with respect to its functionality, operability or use, including, without limitation, any implied warranties OF MERCHANTABILITY, SATISFACTORY QUALITY, FITNESS FOR A PARTICULAR PURPOSE or infringement. We expressly disclaim any liability whatsoever for any direct, indirect, consequential, incidental or special damages, including, without limitation, lost revenues, lost profits, losses resulting from business interruption or loss of data, regardless of the form of action or legal theory under which the liability may be asserted, even if advised of the possibility or likelihood of such damages.

A copy of the full license is included in file [LICENSE.pdf](LICENSE.pdf), please refer to it for applicable conditions. In order to properly deal with its terms, please see file [LICENSE_HOWTO.pdf](LICENSE_HOWTO.pdf).

The contact points for information about manufactured Products (see section 4.2) are listed in file [PRODUCT.md](PRODUCT.md).

Any modifications made by Licensees (see section 3.4.b) shall be recorded in file [CHANGES.md](CHANGES.md).

The Documentation Location of the original project is https://github.com/SukkoPera/OpenAmigaFourPlayerAdapter/.

### Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay through this link:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/OpenAmigaFourPlayerAdapter_V1.html)

You get my gratitude and cheap, professionally-made and good quality PCBs, I get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and yield me some more).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :). But then you can buy me a coffee if you want:

<a href='https://ko-fi.com/L3L0U18L' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi2.png?v=2' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

### Get Help
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).

### Thanks
- http://www.hardwarebook.info/Amiga_4_Joysticks
- http://eab.abime.net/showthread.php?t=3062