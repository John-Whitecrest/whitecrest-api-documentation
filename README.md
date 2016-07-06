# Whitecrest Mushrooms

This API lists all the growers associated with a site, sends information about hardware status, and shows data about picking, packing, and mushroom growing.

## Endpoints and API Access

For ItemPath (or any other application) to access data from the grower, an endpoint structure will need to be set up. Either the growers each will need to be connected to the internet and have an endpoint where this API is accessible, or each site will need to have a global processor to take data from the growers and provide a single endpoint to connect to.

## Core Concepts and Routes


### Hardware

* *Grower:* A grower is a single unit consisting of beds, a lift, cart, scale and a harvester. Inside a grower there are mushrooms growing on beds, spread over multiple vertical levels.
    * *Scale:* The scale weighs each packed lug of mushrooms.
    * *Lift:* The lift is the apparatus that moves the harvester between levels.
    * *Harvester:* The cart and robotic arm mechanism that scans and picks mushrooms off of a bed and brings them to a packer.
* *Level:* A level is a horizontal position within a grower and contains a collection of beds.
* *Bed:* A bed is a soil area on a level where mushrooms are grown.
* *Mushroom:* Mushrooms grow on a bed.
* *Lug:* The bin that contains trays of mushrooms.
* *Tray:* A tray is where harvested mushrooms are placed on, and are put into lugs.

### Events

* *Harvest:* The action of picking a mushroom.
* *Scan:* When the grower records mushroom changes on a bed.
* *Test:* When a bed's temperature, pH, moisture, and humidity is recorded.
* *Pack:* The action of putting a tray into a lug.
* *Release:* When the lug is sent from the grower.
