# PCB-Powerwalls
This is the public file Repository for the [DIY PCB Powerwalls Community](https://www.facebook.com/groups/2573968699280898/). The projects are developed and maintained by **Vinnie Maro** and **Shaun Bond**.

We are developing a PCB alternative to common powerwall building techniques for 18650(and similar) batteries. This system has been developed with maintainability, expandability, and practicality in mind. 

For additional DIY Powerwall building resources, please check out some of the many other active facebook groups and forums:
* [DIY Powerwalls](https://www.facebook.com/groups/323586824654552/)
* [Jehu's DIY Powerwalls](https://www.facebook.com/groups/183620862292017/)
* [DIY Powerwall - easy](https://www.facebook.com/groups/244099703167519/)
* [Second Life Storage](https://secondlifestorage.com/index.php)

## Features in Development
To see features currently in development or exploration, check out our [issues](https://github.com/WannaBAcoder/PCB-Powerwalls/issues) page.

## 15s4p PCB

The 15s4p battery board is a stackable solution that reduces the amount of wiring required by placing all series and balance connections through standoffs that structurally connect the boards. Batteries mount to both sides of the PCB, in a variety of ways. Each cell is individually fused for added safety.

### 1. Plastic battery holders

You can choose to use plastic cell holders that are available in many through-hole and surface mount packages. For the through-hole packages, you must bend the pins at a 90 degree angle so that the holders sit as flat as possible.

![Top view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/15s4p_PCB/Renders/holder_top.jpg)
![Iso view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/15s4p_PCB/Renders/holder_side.jpg)

### 2. Spring clips

A cheaper alternative to plastic holders is spring clips. The clips work like traditional battery holders with springs, but these require the use of zip ties to hold the cells in place.

![Top view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/15s4p_PCB/Renders/15s4p_board_top.jpg)
![Iso view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/15s4p_PCB/Renders/15s4p_board_side.jpg)

### 3. Fuse wire

The last option is to use fuse wire. You will still need to use zip ties to hold the cells in place, but you can solder the fuse wire directly to the PCB pads, and remove the need for populating fuses(you will need to short the fuse pads to do this). You can also use large fuse wire and still use fuses, if desired. Spotwelding fuse wire to the batteries and soldering the other end to the PCB pads is recommended.

![Top view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/15s4p_PCB/Renders/fw_top.jpg)
![Iso view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/15s4p_PCB/Renders/fw_side.jpg)

### 7s Adapter PCB

The 7s Adapter PCB was created to take our popular 15s4p design and convert it into a 7s8p PCB. We do this by leaving the out the 8s cells, which creates two 7s groups that get connected in parallel. It is recommended to use at least one of these adapter PCBs for every 5 boards, or 20A of main fuse(which is 10A load on each of these boards). This board also joins the battery stacks with standoffs. It's important to equally space these boards within a pack for best current distribution. For example, a 12 battery board stack could use 3 adapter boards, spaced every 4 boards.

![Top view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/master/7sAdapter_PCB/Renders/top.png)
![Iso view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/Development/7sAdapter_PCB/Renders/iso.png)

### BMS/Display Adapter PCB

The BMS/display adapter board helps the user connect a [Moonitor](https://www.sarperonal.com/product/6s-16s-solar-plc-li-ion-battery-protection-system/), or a variety of BMS systems to the battery PCB stacks, and is capable of supporting ~5A balance current. This board also includes spaces to add series-level voltage displays, but they can be disabled if not desired.  You can also use this board with the 7s adapter board configurations.

![Top view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/Development/BMS_display_adapter_PCB/Renderings/top.png)
![Iso view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/Development/BMS_display_adapter_PCB/Renderings/iso.png)

![moonitor view](https://github.com/WannaBAcoder/PCB-Powerwalls/blob/Development/BMS_display_adapter_PCB/Renderings/MoonitorBMS.png)

## Building Your Own

### Ordering the PCBs

You can order your own boards from any number of PCB manufacturers. Many of our supporters use [JLCPCB.com](https://jlcpcb.com/quote).

**Recommended manufacturing options:**
* PCB thickness - 1.6mm
* PCB color-Your choice (black is not available for 2oz copper orders)
* Surface finish - HASL(with lead)
* Copper weight - 1oz or 2oz **(Higher current applications use 2oz)**
* All other options can be left as default

### Ordering Parts
#### Common Parts
* M4 Standoffs(40mm for SMD plastic holders, 45mm for through-hole plastic holders, may be able to make 40mm work with zip tie methods if zipties are alternated. Not confirmed at this time)
    -  [Nickel plated steel](https://www.aliexpress.com/item/33009686876.html?spm=a2g0o.productlist.0.0.61571f66pt5bWm&algo_pvid=9a643e7a-535f-40cf-b5ed-bd621be4c2a2&algo_expid=9a643e7a-535f-40cf-b5ed-bd621be4c2a2-38&btsid=cb015f28-81e7-4d5b-bff6-ac27e1b705c9&ws_ab_test=searchweb0_0%2Csearchweb201602_7%2Csearchweb201603_53&fbclid=IwAR1i7L36_8TP1QeeUUGsSI7OYQZ8V5TdpMY-vIQx72vAV06tubDgNu83XK8)
    - [Brass](https://www.aliexpress.com/item/32909068891.html?pid=808_0000_0109&spm=a2g0n.search-amp.list.32909068891&aff_trace_key=332c98827ee6446f80143395d597b19b-1564724741171-07852-UneMJZVf&aff_platform=msite&m_page_id=9849amp-ds4DZWQQ-IDu7HzwI4TLGw1564724838958&fbclid=IwAR3M15Ip61Iu9X8k-uB9fa5s9BZqdkEpw6nAfUjtFbnB0vwKfW6etgOFu9g)
    
* 60x Glass Axial Fuses
**Choosing the right fuse is based on tradeoff between usebility and saftey. Even a 0.5A fuse can't protect against all 18650(and similar) failure modes. Shaun Bond's testing suggests 0.5A fuses are the ideal size for safety, but impractical for all massive builds with low load. You should still consider your pack-loading characteristics when choosing them.**
  - [0.5A](https://www.ebay.com/itm/200Pcs-Glass-Fuse-Tube-Axial-With-Lead-Wire-Fast-Blows-Fuse-3x10mm-250V-0-5A-US-/283481427034?hash=item4200cf4c5a)
  - [1A](https://www.ebay.com/i/372678478703?chn=ps&norover=1&mkevt=1&mkrid=711-117182-37290-0&mkcid=2&itemid=372678478703&targetid=486560530718&device=m&mktype=pla&googleloc=9030145&poi=&campaignid=1497793114&mkgroupid=60383707360&rlsatarget=pla-486560530718&abcId=1139456&merchantid=137697764&gclid=EAIaIQobChMItaCEy6Dk4wIV0Rx9Ch3iWgGvEAQYCyABEgKVxPD_BwE&fbclid=IwAR1QAa1hm0T0Rmuvq4w6-hz3E788jz0vE18OvbbaAJsIOb30UHCT80PTtSM)
  - [1.5A](https://www.ebay.com/itm/200Pcs-Glass-Fuse-Tube-Axial-With-Lead-Wire-Fast-Blows-Fuse-3x10mm-250V-1-5A-P/401758396012?_trkparms=aid%3D555018%26algo%3DPL.SIM%26ao%3D2%26asc%3D20160908110712%26meid%3Da10f567fa4374be69fc06417b70cef45%26pid%3D100677%26rk%3D4%26rkt%3D30%26sd%3D333259318203%26itm%3D401758396012%26pg%3D2385738&_trksid=p2385738.c100677.m4598)
  - [2A](https://www.ebay.com/i/283303754606?rt=nc&_trkparms=aid%3D222007%26algo%3DSIM.MBE%26ao%3D2%26asc%3D20160908110712%26meid%3Da10f567fa4374be69fc06417b70cef45%26pid%3D100677%26rk%3D5%26rkt%3D30%26sd%3D333259318203%26itm%3D283303754606%26pg%3D2385738)
  - [3A](https://www.ebay.com/itm/200Pcs-Glass-Fuse-Tube-Axial-With-Lead-Wire-Fast-Blows-Fuse-3x10mm-250V-3A-US/283485834501?_trkparms=aid%3D555018%26algo%3DPL.SIM%26ao%3D2%26asc%3D20160908110712%26meid%3D45fd6583f6e14ab2a546fee1b4138e27%26pid%3D100677%26rk%3D1%26rkt%3D30%26sd%3D283303754606%26itm%3D283485834501%26pg%3D2385738&_trksid=p2385738.c100677.m4598)
  - [aliexpress](https://www.aliexpress.com/item/32910625856.html?spm=a2g0o.productlist.0.0.1737d2b4jAQsRa&algo_pvid=d670b6fe-927f-49bc-8e46-4ea88ec12f0d&algo_expid=d670b6fe-927f-49bc-8e46-4ea88ec12f0d-17&btsid=31c10488-12d2-4517-82d5-fce6cd9fe86a&ws_ab_test=searchweb0_0%2Csearchweb201602_7%2Csearchweb201603_53&fbclid=IwAR2cu_fARDCkvXmC-ECtJe0K4SezOG-_YxEne1wyviiZ2j2a6Mf_GHND5QM)
    
#### 15s4p PCB
**Be sure to choose the right holders for your desired build. For plastic holder builds, the quantities assume using only 1-cell and 2cell, or 3-cell and 4-cell holders per board. 
* Plastic Holders
  - 4x 1-cell holder([Keystone 1042](https://www.keyelco.com/product.cfm/product_id/918))
    - [mouser](https://www.mouser.com/ProductDetail/Keystone-Electronics/1042?qs=%2F7TOpeL5Mz4qPdWi9tuLKw%3D%3D&gclid=CjwKCAjwm4rqBRBUEiwAwaWjjC21kEPrcNO7SQeen5w2QoHVTzlL-M1gGIkDHi2yZwdU-rbxfRRc6xoCWLsQAvD_BwE)
    - [aliexpress](https://www.aliexpress.com/item/32843455571.html?spm=a2g0o.productlist.0.0.487c40e68pqd20&algo_pvid=2d7f9b9f-3d4c-4ce9-a35f-b65c2eb5f04f&algo_expid=2d7f9b9f-3d4c-4ce9-a35f-b65c2eb5f04f-0&btsid=5be8ef8c-3a87-41c8-af7c-a986ac64726d&ws_ab_test=searchweb0_0,searchweb201602_4,searchweb201603_52)

  - 28x 2-cell holder([Keystone 1048](https://www.keyelco.com/product.cfm/product_id/920)) 
    - [mouser](https://www.mouser.com/ProductDetail/Keystone-Electronics/1048?qs=%2F7TOpeL5Mz5jXkg8vI8Dyw%3D%3D)
    - [aliexpress](https://www.aliexpress.com/item/32810550974.html?spm=a2g0o.productlist.0.0.6d23509fdGDO8G&algo_pvid=bc697f71-8610-42bf-9caa-2c6182c8690e&algo_expid=bc697f71-8610-42bf-9caa-2c6182c8690e-0&btsid=5fac0df8-46fd-44b7-bddc-d52b5a4952c4&ws_ab_test=searchweb0_0,searchweb201602_4,searchweb201603_52)

  - 4x 3-cell holder(BK-18650-PC6)(through-hole)
    - [digikey](https://www.digikey.com/product-detail/en/mpd-memory-protection-devices/BK-18650-PC6/BK-18650-PC6-ND/2330514)
    - [aliexpress](https://www.aliexpress.com/item/32855470302.html?spm=a2g0o.productlist.0.0.26e322047uCJsr&algo_pvid=3ca87fa6-d69e-461c-b294-00b2a046b8a9&algo_expid=3ca87fa6-d69e-461c-b294-00b2a046b8a9-0&btsid=ad3d8f8d-a38c-414e-bdd7-eb4ffd6dbeee&ws_ab_test=searchweb0_0,searchweb201602_7,searchweb201603_53)

  - 24x 4-cell holder(BK-18650-PC8)(through-hole)
    - [digikey](https://www.digikey.com/product-detail/en/mpd-memory-protection-devices/BK-18650-PC8/BK-18650-PC8-ND/2330515)
    - [aliexpress](https://www.aliexpress.com/item/32813957846.html?spm=a2g0o.productlist.0.0.69dd44c0Jy70zY&algo_pvid=6d1f0285-86b4-4f30-8689-4ffc808e86bf&algo_expid=6d1f0285-86b4-4f30-8689-4ffc808e86bf-0&btsid=38b36ad8-3752-4109-9ae1-f03aeb2c26e8&ws_ab_test=searchweb0_0,searchweb201602_7,searchweb201603_53)
       
* 120x Spring clips([Keystone 5331](https://www.keyelco.com/product.cfm/product_id/823))
    - [mouser](https://www.mouser.com/ProductDetail/Keystone-Electronics/5331?qs=poiiR8sYdC9oC9Ij8wI9kA%3D%3D)
    - [newark](https://www.newark.com/keystone/5331/battery-contact-a-aa-2-3a-cell/dp/25T0473)
 
#### BMS/Display Adapter PCB
* 1x Total voltage pack voltage display(Adafruit 705)
    - [mouser](https://www.digikey.com/products/en/industrial-automation-and-controls/panel-meters/805?k=adafruit%20705)
    - [Adafruit](https://www.adafruit.com/product/705
    
* 15x Series-group voltage display(Seeed 114990163)
    - [mouser](https://www.mouser.com/ProductDetail/Seeed-Studio/114990163?qs=%2Fha2pyFaduhQJK%2FIqB6h3cWbaw8mrLdet0cfTARQbUci7a%252BfqW62TQ%3D%3D)
    - [Seeed](https://www.seeedstudio.com/0-28-Inch-LED-digital-DC-voltmeter-Green-p-2287.html)
    - [Digikey](https://www.digikey.com/products/en/industrial-automation-and-controls/panel-meters/805?k=&pkeyword=&sv=0&v=1597&pv1989=0&sf=0&FV=ffe00325&quantity=&ColumnSort=0&page=1&stock=1&pageSize=25) has other colors too.
    
* 1x 12VDC 40x40mm PC Fan(2-wire)
    - Tons of these on [Amazon](https://www.amazon.com/WINSINN-Brushless-40x40x10mm-Extruder-Makerbot/dp/B0757LXKST/ref=sr_1_3?keywords=12v+40mm+fan&qid=1564763803&s=gateway&sr=8-3)

* 1x 75VDC to 12V buck converter module.
    - [mouser](https://www.mouser.com/ProductDetail/XP-Power/SRH05S12?qs=%2Fha2pyFadugN%252BYt0642c137FJqBA04EEkA%252BHmhjnYgQ%3D)
    - [Digikey](https://www.digikey.com/products/en?keywords=srh05s12)
    
* 1x 0.25A glass fuse
    - [Digikey](https://www.digikey.com/product-detail/en/littelfuse-inc/0251.250NRT1L/F5997CT-ND/4146349)
    - [mouser](https://www.mouser.com/ProductDetail/Littelfuse/0251250NRT1L?qs=%2Fha2pyFadugfDk6tKwZ2TFq2EME7Ea%252Bx7IV62g8M4POuyu4j1eOqCA%3D%3D)
    - [Ebay](https://www.ebay.com/itm/200Pc-Glass-Tube-Fuse-Metal-Axial-Double-Hat-Fast-Blow-Fuse-3-6x10mm-250V-0-25A/264389811818?epid=2270852170&hash=item3d8edc5e6a:g:CDoAAOSwokVdIOIx)

* 16x B4A Lugs
    - [hex](https://lugsdirect.com/B4A-PCB-HEX.html)
    
* 0.1" male pin headers
    - [aliexpress](https://www.aliexpress.com/item/32899255706.html?spm=a2g0o.productlist.0.0.6a13532boQDFkx&algo_pvid=8dbb68db-2cf8-45e3-86e2-01a316cf7929&algo_expid=8dbb68db-2cf8-45e3-86e2-01a316cf7929-8&btsid=413ff5c7-b166-4259-ab24-a0d8e013eebf&ws_ab_test=searchweb0_0,searchweb201602_7,searchweb201603_53)
    
* 0.1" jumper blocks
    - [aliexpress](https://www.aliexpress.com/item/32972892184.html?spm=a2g0o.productlist.0.0.679cd873JeFb6B&s=p&algo_pvid=b014d28b-b7de-4ef0-ac41-d2149ee41d24&algo_expid=b014d28b-b7de-4ef0-ac41-d2149ee41d24-5&btsid=e50a15f9-9d8d-4b6d-bcb8-219688b9c177&ws_ab_test=searchweb0_0,searchweb201602_7,searchweb201603_53)
 
* Moonitor BMS

You can purchase this BMS from the Moonitor team on their [website](https://www.sarperonal.com/product/6s-16s-solar-plc-li-ion-battery-protection-system/). You can also contact [them](https://www.sarperonal.com/contact-us/) directly for more information.

### Building Instructions and Documentation
Check out the [wiki](https://github.com/WannaBAcoder/PCB-Powerwalls/wiki) for assembly instructions, and additional information.

## Versioning

Each powerwall PCB has its own revision in the form of VX.X. In addition to this, we version the entire system package in a release in the form of RX.0. See the latest release for the most recent hardware package. Whenever any of the hardware in a package changes, the PCB version and package release will be updated. PCB versions are printed on all PCBs for easy identification.

## Contributing

Although the kicad source files are available, the safety considerations that go into this project make it potentially unsafe to modify; do so at your own risk! You can always contribute to the development of this project by suggesting improvements or new features desired by reporting them as [issues](https://github.com/WannaBAcoder/PCB-Powerwalls/issues).

## License

This project is licensed under the CERN Open Hardware License - see the [LICENSE.txt](LICENSE.txt) file for details.

## Acknowledgments

A special thank you to the people and communities that inspired or helped develop the early versions of this hardware and helped others realize the growing potential for these designs:
* Shaun Bond
* Izz Eselam
* Paulo E Cabigao
* Dale Bliss
* Jehu Garcia 
* Andrew Hunt
* Daniel Wiermans

