# Dial plan

* Tells the system how to interpret the numbers dialed
	* pattern matching
	* Includes:
		* special digits
		* feature access codes (FAC)
		* dial access codes (DAC)
* often setup before the system is deployed
* everything to be dialed must be entered into the dial plan
* dial plans also cover devices that can be contacted
	* fax
	* modem
	* extensions are not just phones

## Best Practices

* 911
	* 911 has to be able to find you wherever you are in the world
		* Goes to the 911 closest to your area code
	* 9-911
		* What your phone translates to if you need to dial 9 to get out
	* E911
		* GPS and cell tower triangulation
* 411? (555-1212)
* extensions/phone numbers
* trunks/dial access
* Direct inward dial
* Feature access codes

# Wiring

* tip and ring 
	* pair of wires to a particular set 
	* ring (red)
	* tip (green)
	* positive + negative connections
	* 48v DC (ringing: 90v AC)
* 568A + B
	* standards used for telco and data cabling (structured)
	* each pair is actually a tip and ring connection
	* pins 4+5 are the telco pair
* Use auto-negotiation to figure out how shit's wired so you don't need to care

## Household Pairs

* typically 4 wires (we use 2)
* pair 1 (green + red)
* pair 2 (yellow + black)
* all the phones are wired together

## Local Loop

* In band signaling
	* discrete multitone sounds from the keypad which indicate telephone #, dialtone, etc.
* digital signal 0 (DS-0)
	* base circuit for the telco line
	* basis for higher connection circuits
	* digital version of a single line or local loop
	* pulse code modulation
	* 64kbps
		* 8 bits per sample
		* 8000 samples per second

# PRI/T-1

* PRI
	* ISDN primary rate interface at 1.544 Mbps
	* 23B+D
		* B - Bearer channel
		* D - Data channel
* T-1
	* 24 Channels for voice, each at 64kbps
	* Q.931
	* G.701-G.704