Eco and unit factory's nexttime is 5000,which means they check units's stat every 5 secs,once it's find unit it's will continute work,turret is 2000
shorter nexttime eat more performance for check unit's stat,can't do lot work,but grab unit faster at first run



# Utilities(Important)

If you're new to logic,I suggest build this,prevent idle unit take resource and set broken unit's flag to 0 which prevent save game broken your flag

If you've your own flag resetter and controller,you can ignore it

| Name                                                         | Description                                                  | stat |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| flag_resetter                                                | reset unit has flag but uncontrolled to flag 0 make it can be use again<br />it's doesn't has global resource recycle function  <br />cuz if you let flag 0 + uncontrolled units put resource back to core,but when you try to do that it's already got controlled by this logic <br />so no way to prevent disturb flag 0 zenith/horizon take blast/spore/coal/thorium<br /> | good |
| flare_controller_put_resource_back_to_core_when_flag_0.msch  | flare,flare flag resetter + flag 0 uncontrolled units put resource back to core | good |
| horizon_controller_put_resource_back_to_core_when_flag_0.msch | horizon,sorter for auto search target                        | good |

------

#### Template:

Template,if you want write your own thing,you can check it

| Name                                               | Description                                                  | stat      |
| -------------------------------------------------- | ------------------------------------------------------------ | --------- |
| bind3_template_with_switchunit                     | copper=flare lead=mono glass=horizon <br />graphite=nova sand=pulsar coal=poly titanium=mega<br />nova and pulsar will auto turn on boost<br />other and null=stop working set unit's flag to 0 | rewriting |
| bind6_template                                     |                                                              | rewriting |
| bind3_template_with_switchunit_factorycheckversion |                                                              | rewriting |

------------

#### Eco:

copper=flare lead=mono glass=horizon other or null=stop working set unit's flag to 0
if it's has button click add 2 more units for 150% overdrive projector

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|  8silicon |  8units |v7 transport speed faster,so change back to 8 silicon|ok|
|  2blast | 2units |change to 3 spore for v7<br />blast2 need build around water|ok|
|  2differgen | 2units  |v7 transport speed faster,so remove button,now 2 flare can feed 4 differgen+1.5 x overdrive|ok|
|  3glass  | 3units  ||ok|
|  8graphite  | 3units  |v7 transport speed faster,so add 1 graphite|ok|
|  2phase(sand)  | 1unit  | 2 units > 1 unit                                             | ok                                           |
|  2phase  | 3units  |4 units > 3 units|ok|
|  3plast(blacksand)  | 3units  ||ok|
|  1plast(water)  | 2units  |2 units > 1 unit|ok|
|  2surge | 5units |can 1.5 x overdrive|ok|
|  cent's itembox  | 2units  |button add 2 more units,take first item from box to your core|ok|

------------

#### Unit factory:

Due faster unit transport,can support 200-225% overdrive in V7

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|T3 fortress|3units||rewriting|
|T3 spiroct|3units||rewriting|
|T3 zenith|3units||rewriting|
|T3 mega|4units||rewriting|
|T3 bryde|4units||rewriting|
|T3 bryde|4units||rewriting|
|T3 quasar|4units||rewriting|
|T3 cyerce|4units||rewriting|
|T1 3risso|3flares|can't change unit type,for early game rush<br />when factory3 reach 70metaglass auto turn to 2 flares,no unit type switch function|rewriting|
|T4|6units|button add 4 more units,if you're making T5 don't need click button|rewriting|
|T5|5units||rewriting|
|Cryofluid|1units|60Cryofluid,button add 1 unit=120cryofluid|rewriting|
|pulsar_polymix|2units|auto use 1 unit when only has 1 T1 factory<br />can auto search sand now|rewriting|
------------

#### Turret:

remove hail rader,it's doesn't need in V7

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|4 thorium salvo|2flare|for faster refill speed,remove hail for v7|good|
|2 hail+2 scatter|2flare|default sorter copper=don't hit building,other attack anything<br />if you don't need this control feature you can remove the sorter|good|
|6 scatter|3flare|epic|good|
|2 cyclone|2flare|plastanium only,other ammo too weak|good|
|1 spectre|2flare||good|
|1 CryoTsunami|1flare||good|
|2 ripple|2flare|plastanium only,other ammo too weak|good|
|||||

