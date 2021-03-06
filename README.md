# Turin SUMO Traffic (TuST) Scenario

Contacts: Marco RAPELLI [rapelli.m@libero.it], Claudio CASETTI [claudio.casetti@polito.it] and Giandomenico GAGLIARDI [giandomenico.gagliardi@5T.torino.it]

This project is licensed under the terms of the GPLv3 license.

TuST Scenario is meant to be used with SUMO (Simulator of Urban MObility) and is developed with [SUMO 1.1.0](https://github.com/eclipse/sumo/tree/v1_1_0).

Please refer to the [SUMO wiki](http://sumo.dlr.de/wiki/Simulation_of_Urban_MObility_-_Wiki) for further information on the simulator itself.

### Overview

The _TuST (Turin SUMO Traffic)_ simulation scenario describes the traffic within the city of Turin, Italy for a whole day. The original demand data stems from real traffic data of 5T, a public agency managing all the traffic mobility data in the Italian region of Piemonte.

From the original OSM file, an accurate road graph was created using real average velocities from Google APIs and real traffic light phases from 5T data.

To validate the model, traffic flows were compared to real flows measured from 5T street sensors, crating in this way a very realistic large-scale simulator.

### Case Study Map

![Case Study Map](Map.png)

## Publications: [BibTeX](cite.bib)

Best paper award of DS-RT 2019 to M. Rapelli, C. Casetti, G. Gagliardi,
*"TuST: from Raw Data to Vehicular Traffic Simulation in Turin"*
2019 IEEE/ACM 23rd International Symposium on Distributed Simulation and Real Time Applications (DS-RT)
October, 2019, Cosenza, Italy.

## How To

TuST project includes two scenarios:

* A complete traffic demand scenario with the full-day O/D traffic of Turin and vehicles with 1.8m length.
* A scenario with 80% of full-day O/D traffic of Turin and vehicles with normal length.

Both TuST scenarios can be lunched directly with their configuration file.

* `sumo -c Torino_shortCars.sumocfg` or `sumo -c Torino_normalCars.sumocfg` from the corresponding scenario folder.

In order to rebuild the routes it is possible to lunch the route configuration files.

* `marouter -c RoutingConfig_shortCars.xml` or `marouter -c RoutingConfig_normalCars.xml` from the corresponding scenario folder.

### Available Outputs

Inside each scenario folder it is possible to find three different outputs:

* _Summary_ file with general simulation outputs.
* _DetectorsOutput_ file with edge-based simulation outputs.
* _VehTraces_ file with the full vehicles traces available.

### IMPORTANT: this wiki page is a work in progress. Do not hesitate to ask for help
