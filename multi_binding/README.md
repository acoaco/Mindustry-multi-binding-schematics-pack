Eco and unit factory's nexttime is 5000,which means they check units's stat every 5 secs,once it's find unit it's will continute work,turret is 2000
shorter nexttime eat more performance for check unit's stat,can't do lot work,but grab unit faster at first run



# Utilities

If you're new to logic,I suggest build this,prevent idle unit take resource and set broken unit's flag to 0 which prevent save game broken your flag

If you've your own flag resetter and controller,you can ignore it

# (Important)If you're play offline you need build flag_resetter cuz logic will lost their binding stat after you load a game(but units still keep flag,due logic only search flag 0 to bind,so they can't find units,you need a resetter to reset idle orphan units make logic can find them again)

| Name                                                         | Description                                                  | stat |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| Flag Resetter                                                | reset unit has flag but uncontrolled to flag 0 make it can be use again<br />it's doesn't has global resource recycle function  <br />cuz if you let flag 0 + uncontrolled units put resource back to core<br/>but when you try to do that it's already got controlled by this logic <br/>so the only choice is let flag 0 units take resources back to core,but it's will disturb flag 0 zenith/horizon control logic take blast/spore/coal/thorium<br/> | done |
| Flare Controller+put resource back to core_when flag0.msch   | flare,flare flag resetter + flag 0 uncontrolled flare put resource back to core<br />it's a old thing so no label code | done |
| Horizon Controller+put resource back to core_when flag0.msch | orizon,same as above<br />sorter copper for auto search core,lead for search generator<br />it's a old thing so no label code | done |
| Tower Controller                                             | control tower shot same position<br />click logic>bind the tower you want control>enter arc>shot<br />it's a old thing so no label code | done |



------

#### Template:

Template,if you want write your own thing,you can check it

| Name                                         | Description                                                  | stat |
| -------------------------------------------- | ------------------------------------------------------------ | ---- |
| bind_template_with_switch_unit               | ![copper](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-copper.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-flare-ui.png?raw=true" alt="flare" style="width: 50px; height: 50px" /> ![lead](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-lead.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-mono-ui.png?raw=true" alt="mono" style="width: 50px; height: 50px" /> ![glass](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-metaglass.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-horizon-ui.png?raw=true" alt="horizon" style="width: 50px; height: 50px" /> ![graphite](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-graphite.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-nova-ui.png?raw=true" alt="nova" style="width: 50px; height: 50px" /> <br />![sand](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-sand.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-pulsar-ui.png?raw=true" alt="pulsar" style="width: 50px; height: 50px" /> ![coal](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-coal.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-poly-ui.png?raw=true" alt="poly" style="width: 50px; height: 50px" /> ![titanium](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-titanium.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-mega-ui.png?raw=true" alt="mega" style="width: 50px; height: 50px" />![zenith](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-thorium.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-zenith-ui.png?raw=true" alt="thorium" style="width: 50px; height: 50px" /><br /> ![scrap](https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/item-scrap.png?raw=true)=<img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-atrax-ui.png?raw=true" alt="atrax" style="width: 50px; height: 50px" /><br /><img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-nova-ui.png?raw=true" alt="nova" style="width: 50px; height: 50px" /> and <img src="https://github.com/acoaco/Mindustry-multi-binding-schematics-pack/blob/V7/icon/unit-pulsar-ui.png?raw=true" alt="pulsar" style="width: 50px; height: 50px" /> will auto turn on boost<br />set sorter to other and null=stop factory and set unit's flag to 0 | done |
| bind_template_with_switch_unit_factory_check | add a factory check block,check factory/container stat every 2 sec | done |
| bind_flare                                   | only flare no sorter,good for wireless Turret fast refill    | done |
| call_job_template                            | 2 most useful function in V7,easily set control unit trans resources | done |

------------

#### Eco:

check Template>bind_template_with_switch_unit for unit control detail

some autocheck will try add more units

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
| 8 Silicon |  8units |v7 transport speed faster,so change back to 8 silicon|done|
| 2 Blast | 2units |Change to 3 spore for v7<br />blast2 need build around water|done|
| 2 Differgen | 2units  |v7 transport speed faster,so remove button<br />2 flare can feed 4 differgen|done|
|  3 Glass  | 3units  ||done|
|  8 Graphite  | 3units  |v7 transport speed faster,so add 1 graphite| done |
|  2 Phase(sand)  | 1unit  | 2 units > 1 unit                                             | done                                   |
|  2 Phase  | 3units  |4 units > 3 units| done |
|  3 Plast(blacksand)  | 3units  |for white sand,remove 1 plast compressor|done|
|  1 Plast(water)  | 1units  |2 units > 1 unit|done|
| 2 Surge | 5units |if you use large storage units like zenith want consume more resources just copy some setup expand it to 4 surge|done|
|  Cent's item collect box  | 2units~4units |take items inside box back to core<br />when total items>100 auto add 2 units,save 2 mass driver<br />(P.S Cent are first person use it on pvp ranked server)| done |
| Dome | 2units |a dome has conveyor storage can run long time without flare keep refill<br />when conveyor1&2 has more than 5 items,it's stop flare<br />when dome less than 7 items it's call flare again| done |
| 3 Impact | 6units |For long game,can decide use free water or build water ex to feed it| done |



------------

#### Unit factory:

check Template>bind_template_with_switch_unit for unit control detail

unlike eco factory,unit factory is expensive,so autocheck overdrive try add more units

if no T3 factory it's bind 2 units for T1~T2

|  Name | Count | OD | no T3 factory<br />(T1~T2only mode) | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |  ------------ |  ------------ |
|T3 Fortress|3 units|4 units|2 units||done|
|T3 Spiroct|3 units|4 units|2 units||done|
|T3 Zenith|3 units|4 units|2 units||done|
|T3 Mega|4 units|5 units|2 units||done|
|T3 Bryde|4 units|5 units|2 units||done|
|T3 Quasar|4 units|5 units|2 units||done|
|T3 Cyerce|4 units|5 units|2 units||done|
|T1 3Risso|3 flares|||can't change unit type,for early game rush<br />when factory3 reach 70metaglass auto turn to 2 flares<br />no unit type switch function<br />a legacy schematic|ok|
|T4|6 units||||done|
|T5|5 units||||done|
|T4 T5 Cryo Fluid|1 units|||thank qqq for layout,60Cryo fluid,build 2 for T4,3 for T5|done|
|pulsar+poly+ pulsar mining|2 units|||auto use 1 unit when only has 1 T1 factory<br />can auto search sand now<br />include a pulsar mining logic<br />good for getting coal/sand/building speed at early game|done|
------------

#### Turret:

remove hail rader,it's doesn't need in V7

|  Name | Count | Description | stat |
| ------------ | ------------ |  ------------ |  ------------ |
|4 Thorium Salvo|2 flare|for faster refill speed,remove hail for v7|done|
|2 Hail+2 Scatter|2 flare|default sorter copper=don't hit building,other attack anything<br />if you don't need this control feature you can remove the sorter<br />use graphite and lead|done|
|6 Scatter|3 flare|a epic|done|
|2 Cyclone|2 flare|use plastanium ,other ammo too weak,or.. too expensive|done|
|1 Spectre|3 flare|same like Foreshadow|done|
|1 Cryo_Tsunami|1 flare|debuff air unit's speed so doesn't has lot ammo storage|done|
|2 Ripple|2 flare|use plastanium,other ammo too weak|done|
|1 Foreshadow|3 flare|2 for ammo,1 for Cryo Fluid,if you build lot(replace with T4 T5 Cryo Fluid) or use water you can remove mixer,it's will stop the mixer flare|done|

------

#### Mining Logic:

you can set keep at least how many copper and lead at logic's line 1,before mining other resources,default is 1k

| Name   | Description                                                  | stat |
| :----- | ------------------------------------------------------------ | ---- |
| Mono   | keep 1k copper and lead then try balance between lead/copper/sand,this one has a auto unloader config make 1 unloader can feed 2 mono factory | done |
| Pulsar | keep 1k copper and lead then try balance between sand/coal   | done |
| Quasar | keep 1k copper and lead then try balance between  sand/coal/titanium | done |
| Mega   | keep 1k copper and lead then try balance between  sand/coal/titanium | done |

