# Implementation Plan

* how much time do we need?
	* planning
	* training
	* testing
	* phase out
	* rollout
* How many people do we need?
	* what type/expertise?
	* project management
	* teams
	* admins
* training
	* end users
	* admins
	* develop in house expertise
* solutions
	* which style of VoIP deployment is best?
	* which state of protocols/standards should we go with?
	* are we qualified to make the decision?
	* how much should vendors be involved?

# Comparisons

* features vs cost vs standards

* ask community about usage
* examine workflows (especially for UC)
	* can you improve efficiency or productivity?
* create an RFP

# RTP

Real time transport protocol

* RFC 1889 (3550)
* end to end transport functions suitable for applications transmitting real time data
* by parts
	* sequencing
	* payload ID
	* UDP based
		* ports RTP is supposed to be even; RTCP is the next odd port
	* RFC includes both RTP and RTCP
* not a complete standard, often built into an app
* but it is designed to handle most of the required functions
	* expandable and flexible

## Header fields

* version 
	* 0 - original
	* 1 - RTP draft
	* 2 - 1889
* padding - indicates that the packet includes padded octets that are not part of the payload (A/V stream)
* extension - this header is followed by an extension header
* constributing service ID count
* marker - indicates important boundaries in the RTP stream ex. sample end
* payload
	* format of the data in the data field
	* often selected before transmission
	* codes are part of the profiles in RFC 3551
	* ex. 00 is G.711
	* audio - lower numbers
	* vide - upper
	* dynamic
* sequence numbers
	* increment by 1 for each packet sent
	* start number is supposed to be random
* timestamp
	* sample time of the first octet
	* clock is critical
		* ex. jitter calculation
* synchronizing source (SSRC)
	* random identifier for the sources *not* based on the net id (ip addrs) groups packets for playback
* contributing source (CSRC)
	* lists other source source IDs for the payload if present
	* important for mixing or multiplexing