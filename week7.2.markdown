# RTCP

* real time control protocol
* purpose
	1. provides feedback on quality
		* can be useful for QoS or encoding changes
		* can be a multicast function
	2. carries a persistent transport ID for each uses in case the SSRC changes
		* called the CNAME
		* also used to synchronize streams with users
	3. all participants **MUST** send RTCP packets
		* used to help control data rates and determine the number of users
	4. optional
		* convey session info

## Message types

* sender report (SR) - from active sender, NTP, packet count
* receiver report (RR) - from "not active" senders
* source description (SDES)
* BYE
* APP - application specific

# Unified Communications

##Problems

1. multiple ways to communicate
2. multiple devices and capabilities
3. assortment of communication entities or IDs
4. several different addresses or numbers

## Elements

1. Unified portal to control all: easy to use, similar features for all
2. integration: you decide how to send it, I decide how to pick it up
3. reachability, presence and the ability to control it
	* I decide what gets to me and how

**UC** - made up of many tools and components

* call control and multimodal communications
* presence
* instant messaging
* unified messaging
* speech access and personal assistant
* conferencing: audio, video and web
* collaborative tools
* mobility
* business process integration

## Keys

1. Integration with voice
	* ex. click to call
2. presence: offline and online
3. unified interface

* **COLLABORATION AND PRESENCE AND MOBILITY USED TO IMPROVE EFFICIENCY, REDUCE STRESS AND IMPROVE PRODUCTIVITY**