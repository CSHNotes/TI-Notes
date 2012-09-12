# Why go VoIP?

1. Cost - toll charges
	- maintenance
	- cost of equipment
	- one type of network to maintain
2. Management
	- Devices and the PBX are IP based, familiar and probably simpler
3. Upgrades and scalability
	- off the shelf components
	- well understood licensing
4. Server based
	- same recovery and management issues
5. no need to throw out old equipment
6. more and more vender/standard support
	- SIP
7. soft phones

# Public Switched Telephone Network (PSTN)

## Global network
- In 2004 there were about 200 million traditional landlines in the US (ITU-T)
- The PSTN handles connections for all of these
- Several different types of connections (analog, cellular, digital)
- Switched net where connections are setup and torn down as needed
- calls are multiplexed over some links which minimizes the number of physical links
- home and small businesses usually have analog connections and POTS
- Connections between sites and switches are usually digital. Internal sites using a PBX are also commonly digital
- Signaling System 7 is the overlay network within the PSTN that controls everything
	- call setup, billing, 800, long distance, etc.
- POTS (Plain old telephone service)
	- simple electrical loop to a home
	- very reliable with a few basic services
- phone connections are lines
- office/switch connections are links or trunks

## Frames
- distribution frame
	- low density for subscribers (copper) for 2-25 pair
	- aggregation point
	- high density (50-800 pair)
- main dest frame
	- includes switchying or encoding support
		- DSL
	- greater density (fiber) to CO

## Central Office
- contains the local exchange switch
- typically a telephone prefix (ex. 475) identifies the CO
- a CO may be a group of COs

## LATA
- Local access transport area
- 196 geographic ares in which a local telco can provide services
	- telco aka Local Exchange Carrier (LEC)

## IXC - interexchange carrier
- long distance = inter-LATA
- ex. ATT, Sprint
- some IXC now operate as CLECs

## PSTN
- made up of LATAs, IXCs, CLEC, ILEC
- highly geographic & highly regulated

# Telephone numbers
- ITU-T E.164 International Telecom Numbering Plan
- In North America, we use the NANP (North American Numbering Plan) which complies with E.164

1Nxx-Nxx-xxxx    N = 2-9     x = 0-9
(area code) (prefix (switch assignment)) (station code (port/circuit))