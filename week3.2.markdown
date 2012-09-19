# H.225

* call setup and teardown
* framing for audio and video
* synchronization and sequencing
* port 1720
* other stuff
	* H.225 - Q.731 - call setup and framing
	* H.225 - RAS - communication with gatekeeper
* steps
	1. setup
	2. call proceding
	3. alerting
	4. connect
	5. release complete
	6. facility
* encapsulated in TPKT + Q.731
	* transport sequence for TCP
* during the connect, the IP address and port to be used by the called station are sent back to the calling station
	* ports are dynamic
* routing can be handled via direct endpoint call signaling
* or gatekeeper routing call signaling (GKRCS)
	* this centralizes accounting and allows other apps

# H.245

* Call control procedures
* end to end messages for the logical channel
* flow control sync between send and receiver, capabilities exchange (ex. codec), chanelling
* codec selection
* like H.225, these can be between endpoints or via the gatekeeper
* can also be handled inside H.225 messages
* H.323 info is exchanged via ASN.1 format
* message types 
	* requests - command that requires a response
	* command - does not require a response
	* response - answer to a request
	* indication - info message
* messages are often tied to a procedure like open_logical_channel
	* but they may not be (SendTerminalCapabilitySet)
* also inside TPKT
* header indicates a type and then a the codec
* type/codec combos
	1. master/slave determination + ack
	2. term cap set + ack
	3. open logical channel + ack
	4. flow control
* Capability exchange
	* used to describe what terminals/endpoints can do
	* transmit and receive are separate ideas
	* encryption is part of it (H.235)
	* enumerated in the capability table
		* capability number and name
* Master / Slave determination
	* 2 important numbers
		* TT (terminal type)
		* SDNUM (status determination number)
* H.323 gateways can terminate calls between endpoints on their own VoIP net 
	* can also act as an actual gateway to another IP net or the PSTN

## Port numbers

* 1719-1720 - H.225
* 1720, 1080, 2060, dyn - H.245

# H.323 Security

* not mandated but supported by H.235
* VoIP encryption focuses on either the signaling protocol, RTP stream or both
* Annex D - symmetric
* Annex E - asymmetric
* Annex G - secure RTP