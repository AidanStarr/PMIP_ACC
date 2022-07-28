# PMIP_ACC
Repository to develop a workflow for analysing PMIP model outputs in the pangeo framework. 

## Sediment core records (SS records spanning last glacial cycle; some still to generate)
- MD02-2588 (Agulhas Plateau) -- 41°20'S, 25°49.7′E, 2907 m water depth
- MD02-2589 (Agulhas Plateau) -- 41°26'S, 25°15.30′E, 2660 m water depth
- TT1811-34GGC (SE Indian) -- 41°43'S, 80°9'E, 3167 m water depth
- TT1811-50GGC (SE Indian) -- 38°20'S, 77°43'E, 1116 m water depth
- TT1811-71GGC (SE Indian) -- -35°35'S, 80°50'E, 2598 m water depth
- RS149-GC07 (South Tasman Rise) -- 45°09'S, 146°17'E, 3300 m water depth


## Project Objectives

### Phase 1: Examine ACC flow speeds in PMIP4 experiments
Need `uo` variable for `piControl` and `lgm` experiments. 

Objective is to **extract eastward velocity at location of sediment core sites**. 

1. Was eastward velocity stronger or weaker at each location during the lgm, relative to piControl?
2. How well do PMIP4 models and sediment core proxies (sortable silt) agree?

_note: `vo` may also be useful here if we think speed rather than velocity is a better metric_

### Phase 2: Compare velocity/speed to additional metrics from each model/experiment
Compare ACC strength/core position to additional variables such as wind stress and sea ice. Try to exploit inter-model differences to better understand the sensitivty of the ACC to different forcing on glacial-interglacial timescales. Link this to sortable silt by incorporating additional proxy data.

#### ACC metrics
- Intergrated ACC transport through key longitudes (Drake Passage, Greenwich Meridian, Amsterdam-Kerguelen Passage)
- ACC core position: following [Sen Gupta et al., 2009](https://doi.org/10.1175/2008JCLI2827.1): 
> at each longitude, an average of latitude weighted by the depth-integrated zonal flow strength is calculated to obtain an estimate of the average core position (using only those latitudes where the zonal flow exceeds 50% of the maximum eastward flow magnitude). Core strength is then simply the mean depth-integrated velocity over these values. While this strength estimate does not correspond to the maximum core strength (as it includes everything to 50% of the maximum), it provides a representative magnitude for the ACC core”


#### Additional metrics
- Metrics for front positions: need `thetao` and `so` 
- Westerly wind stress: need `uas` from atmospheric realm 
- Sea ice extent: need `sic`

