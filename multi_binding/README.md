Eco and unit factory's nexttime is 5000,which means they check units's stat every 5 secs,once it's find unit it's will continute work,turret is 2000
shorter nexttime eat more performance for check unit's stat,can't do lot work,but grab unit faster at first run



# Utilities

If you're new to logic,I suggest build this,prevent idle unit take resource and set broken unit's flag to 0 which prevent save game broken your flag

If you've your own flag resetter and controller,you can ignore it

# (Important)If you're play offline you need build flag_resetter cuz logic will lost their binding stat after you load a game(but units still keep flag,due logic only search flag 0 to bind,so they can't find units,you need a resetter to reset idle orphan units make logic can find them again)

| Name                                                         | Description                                                  | stat |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| flag_resetter                                                | reset unit has flag but uncontrolled to flag 0 make it can be use again<br />it's doesn't has global resource recycle function  <br />cuz if you let flag 0 + uncontrolled units put resource back to core<br/>but when you try to do that it's already got controlled by this logic <br/>so the only choice is let flag 0 units take resources back to core,but it's will disturb flag 0 zenith/horizon control logic take blast/spore/coal/thorium<br/> | done |
| flare_controller_put_resource_back_to_core_when_flag_0.msch  | flare,flare flag resetter + flag 0 uncontrolled flare put resource back to core | done |
| horizon_controller_put_resource_back_to_core_when_flag_0.msch | horizon,same as above<br />sorter copper for auto search core,lead for search generator | done |
| tower_controller                                             | control tower shot same position<br />click logic>bind the tower you want control>enter arc>shot | done |



------

#### Template:

Template,if you want write your own thing,you can check it

| Name                                         | Description                                                  | stat |
| -------------------------------------------- | ------------------------------------------------------------ | ---- |
| bind_template_with_switch_unit               | ![copper](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-copper.png?raw=true)=![flare](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-flare-ui.png?raw=true) ![lead](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-lead.png?raw=true)=![mono](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-mono-ui.png?raw=true) ![glass](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-metaglass.png?raw=true)=![horizon](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-horizon-ui.png?raw=true) <br />![graphite](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-graphite.png?raw=true)=![nova](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-nova-ui.png?raw=true) ![sand](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-sand.png?raw=true)=![pulsar](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-pulsar-ui.png?raw=true) ![coal](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-coal.png?raw=true)=![poly](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-poly-ui.png?raw=true) ![titanium](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-titanium.png?raw=true)=![mega](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-mega-ui.png?raw=true)<br />![zenith](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-thorium.png?raw=true)=![thorium](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-zenith-ui.png?raw=true) ![scrap](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-scrap.png?raw=true)=![atrax](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-atrax-ui.png?raw=true)<br />![nova](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-nova-ui.png?raw=true) and ![pulsar](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-pulsar-ui.png?raw=true) will auto turn on boost<br />set sorter to other and null=stop factory and set unit's flag to 0 | done |
| bind_template_with_switch_unit_factory_check | add a factory check block,check factory/container stat every 2 sec | done |
| bind_flare                                   | only flare no sorter,good for wireless Turret fast refill    | done |
| call_job_template                            | 2 most useful function in V7,easily set control unit trans resources | done |

------------

#### Eco:

check Template>bind_template_with_switch_unit for unit control detail

some autocheck will try add more units

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|  8silicon |  8units |v7 transport speed faster,so change back to 8 silicon|done|
|  2blast | 2units |change to 3 spore for v7<br />blast2 need build around water|done|
|  2differgen | 2units  |v7 transport speed faster,so remove button<br />2 flare can feed 4 differgen|done|
|  3glass  | 3units  ||done|
|  8graphite  | 3units  |v7 transport speed faster,so add 1 graphite| done |
|  2phase(sand)  | 1unit  | 2 units > 1 unit                                             | done                                   |
|  2phase  | 3units  |4 units > 3 units| done |
|  3plast(blacksand)  | 3units  ||done|
|  1plast(water)  | 1units  |2 units > 1 unit|done|
|  2surge | 5units |can 1.5 x overdrive|done|
|  cent's item_collect_box<br />(take items inside box back to core)  | 2units~4units |when total items>100 auto add 2 units| done |
| dome | 2units |a dome has conveyor storage can run long time without flare keep refill<br />when conveyor1&2 has more than 5 items,it's stop flare<br />when dome less than 7 items it's call flare again| done |



------------

#### Unit factory:

check Template>bind_template_with_switch_unit for unit control detail

unlike eco factory,unit factory is expensive,so autocheck overdrive try add more units

if no T3 factory it's bind 2 units for T1~T2

|  Name | Count | OD | no T3 factory(T1~T2only mode) | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |  ------------ |  ------------ |
|T3 fortress|3units|4units|2units||done|
|T3 spiroct|3units|4units|2units||done|
|T3 zenith|3units|4units|2units||done|
|T3 mega|4units|5units|2units||done|
|T3 bryde|4units|5units|2units||done|
|T3 quasar|4units|5units|2units||done|
|T3 cyerce|4units|5units|2units||done|
|T1 3risso|3flares|||can't change unit type,for early game rush<br />when factory3 reach 70metaglass auto turn to 2 flares,no unit type switch function<br />a legacy schematic|ok|
|T4|6units||||done|
|T5|5units||||done|
|cryo_fluid|1units|||60Cryofluid,button add 1 unit=120cryofluid|done|
|pulsar_polymix_with_pulsar_mining|2units|||auto use 1 unit when only has 1 T1 factory<br />can auto search sand now<br />include a pulsar mining logic,good for getting coal/sand/building speed at early game|done|
------------

#### Turret:

remove hail rader,it's doesn't need in V7

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|4 thorium salvo|2flare|for faster refill speed,remove hail for v7|done|
|2 hail+2 scatter|2flare|default sorter copper=don't hit building,other attack anything<br />if you don't need this control feature you can remove the sorter<br />use graphite and lead|done|
|6 scatter|3flare|a epic|done|
|2 cyclone|2flare|plastanium only,other ammo too weak|done|
|1 spectre|2flare||done|
|1 cryo_tsunami|1flare||done|
|2 ripple|2flare|plastanium only,other ammo too weak|done|
|||||

------

#### Mining Logic:

you can set keep at least how many copper and lead at logic's line 1,before mining other resources,default is 1k

| Name   | Description                                                  | stat |
| :----- | ------------------------------------------------------------ | ---- |
| Mono   | keep 1k copper and lead then try balance between lead/copper/sand,this one has a auto unloader config make 1 unloader can feed 2 mono factory | done |
| Pulsar | keep 1k copper and lead then try balance between sand/coal   | done |
| Quasar | keep 1k copper and lead then try balance between  sand/coal/titanium | done |
| Mega   | keep 1k copper and lead then try balance between  sand/coal/titanium | done |

