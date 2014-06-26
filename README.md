`speedboat` is a Python-based CLI Control Panel for [Digital Ocean](https://digitalocean.com).

Installation
============

speedboat relies on the `requests` library.

	# if requests is not installed:
	# sudo easy_install pip
	# sudo pip install requests
	git clone https://github.com/crylico/speedboat.git
	cd speedboat && cp speedboat /usr/local/bin
	chmod +x /usr/local/bin/speedboat

Setup
=====

Setup speedboat  		- `speedboat setup`

You can get your Client and API keys [here](https://developers.digitalocean.com).

	kyles-mbp:~ kyle$ speedboat setup
	Speedboat - the Digital Ocean CLI


	Digital Ocean API Credentials
	=============================

	Enter your client key:
	Enter your api key:

	kyles-mbp:~ kyle$

Listing Information
===================

List All Droplets 		- `speedboat drops`

List All Regions		- `speedboat regions`

List All Sizes			- `speedboat sizes`

List All SSH Keys		- `speedboat keys`

List Private Images		- `speedboat images`

List Global Images 		- `speedboat images global`

List All Images 		- `speedboat images all`

	kyles-mbp:~ kyle$ speedboat drops
	Speedboat - the Digital Ocean CLI

	Droplets
	========
	kylelevin.com - ip: 162.243.175.67 - status: active - region: 1 - id: 1332093
	dev.kylelevin.com - ip: 162.243.170.87 - status: active - region: 1 - id: 1380768
	vpn.kylelevin.com - ip: 162.243.170.88 - status: active - region: 1 - id: 1380771
	server.kylelevin.com - ip: 162.243.170.89 - status: active - region: 1 - id: 1380772

	kyles-mbp:~ kyle$ speedboat sizes
	Speedboat - the Digital Ocean CLI

	Sizes
	=====
	ID: 66 - 512MB
	ID: 63 - 1GB
	ID: 62 - 2GB
	ID: 64 - 4GB
	ID: 65 - 8GB
	ID: 61 - 16GB
	ID: 60 - 32GB
	ID: 70 - 48GB
	ID: 69 - 64GB

	kyles-mbp:~ kyle$

Droplet Commands
================

Create New Droplet 	- `speedboat new`


Restart	- `speedboat restart <name>`

Power Cycle	- `speedboat cycle <name>`

Shutdown - `speedboat shut <name>`

Power Off - `speedboat off <name>`

Power On - `speedboat on <name>`

Snapshot - `speedboat snap <name>`

Print Info - `speedboat info <name>`

Resize - `speedboat resize <name>`

Destroy - `speedboat destroy <name>`

*\<name\> argument is optional, except for the destroy command*

###Without \<name\>

	kyles-mbp:~ kyle$ speedboat restart
	Speedboat - the Digital Ocean CLI

	Droplets
	========
	(0) kylelevin.com - ip: 162.243.175.67 - status: active - region: 1 - id: 1332093
	(1) dev.kylelevin.com - ip: 162.243.170.87 - status: active - region: 1 - id: 1380768
	(2) vpn.kylelevin.com - ip: 162.243.170.88 - status: active - region: 1 - id: 1380771
	(3) server.kylelevin.com - ip: 162.243.170.89 - status: active - region: 1 - id: 1380772
	(x) Cancel

	Which droplet would you like to restart? 2

	Restarting vpn.kylelevin.com...
	Done!

	kyles-mbp:~ kyle$

###With \<name\>

	kyles-mbp:~ kyle$ speedboat restart dev
	Speedboat - the Digital Ocean CLI

	Restarting dev.kylelevin.com...
	Done!

	kyles-mbp:~ kyle$

Help
====

	kyles-mbp:speedboat kyle$ speedboat help
	Speedboat - the Digital Ocean CLI

	List Digital Ocean Information
	==============================

	List all Droplets 		- speedboat drops
	List All Regions 		- speedboat regions
	List All Sizes 			- speedboat sizes
	List All SSH Keys 		- speedboat keys
	List Private Images 	- speedboat images
	List Global Images 		- speedboat images global
	List All Images 		- speedboat images all

	List of Droplet Commands
	========================

	Create New Droplet 	- speedboat new
	Restart 			- speedboat restart <name>
	Power Cycle 		- speedboat cycle <name>
	Shutdown 			- speedboat shut <name>
	Power Off			- speedboat off <name>
	Power On			- speedboat on <name>
	Snapshot 			- speedboat snap <name>
	Print Info 			- speedboat info <name>
	Resize 				- speedboat resize <name>
	Destroy 			- speedboat destroy <name>

	kyles-mbp:speedboat kyle$
