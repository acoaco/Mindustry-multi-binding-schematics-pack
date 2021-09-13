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

| Name                                       | Description                                                  | stat |
| ------------------------------------------ | ------------------------------------------------------------ | ---- |
| bind_template_with_switchunit              | copper=flare lead=mono glass=horizon <br />graphite=nova sand=pulsar coal=poly titanium=mega<br />zenith=thorium scrap=atrax<br />nova and pulsar will auto turn on boost<br />other and null=stop working set unit's flag to 0 | good |
| bind_template_with_switchunit_factorycheck | add a factory check block,check factory/container stat every 2 sec | good |
| bind_flare                                 |                                                              | good |

------------

#### Eco:

copper=flare lead=mono glass=horizon <br />graphite=nova sand=pulsar coal=poly titanium=mega<br />zenith=thorium scrap=atrax<br />nova and pulsar will auto turn on boost<br />other and null=stop working set unit's flag to 0

some autocheck will try add more units

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|  8silicon |  8units |v7 transport speed faster,so change back to 8 silicon|good|
|  2blast | 2units |change to 3 spore for v7<br />blast2 need build around water|good|
|  2differgen | 2units  |v7 transport speed faster,so remove button<br />2 flare can feed 4 differgen+1.5 x overdrive|good|
|  3glass  | 3units  ||good|
|  8graphite  | 3units  |v7 transport speed faster,so add 1 graphite|good|
|  2phase(sand)  | 1unit  | 2 units > 1 unit                                             | good                                       |
|  2phase  | 3units  |4 units > 3 units| good |
|  3plast(blacksand)  | 3units  ||good|
|  1plast(water)  | 1units  |2 units > 1 unit|good|
|  2surge | 5units |can 1.5 x overdrive|good|
|  cent's itembox<br />(take items inside box back to core)  | 2units~4units |when total items>100 auto add 2 units| good |



------------

#### Unit factory:

copper=flare lead=mono glass=horizon <br />graphite=nova sand=pulsar coal=poly titanium=mega<br />zenith=thorium scrap=atrax<br />nova and pulsar will auto turn on boost<br />other and null=stop working set unit's flag to 0

unlike eco factory,unit factory is expensive,so autocheck overdrive try add more units

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|T3 fortress|3units||ok|
|T3 spiroct|3units||ok|
|T3 zenith|3units||ok|
|T3 mega|4units||ok|
|T3 bryde|4units||ok|
|T3 bryde|4units||ok|
|T3 quasar|4units||ok|
|T3 cyerce|4units||ok|
|T1 3risso|3flares|can't change unit type,for early game rush<br />when factory3 reach 70metaglass auto turn to 2 flares,no unit type switch function|ok|
|T4|6units|button add 4 more units,if you're making T5 don't need click button|ok|
|T5|5units||ok|
|Cryofluid|1units|60Cryofluid,button add 1 unit=120cryofluid|ok|
|pulsar_polymix|2units|auto use 1 unit when only has 1 T1 factory<br />can auto search sand now|ok|
------------

#### Turret:

remove hail rader,it's doesn't need in V7

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|4 thorium salvo|2flare|for faster refill speed,remove hail for v7|ok|
|2 hail+2 scatter|2flare|default sorter copper=don't hit building,other attack anything<br />if you don't need this control feature you can remove the sorter|ok|
|6 scatter|3flare|epic|ok|
|2 cyclone|2flare|plastanium only,other ammo too weak|ok|
|1 spectre|2flare||ok|
|1 CryoTsunami|1flare||ok|
|2 ripple|2flare|plastanium only,other ammo too weak|ok|
|||||

